# CSS - Cascating Style Sheets

## Sintaxe

```css
seletor {
  propriedade: valor
}
```

Seletor é a regra CSS e tudo o que está dentro de chaves `{  }` é onde ficam
as declarações das regras.

### Exemplo

```css
h1 {
  color: red;
  font-size: 16px;
}
```

- h1: É o seletor
- color: É uma proriedade desse seletor
- red: É o valor que a propriedade color irá ter

O que ele faz? muda a cor do texto que está dentro da tag `<h1>` para vermelho.

## Formas de colocar CSS na página

- Inline: `<p style="...">` as regras CSS são declaradas dentro da TAG. **Não use assim pois dificulda a manutenção**
- Interno: `<style>...</style>` as regras CSS são declaradas dentro da tag `<style>` que fica dentro da 
tag `<head>`. *Também não utilize dessa forma pois também dificulda a manutenção*
- Externo: É criado um arquivo .css e nele é colocado todas as regras CSS. E então esse arquivo é linkado
ao HTML por meio da tag `<link hred="styles.css" rel="stylesheet">`. Assim todas as páginas que tiverem
esse link, passarão a usar as regras css declaradas nesse arquivo. 
**Prefira sempre usar a forma externa pois facilita a manutenção**

## Formas de selecionar elementos HTML com CSS

- tag: Não recomendado pois irá estilizar todas aquelas tags
- class: Recomendato pois, você pode escolher quais elementos terão a classe desejada
- id: **cuidado** apenas é permitido 1 id por página. Pois id é uma identificação. É possivel estilizar
via id, porém será um elemento único.

### O HTML

```html
<h1 class="my-class" id="my-id">Meu título</h1>
```
### Os seletores CSS

- tag: `h1 { color: red }`
- class: `.my-class { color: red }`
- id: `#my-id { color: red }`

