---
name: acessibilidade
description: Garantir conformidade pratica com as diretrizes de acessibilidade: contraste, semantica, teclado, leitor de tela e formulario.
---

# Acessibilidade

## Quando usar

Em toda tela. Acessibilidade entra no desenho; corrigir depois custa tres vezes mais.

## Contraste

| Conteudo | Minimo |
|---|---|
| Texto normal | 4.5:1 |
| Texto grande (24 px, ou 19 px em negrito) | 3:1 |
| Componente de interface e indicador de foco | 3:1 |
| Elemento puramente decorativo | sem exigencia |

Verifique com ferramenta, nao a olho. Texto cinza-claro sobre branco e a falha mais comum.

Cor nunca e o unico portador de informacao: situacao precisa de icone ou texto, alem da cor.

## Semantica primeiro

Use o elemento nativo. Marcacao auxiliar existe para o que o HTML nao expressa — nao para
substituir o que ele ja expressa.

| Em vez de | Use |
|---|---|
| caixa com evento de clique | `<button>` |
| caixa com papel de link | `<a href>` |
| caixa com papel de lista | `<ul>` / `<li>` |
| texto grande em negrito | `<h1>`...`<h6>` |

Estrutura da pagina: `header`, `nav`, `main` (um por pagina), `aside`, `footer`. Hierarquia de
titulos sem salto de nivel.

## Teclado

- Tudo que se faz com o ponteiro se faz com o teclado.
- Ordem de tabulacao segue a ordem visual.
- Foco **sempre** visivel. Remover o contorno sem substituto e uma das piores falhas possiveis.
- Tecla de escape fecha sobreposicao; setas navegam em grupo de opcoes; espaco e enter acionam.
- Link de salto para o conteudo principal, como primeiro elemento focavel.
- Foco preso dentro de janela modal enquanto aberta, e devolvido ao fechar.

## Leitor de tela

- Imagem informativa com texto alternativo descritivo; imagem decorativa com alternativo vazio.
- Conteudo que muda sozinho (aviso, resultado de busca) dentro de regiao anunciada.
- Icone sem texto precisa de nome acessivel.
- Nenhum conteudo escondido do leitor por mero efeito visual.

## Formulario

- **Rotulo associado ao campo por identificador.** Texto ao lado nao e rotulo. Sem isso, o campo
  nao tem nome acessivel e nao e alcancavel por teste automatizado.
- Mensagem de erro vinculada ao campo por referencia de descricao.
- Campo obrigatorio marcado de forma programatica, nao apenas com asterisco.
- Agrupamento de opcoes relacionadas com legenda.
- Nunca usar apenas o texto de exemplo dentro do campo como rotulo: ele desaparece ao digitar.

## Movimento

Respeite a preferencia de movimento reduzido: desabilite animacao, transicao e rolagem automatica.
Nada que pisque mais de tres vezes por segundo.

## Checklist

- [ ] Contraste conferido com ferramenta em todos os textos
- [ ] Cor nao e o unico portador de significado
- [ ] Elementos nativos; marcacao auxiliar so onde necessaria
- [ ] Um `main` por pagina, titulos sem salto de nivel
- [ ] Fluxo completo navegavel por teclado, com foco visivel
- [ ] Link de salto presente
- [ ] Todo campo com rotulo associado
- [ ] Erro vinculado ao campo
- [ ] Preferencia de movimento reduzido respeitada

## Pronto quando

O fluxo central se completa usando apenas o teclado, o foco e sempre visivel, e nenhum campo fica
sem nome acessivel.
