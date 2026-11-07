---
name: revisao-de-interface
description: Roteiro de revisao visual e de experiencia antes de aprovar uma tela, incluindo propagacao da correcao para telas irmas.
---

# Revisao de interface

## Quando usar

Antes de aprovar qualquer tela nova ou alterada.

## Roteiro

### Hierarquia
- [ ] Um unico elemento dominante por tela
- [ ] Ordem de leitura clara: titulo, subtitulo, corpo, apoio
- [ ] Acao principal com mais peso visual que a secundaria
- [ ] Acao destrutiva visualmente distinta e nunca adjacente a acao comum

### Espaco
- [ ] Multiplos de 4 px
- [ ] Elementos relacionados mais proximos entre si do que de outros grupos
- [ ] Respiro nas bordas; em tela estreita, margem lateral de 16 px

### Cor e tipografia
- [ ] Somente simbolos do sistema
- [ ] Cor semantica correta (sucesso, aviso, erro, informacao)
- [ ] No maximo tres tamanhos de texto por tela
- [ ] Nenhum texto com contraste abaixo do minimo

### Conteudo
- [ ] Textos no idioma do usuario, com acentuacao correta
- [ ] Rotulo de botao no imperativo, dizendo o que acontece ("Salvar alteracoes", nao "Enviar")
- [ ] Mensagem de erro diz o que fazer, nao apenas o que falhou
- [ ] Nenhum texto de exemplo ou conteudo de preenchimento esquecido

### Comportamento
- [ ] Carregamento em toda acao assincrona
- [ ] Retorno visivel de sucesso
- [ ] Erro ao lado do campo, alem do aviso geral
- [ ] Nenhum dialogo nativo do navegador
- [ ] Alteracao nao salva avisa antes de sair — e **nao** avisa quando a sessao ja expirou, senao a
      saida forcada travaria no aviso

### Responsividade e acessibilidade
- [ ] Tres larguras verificadas, sem estouro horizontal
- [ ] Navegacao por teclado completa, foco visivel
- [ ] Rotulo associado em todo campo

## Propagacao da correcao

Ao corrigir um defeito visual, procure **todas** as telas que usam a mesma fonte de dado ou o mesmo
componente. Correcao em uma tela deixa as irmas com o mesmo defeito, e o relato volta na semana
seguinte.

Em gerador de site estatico, correcao em componente compartilhado alcanca todas as paginas
automaticamente — mas confirme amostrando duas ou tres paginas servidas, porque uma delas pode usar
outra classe parecida de uma versao antiga.

## Cache ao corrigir recurso estatico

Arquivo de imagem, estilo ou script substituido com o mesmo nome continua sendo servido da versao
antiga pela rede de distribuicao. Compare o resumo criptografico do arquivo publico com o local; se
divergir, versione o **nome** do arquivo em vez de esperar o tempo de expiracao.

Quando o relato for "continua errado" logo depois de uma publicacao, verifique isso **antes** de
mexer no desenho.

## Checklist de aprovacao

- [ ] Roteiro completo percorrido
- [ ] Correcao propagada para telas irmas
- [ ] Versao servida confirmada (resumo do arquivo)
- [ ] Captura de tela nas tres larguras anexada

## Pronto quando

A tela passa o roteiro inteiro, as telas irmas receberam a mesma correcao, e a versao servida e
comprovadamente a nova.
