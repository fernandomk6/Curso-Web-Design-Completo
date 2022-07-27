# Imagens

## Formas de trabalhar com imagens

- HTML: `<img src="./my-image.jpg" alt="Texto alternativo caso a imagem não seja carregada">`
- CSS: `seletor { background-image: url(./my-image.jpg); }`

### Quando usar no HTML

Use imagem no HTML quando a imagem tiver relação **direta** com o conteudo.

### Quando usar no CSS

- Use imagem no CSS quando a imagem for apenas, decorativa.

### Dica

Verifique se a imagem a ser inserida, pode possuir um atributo alt, se sim
é um indicio que ela deve ser colocada no HTML. Se não, é um indicio que ela
deva ser colocada no CSS.

## Tipos de imagens

- .jpg / jpeg
- .png *Geralmente usado quando precisa de transparencia*
- .gif *Imagens animadas*
- .svg *Não perde qualidade quando o usuario dar zoom e é bastante leve*

Formatos bitmap (.jpeg, .png dentre outros) são formados por pixels.
Já os .svg não são bitmap, ou seja, não é formado por pixel. Por isso não
perde qualidade ao dar zoom.