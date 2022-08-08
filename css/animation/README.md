# Animation

## RElemprando transition

- transition-property
- transition-duratiom
- transition delay
- transition-timing-function

Atalho: `transition: property duration timing-function delay`

*As transitions auxiliam as animações para torna-las mais suaves*.

É possivel fazer transições multiplas

```css
element {
transition: 
  property duration timing-function delay, 
  property duration timing-function delay;
}
```

### Transition VS Animations

Transition

- Apenas para transições simples (sem key frames)
- Depende da iteração do usuário (:hover, :focus... ou do javascript)

Animations

- Transições mais complexas (vários key frames)
- Não depende da iteração do usuário
- Maior controle sobre a animação criada

## Timeline

[timeline key frame animation css](https://css-tricks.com/wp-content/uploads/2015/01/keyframes1.jpg)

## Dicas

Apenas **valore númericos** podem ser animados (10px, .5, 50%, #333333, red).
Valores como auto, arial, hidden, block, entre outros, não são númericos.

Propriedades mais performáticas para animação são: transform e opacity.

## key frames

Exemplo de definição de key frames

```css
@keyframes animaCor {
  from {
    color: red;
  }
  to {
    color: blue;
  }
}

@keyframes animaCor {
  0% {
    color: red;
  }

  50% {
    color: orange;
  }

  100% {
    color: blue;
  }
}
```

### Aplicando key frames no elemento

Podemos aplicar kay frames nos elementos da seguinte maneira

```css
element {
  animation: animacor 1s;
  /* animation: keyframe-name duration */
}
```

## Outras propriedades animations

- animation-name (nome do key frame)
- animation-duration (duração)
- animation-deley (delay)
- animation-timming-function (easy, easy-in igual o transition)
- animation-iteration-count (quantas vezes será repetido)
- animation-direction (dofinal para o inicio ou do inicio para o final)
- animation-fill-mode (preserva as propriedades animadas no elemento ao final ou inicio da animação) 
- animation-play-state (dar play ou pausar a transição)

