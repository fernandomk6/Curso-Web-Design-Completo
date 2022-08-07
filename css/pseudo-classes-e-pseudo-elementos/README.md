# Pseudo-classes e pseudo-elementos

## Pseudo-classes

Antecedidas de `:` (dois pontos)

Uma pseudo-classe CSS é uma palavra-chave adicionada a seletores que 
especifica um **estado especial** do elemento selecionado. Por exemplo, 
`:hover` pode ser usado para alterar a cor de um botão quando o usuário passar o cursor sobre ele.

Pseudo-classes permitem que você aplique um estilo a um elemento não apenas em 
relação ao conteúdo da árvore do documento, mas também em relação a fatores 
externos como o histórico de navegação (`:visited`, por exemplo), o status do 
seu conteúdo (como `:checked` em certos elementos de um formulário), ou a posição 
do mouse (como `:hover`, que permite saber se o mouse está sobre um elemento ou não).

### Índice de pseudo-classes comuns

- :active
- :checked
- :default
- :dir()
- :disabled
- :empty
- :enabled
- :first
- :first-child
- :first-of-type
- :fullscreen
- :focus
- :hover
- :indeterminate
- :in-range
- :invalid
- :lang()
- :last-child
- :last-of-type
- :left
- :link
- :not()
- :nth-child()
- :nth-last-child()
- :nth-last-of-type()
- :nth-of-type()
- :only-child
- :only-of-type
- :optional
- :out-of-range
- :read-only
- :read-write
- :required
- :right
- :root
- :scope
- :target
- :valid
- :visited

## Pseudo-elementos

Antecedidos de `::` (dois sinais de dois pontos)

Um pseudo-elemento CSS é uma palavra-chave adicionada a um seletor que 
permite que você estilize uma **parte específica** do elemento selecionado. 
Por exemplo, o pseudo-elemento `::first-line` aplica o estilo apenas na primeira 
linha de um parágrafo.

```css
seletor::pseudo-elemento {
  propriedade: valor;
}
```

### Índice de pseudo-elementos comuns

- ::after
- ::before
- ::cue
- ::first-letter
- ::first-line
- ::selection
- ::slotted
- ::backdrop
- ::placeholder
- ::marker
- ::spelling-error
- ::grammar-error