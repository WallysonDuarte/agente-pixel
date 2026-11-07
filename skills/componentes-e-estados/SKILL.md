---
name: componentes-e-estados
description: Construir biblioteca de componentes com variantes, todos os estados de interacao e estados de tela desenhados.
---

# Componentes e estados

## Quando usar

Criacao da biblioteca, componente novo, revisao de componente existente.

## Estados de interacao — obrigatorios

Todo elemento interativo tem **sete** estados. Falta de qualquer um e entrega incompleta:

| Estado | Regra |
|---|---|
| repouso | aparencia base |
| sobre o cursor | mudanca perceptivel, sem deslocar o layout |
| foco | contorno visivel, com contraste minimo de 3:1 contra o fundo |
| pressionado | retorno imediato ao toque |
| desabilitado | contraste reduzido **e** motivo visivel ao lado |
| carregando | indicador no proprio elemento, largura preservada |
| erro | borda e mensagem, nao apenas cor |

Botao desabilitado sem explicacao e defeito de experiencia. Mostre a condicao que falta.

Troca de estado nunca pode alterar a largura do elemento: reserve o espaco do indicador de
carregamento desde o inicio.

## Variantes

- **Intencao:** primaria, secundaria, discreta, destrutiva.
- **Tamanho:** pequeno, medio, grande. Em tela de toque, alvo de no minimo 44 px.
- Combinacoes documentadas; combinacao nao prevista nao e criada no uso.

Regra global de altura minima para toque deforma controle compacto (ponto de navegacao vira oval,
icone redondo vira elipse). Aplique altura minima zero nesses controles.

## Componentes essenciais

Botao, campo de texto, campo de senha com alternancia, selecao, caixa de marcacao, opcao unica,
alternador, cartao, janela modal, aviso temporario, etiqueta, avatar, abas, secao expansivel,
caminho de navegacao, paginacao, tabela, indicador de carregamento, estado vazio.

### Janela modal

- Fecha por tres caminhos: botao, clique fora e tecla de escape.
- Foco preso dentro da janela enquanto aberta; retorna ao elemento de origem ao fechar.
- Rolagem do fundo bloqueada.
- Menu suspenso dentro de area com rolagem pode ser cortado: eleve a camada do elemento aberto ou
  posicione de forma fixa.

### Tabela

- Cabecalho fixo em listagem longa.
- Coluna de acoes fixa no lado, com camada maior que as celulas das linhas seguintes — senao o
  menu aberto fica coberto.
- Rolagem horizontal com barra visivel explicitamente estilizada: no sistema que oculta a barra
  automaticamente, a tabela parece cortada mesmo rolando.
- Reduza a largura necessaria antes de recorrer a rolagem (quebre valor composto em duas linhas).

## Estados de tela

Cinco telas por rota, nao uma:

1. **Carregando** — esqueleto com a forma do conteudo, nao apenas um girador centralizado.
2. **Vazio** — explica o que aparecera ali e oferece a acao que preenche.
3. **Com dados** — o caso comum.
4. **Sem resultado** — diferente de vazio: mostra o filtro aplicado e como limpa-lo.
5. **Erro** — o que falhou e um botao de nova tentativa.

## Microinteracoes

- Transicao entre 150 ms e 300 ms. Entrada com desaceleracao, saida com aceleracao.
- Retorno imediato a toda acao: nenhum clique fica sem resposta visivel.
- Respeite a preferencia de movimento reduzido do sistema desabilitando animacao.

## Checklist

- [ ] Sete estados de interacao em todo elemento interativo
- [ ] Largura preservada na troca de estado
- [ ] Alvo de toque com 44 px, sem deformar controle compacto
- [ ] Modal com tres formas de fechar, foco preso e rolagem bloqueada
- [ ] Tabela com cabecalho fixo e camada correta na coluna de acoes
- [ ] Cinco estados de tela em cada rota
- [ ] Animacao respeitando preferencia de movimento reduzido

## Pronto quando

Cada componente tem todos os estados demonstraveis, e nenhuma rota consegue exibir tela branca.
