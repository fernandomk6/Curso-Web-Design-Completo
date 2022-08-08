# Display grid

- Flexbox: unididmensional (uma unica direção column ou row)
- Display grid: Bidimensional (linhas e colunas)

## Introdução

No display grid, sempre tratamos eixos X e Y.

- Grid line: Separa as grid cells. Pode ser horizontal ou vertical.
![Display Grid](https://webkit.org/wp-content/uploads/grid-concepts.svg)

## Grid container

É o container que terá o display grid. Todos os seus filhos serão grid itens.

## Grid-template

```css
.gridContainer {
  display: grid;
  /* define que esse elemento será um grid */

  grid-template-columns: 100px 100px 100px;
  /* Define que o container terá 3 colunas cada uma com o width de 100px */

  grid-template-rows: 200px 200px;
  /* Define que esse container terá 2 linhas cada uma com 200px de height*/
}
```

O exemplo acima pode ser reescrito usando a função repeat quando tiver valores repetidos

```css
.gridContainer {
  display: grid;
  /* define que esse elemento será um grid */

  grid-template-columns: repeat(3, 100px);
  /* Define que o container terá 3 colunas cada uma com o width de 100px */

  grid-template-rows: repeat(2, 200px);
  /* Define que esse container terá 2 linhas cada uma com 200px de height*/
}
```

## gap

`grid-row-gap` e `grid-column-gap` são propriedades que irão colocar um 
espaçamento entre as linhas ou colunas.

```css
.gridContainer {
  display: grid;
  /* define que esse elemento será um grid */

  grid-template-columns: repeat(3, 100px);
  /* Define que o container terá 3 colunas cada uma com o width de 100px */
  grid-template-rows: repeat(2, 200px);
  /* Define que esse container terá 2 linhas cada uma com 200px de height*/

  grid-row-gap: 10px; 
  /* Espaçamento entre linhas */
  grid-column-gap: 10px; 
  /* Espaçamento entre colunas */
  }
```

Também é possivel usar o atalho `grid-gap: 10px  20px;` para setar o gap de linhas e colunas juntas.

## unidade de medida fr

1fr é uma fração, ou todo o espaço que excede, que falta.
Faz com que o bloco ocupe todo o espaço disponivel proporcionalmente.
2fr irá ocupar o dobro do espaço que 1fr. Pode ser lido 2 partes do que falta, e 1 parte
do que falta, onde 3fr é todo o espaço disponivel.

## Grid item

### Ordenando as posições

Podemos definir em qual linha da coluna ou da linha, o grid item vai iniciar e terminar.

```css
.gridItem {
  grid-row-start: 1;
  grid-row-start: 2;
  /* Atalho -> grid-row: 1 / 2; */
  /* Atalho -> grid-row: 1 / span 2; */

  grid-column-start: 3;
  grid-column-start: 4;
  /* Atalho -> grid-column: 3 / 4; */
  /* Atalho -> grid-column: 3 / span 2; */

  /* span 1 = o espaço de 1 celula. span 2 = ocupar o espaço de 2 celulas */
}
```

**Pode ser usado também para "mesclar celulas"**

- Observações

`grid-row-start: -1;` o -1 é a ultima linha. usado quando queremos que uma celula vá até,
a ultiama linha, independentemente do número de linhas.

## Grid template areas

`grid-template-areas` serve para definir em forma de texto a estrutura das celulas.

```css
/* define a estrutura do grid */
.grid-container {
  grid-template-areas : 
    "header header header"
    "nav    nav    aside"
    "main   main   aside"
    "footer footer footer"
}

/* nomeia cada elemento de acordo com o que foi passado para o grid template areas */
.header {
  grid-area: header;
}
.nav {
  grid-area: nav;
}
.aside {
  grid-area: aside;
}
.main {
  grid-area: main;
}
.footer {
  grid-area: footer;
}
```

- Obeservações

```css
.grid-container {
  grid-template-areas : 
    ".      .      header"
    "nav    nav    aside"
    "main   main   aside"
    "footer footer footer"
}

/* o "." indica que é uma celula vazia */

```
