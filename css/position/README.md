# Positions

- static
- relative
- absolute
- fixed
- sticky

Todos com exceção do static acompanham as propriedades left, right, bottom e top.

Essas servem para alterar o posicionamento do elemento na tela 

## static (default)

A ordem que o elementos aparecem na tela, é a mesma ordem do html

## relative

top e left... relativos a posição original

## Absolute

top e left... relativos a posição do primeiro elemento pai que tenha um position
diferente de static

(muda o fluxo do documento)

## Fixed

Não relaciona a ele nem a outro elemento, mas sim a janela do browser (muda o fluxo do documento)

### z-index

Por padrão possi o valor zero 

Ordena qual emento vai se sobrepor ao outro. Elemento que ficará encima e elemento que ficará embaixo
Z-index: 3 sempre ficará por cima de elementos que tenha z-index 2 ou menor