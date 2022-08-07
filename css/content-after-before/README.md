# Content after e before

Sempre que usarmos as pseudo classes `:after` e `:before`
devemos obrigatoriamente, da propriedade `content` (mesmo que seja vazio).

Exemplo: `div:before { content: " "; }` e `div:after { content: " "; }`.

## before (antes)

Inclui um conteudo **antes** do conteudo principal do elemento

## after (depois)

Inclui um conteudo **depois** do conteudo principal do elemento

*O conteúdo inserido via css não é selecionavél pelo usuário e não é lido pelo browser*

Visto que seu conteudo não é selecionável e nem lido pelo browser. 
As peseudo-classe before e after devem ser usadas apenas para fins visuais.

## content

content por padrão é um elemento de linha. Mas pode ter seu display mudado via css.
