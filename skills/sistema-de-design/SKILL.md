---
name: sistema-de-design
description: Definir e aplicar simbolos de cor, espaco, tipografia e elevacao, com tema claro e escuro consistentes.
---

# Sistema de design e simbolos

## Quando usar

Projeto novo, unificacao visual entre aplicacao e painel, troca de identidade, inconsistencia
visual recorrente.

## Simbolos (tokens)

Nenhum valor visual aparece solto no componente. Tudo vem de um simbolo declarado em um unico
lugar.

### Cor

Organize em tres niveis:

1. **Paleta bruta** — a escala de cada matiz (por exemplo, 50 a 900).
2. **Simbolo semantico** — o papel: `superficie`, `superficie-elevada`, `borda`, `texto`,
   `texto-suave`, `primaria`, `primaria-texto`, `sucesso`, `aviso`, `erro`, `informacao`.
3. **Uso no componente** — o componente consome somente o nivel 2.

Tema escuro e claro redefinem o nivel 2, nunca o componente.

```css
:root {
  --superficie: #ffffff;
  --superficie-elevada: #f6f8fa;
  --borda: #d0d7de;
  --texto: #1f2328;
  --texto-suave: #656d76;
  --primaria: #0969da;
  --sucesso: #1a7f37;
  --aviso: #9a6700;
  --erro: #cf222e;
}

:root:not([data-tema="claro"]) {
  @media (prefers-color-scheme: dark) {
    --superficie: #0d1117;
    --superficie-elevada: #161b22;
    --borda: #30363d;
    --texto: #e6edf3;
    --texto-suave: #8b949e;
    --primaria: #58a6ff;
    --sucesso: #3fb950;
    --aviso: #d29922;
    --erro: #f85149;
  }
}

:root[data-tema="escuro"] { /* mesmas redefinicoes */ }
```

O corpo da pagina sempre declara cor de fundo explicita — sem isso, o tema do sistema vaza.

### Espaco

Grade base de 4 px. Toda margem, preenchimento e intervalo e multiplo dela. Escala sugerida:
4, 8, 12, 16, 24, 32, 48, 64.

### Tipografia

Simbolos para familia, tamanho, peso e altura de linha. Escala com razao constante (por exemplo
1,25): 12, 14, 16, 20, 25, 31, 39. Altura de linha maior para texto corrido (1,5) e menor para
titulo (1,2).

### Raio e elevacao

Dois ou tres raios no maximo (pequeno, medio, redondo). Elevacao por sombra em tres niveis:
repouso, flutuante, sobreposto.

## Tema escuro sobre componentes encapsulados

Quando o estilo do componente e encapsulado, a sobrescrita global precisa de especificidade maior
que o seletor gerado. Sobrescreva superficie, borda, texto, campo de formulario e tabela — e
**exclua** elementos que carregam cor por significado (etiqueta de situacao, indicador de
gravidade), senao eles ficam ilegiveis.

## Antipadroes

- Valor de cor escrito dentro do componente.
- Simbolo com nome de aparencia (`azul-claro`) em vez de papel (`informacao`).
- Escala de espaco com valores arbitrarios (13 px, 27 px).
- Mais de duas familias tipograficas.
- Tema escuro feito por filtro de inversao.

## Checklist

- [ ] Nenhum valor visual fixo no componente
- [ ] Simbolos com nome de papel, nao de aparencia
- [ ] Espaco em multiplos de 4 px
- [ ] Tema claro e escuro definidos nos tres pontos (preferencia do sistema e atributo explicito)
- [ ] Cor de fundo explicita no corpo da pagina
- [ ] Elementos semanticos preservados no tema escuro

## Pronto quando

Trocar a cor primaria em um arquivo muda toda a aplicacao, e os dois temas ficam legiveis sem
ajuste pontual.
