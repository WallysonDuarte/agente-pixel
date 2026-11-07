---
name: layout-responsivo
description: Construir layout que funciona de 320 px a telas largas, sem estouro horizontal, com verificacao automatizada.
---

# Layout responsivo

## Quando usar

Toda tela nova e toda correcao de layout relatada como "quebrado no celular".

## Base

Primeiro o tamanho pequeno. Escreva o layout para a largura minima e amplie com pontos de corte,
nunca o contrario.

Pontos de corte de referencia: 640, 768, 1024, 1280 e 1536 px. Teste sempre em **375 px, 768 px e
1440 px**.

## Ferramentas, em ordem

1. **Fluxo natural** — a maioria do conteudo nao precisa de nada.
2. **Caixa flexivel** com intervalo — alinhamento em uma dimensao.
3. **Grade** — layout em duas dimensoes (paineis, cartoes).
4. **Consulta de container** — componente que se adapta ao espaco do pai, nao da janela. Mais
   robusto para peca reutilizavel.
5. Posicionamento absoluto apenas para sobreposicao.

Nunca use flutuacao para layout.

## Causas recorrentes de estouro horizontal

- Elemento com deslocamento lateral inicial de animacao de entrada.
- Largura minima de conteudo em celula de tabela sem container com rolagem.
- Imagem sem largura maxima de 100%.
- Texto longo sem quebra (URL, identificador).
- Unidade de largura total somada a preenchimento lateral.

Defesa: no elemento raiz, impedir rolagem horizontal; e corrigir a causa, nao apenas esconder.

## Cabecalho fixo

Cabecalho fixo cobre o inicio do conteudo. A primeira secao precisa de preenchimento superior
maior que a altura do cabecalho, com folga. Ancora de rolagem tambem precisa de deslocamento.

## Altura de tela em dispositivo movel

Use a unidade de altura dinamica da janela em vez da altura fixa: a barra do navegador aparece e
desaparece, e a unidade fixa provoca corte e salto.

## Imagem e midia

- Largura e altura declaradas para reservar o espaco e evitar deslocamento de conteudo.
- Conjunto de tamanhos para servir a imagem adequada a cada largura.
- Proporcao explicita; imagem retangular dentro de area quadrada precisa de ajuste de
  preenchimento para nao cortar o assunto.
- Carregamento tardio fora da primeira tela; a imagem principal carrega com prioridade.

## Verificacao automatizada

Vale mais que inspecao manual. Percorra todas as rotas publicas em tres larguras verificando:

- largura do conteudo maior que a largura visivel (estouro)
- texto da primeira secao coberto pelo cabecalho fixo
- botao com proporcao deformada
- elemento circular com largura diferente da altura
- alvo de toque abaixo de 44 px

Guarde o roteiro no repositorio e rode a cada mudanca de estilo.

## Checklist

- [ ] Layout escrito do menor para o maior
- [ ] Testado em 375 px, 768 px e 1440 px
- [ ] Nenhuma rolagem horizontal
- [ ] Primeira secao com folga em relacao ao cabecalho fixo
- [ ] Altura dinamica da janela em tela cheia
- [ ] Imagem com dimensoes declaradas e largura maxima
- [ ] Varredura automatizada passando

## Pronto quando

Nenhuma rota tem estouro horizontal nas tres larguras, e a varredura automatizada passa limpa.
