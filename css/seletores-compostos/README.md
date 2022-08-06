# Seletores compostos

Os Seletores definem quais elementos um conjunto de regras CSS se aplica.

## Seletores básicos

### Por tag

Sintaxe: `nome-da-tag { ... }`

### Por classe

Sintaxe: `.nome-da-classe { ... }`

### Por ID

Sintaxe: `#nome-do-id { ... }`

### Universais

Sintaxe: `* { ... }`

### Atributos

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

Corresponde a elementos com um atributo attr cujo valor é **exatamente** value - a string entre aspas.

## Combinadores

### Seletores de irmãos adjacentes (posto ao lado de)

O combinador + seleciona os nós que seguem imediatamente o elemento especificado anteriormente.
Sintaxe: `A + B`.
Exemplo: ul + li irá corresponder a qualquer elemento `<li>` que segue imediatamente após um elemento `<ul>`.

### Seletores gerais de irmãos

O combinador ~ seleciona os nós que seguem (não necessariamente imediatamente) o elemento 
especificado anteriormente, se ambos os elementos compartilham o mesmo pai.
Sintaxe: `A ~ B`.
Exemplo: p ~ span irá corresponder a todo elemento `<span>` que seguir um elemento `<p>` 
dentro de um mesmo elemento pai.

### Seletor de filhos

O combinador > selecina nós que são filhos diretos do elemento especificado anteriormente.
Sintaxe: `A > B`
Exemplo: ul > li irá corresponder a todo elemento `<li>` que estiver diretamente dentro 
de um elemento `<ul>` especificado.

### Seletor de descendentes

O combinador seleciona os nós que são filhos do elemento especificado anteriormente 
(não é necessário que seja um filho direto).
Sintaxe: `A B`
Exemplo: div span irá corresponder a todo e qualquer elemento `<span>` que estiver 
dentro do elemento `<div>`.
