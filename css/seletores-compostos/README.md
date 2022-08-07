# Seletores compostos

Os Seletores definem quais elementos um conjunto de regras CSS se aplica.

---

## Seletores básicos

### Por tag

Sintaxe: `nome-da-tag { ... }`

### Por classe

Sintaxe: `.nome-da-classe { ... }`

### Por ID

Sintaxe: `#nome-do-id { ... }`

### Universal

Sintaxe: `* { ... }`

### Por atributo
Sintaxe: 
`[atrib] [atrib=valor] [atrib~=valor] [atrib|=valor] [atrib^=valor] [atrib$=valor] [atrib*=valor] { ... }`

#### Observações

- `[attr~=value]	p[class~="special"]`	

Corresponde a elementos com um atributo attr cujo valor é exatamente value, 
ou contém valor em sua lista de valores **separados por espaço**.

- `[attr|=value]	div[lang|="zh"]`

Corresponde a elementos com um atributo attr cujo valor é exatamente value ou 
começa com value imediatamente seguido por um **hífen**.

- `[attr]	a[title]`	

Corresponde a elementos com um **atributo** attr cujo nome é o valor entre colchetes.

- `[attr=value]	a[href="https://example.com"]`

Corresponde a elementos com um atributo attr cujo valor é **exatamente** 
value - a string entre aspas.

- `[attr^=value]	li[class^="box-"]`	
Corresponde a elementos com um atributo attr (cujo nome é o valor entre colchetes), 
cujo valor começa com valor.

- `[attr$=value] li[class$="-box"]`

Corresponde a elementos com um atributo attr cujo valor termina com valor.

- `[attr*=value]	li[class*="box"]`

Corresponde a elementos com um atributo attr cujo valor contém o valor 
em qualquer lugar dentro da string.

### :not(*seletor*)

A pseudo-classe CSS de negação, `:not(X)`, é uma notação funcional que recebe 
um seletor simples X como argumento. Ela seleciona um elemento que **não** é 
representado por seu argumento. X não pode conter outro seletor de negação.

`:not(selector) { style properties }`

```css
p:not(.classico) { color: red; }
body *:not(p) { color: green; }
```

---

## Combinadores

### Seletores de irmãos adjacentes (posto ao lado de) (`+`)

O combinador + seleciona os nós que seguem **imediatamente** o elemento especificado anteriormente.
Sintaxe: `A + B`.
Exemplo: ul + li irá corresponder a qualquer elemento `<li>` que segue imediatamente após um elemento `<ul>`.

### Seletor de proxímos irmãos (`~`)

O combinador ~ seleciona os nós que seguem (não necessariamente imediatamente) o elemento 
especificado anteriormente, se ambos os elementos compartilham o mesmo pai.
*Seleciona TODOS os irmãos seguintes, não os anteriores*
Sintaxe: `A ~ B`.
Exemplo: p ~ span irá corresponder a todo elemento `<span>` que seguir um elemento `<p>` 
dentro de um mesmo elemento pai.

### Seletor de filhos diretos (`>`)

O combinador > selecina nós que são **filhos diretos** do elemento especificado anteriormente.
Sintaxe: `A > B`
Exemplo: ul > li irá corresponder a todo elemento `<li>` que estiver diretamente dentro 
de um elemento `<ul>` especificado.

### Seletor de descendentes (` `)

O combinador seleciona os nós que são **decendentes** do elemento especificado anteriormente 
(não é necessário que seja um filho direto).
Sintaxe: `A B`
Exemplo: div span irá corresponder a todo e qualquer elemento `<span>` que estiver 
dentro do elemento `<div>`.
