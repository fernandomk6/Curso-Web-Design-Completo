# Transform 2d

Transforma algum elemento

- translate
- rotate
- skew
- scale

## Translate

**É semelhante ao position relativo**.

Move um elemento baseado nas coordenadas X e Y.

A função CSS translate() **reposiciona** um elemento na direção horizontal e/ou vertical.
O seu resultado é um tipo de dado `<transform-function>`.
Esta transformação é caracterizada por um vetor bidimensional. 
Suas coordenadas definem o quanto o elemento se move em cada direção.

```css
/* Valores <length-percentage> únicos */
transform: translate(200px);
transform: translate(50%);

/* Valores <length-percentage> duplos */
transform: translate(100px, 200px);
transform: translate(100px, 50%);
transform: translate(30%, 200px);
transform: translate(30%, 50%);
```

```css
.moved {
  transform: translate(10px); /* Igual a: translateX(10px) ou translate(10px, 0) */
}
```

### Diferença entre translate e position relative

Uma das principais diferenças é que os valores passados em porcentagem,
são diferentes.

- Porcentagem no translate faz referencia ao width do **próprio elemento**.
- Porcentagem no position relative faz referencia ao width do **elemento pai**.

*Translate não cria um contexto para elementos com position absolute.*

## Rotate

A função CSS rotate() define uma transformação que **gira** um elemento em 
torno de um ponto fixo no plano 2D, sem deformá-lo.

A quantidade de rotação criada por rotate() é especificado por um grau. 
Se positivo, o movimento será no sentido horário; 
Se negativo, ela será no sentido anti-horário. 
Uma rotação de 180° é chamada de point reflection (reflexão do ponto).

```css
div {
  width: 80px;
  height: 80px;
  background-color: skyblue;
}

.rotated {
  transform: rotate(45deg); /* Equal to rotateZ(45deg) */
  background-color: pink;
}
```

### Transform origin

A posição padrão do eixo de rotação, é o centro.

Mas isso pode ser alterado usando as seguintes propriedades:

- `transform-origin: center;`
- `transform-origin: top;`
- `transform-origin: bottom;`
- `transform-origin: left;`
- `transform-origin: right;`
- `transform-origin: unit(x) unit(y);`

![transform-options](https://i7x7p5b7.stackpathcdn.com/codrops/wp-content/uploads/2014/12/transform-origin-examples.png)

## Transformações compostas

É possivel setar mais de uma transformação em um mesmo elemento, exemplo:

`transform: translate(50px) rotate(45deg)`;

## skew

A função CSS define uma transformação que **distorce** um elemento no plano 2D.
O efeito é como se você pegasse cada canto do elemento e os puxasse ao longo de 
um determinado ângulo.
A skew()função é especificada com um ou dois valores, que representam a quantidade 
de inclinação a ser aplicada em cada direção. Se você especificar apenas um valor, 
ele será usado para o eixo x e não haverá distorção no eixo y.

`skew(ax)` ou `skew(ax, ay)`

- ax
É uma `<angle>` representação do ângulo a ser usado para distorcer o elemento ao 
longo do eixo x (ou abcissa).

- ay
É uma `<angle>` representação do ângulo a ser usado para distorcer o elemento ao longo 
do eixo y (ou ordenada). Se não for definido, seu valor padrão é 0, resultando em uma 
inclinação puramente horizontal.

## scale

A função CSS scale() define uma transformação que **redimensiona** um elemento no plano 2D. 
Como o redimensionamento é definido por um vetor, ele pode transformar as dimensões
verticais e horizontais em escalas diferentes.

`scale(sx)` ou `scale(sx, sy)`

- sx

Um `<number>`representando a abscissa do vetor de redimensionamento.
- sy

Um `<number>`representando a ordenada do vetor de redimensionamento. 
Se não for definida, seu valor padrão ésx, resultando em um redimensionamento 
uniforme que preserva a proporção do elemento.