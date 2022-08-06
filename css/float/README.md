# Float

float faz com que o elemento saia do fluxo normal e fique flutuando,
os elementos ao redores "não enxergarão" mais esse elemento, ou seja é como se ele não existisse

```css
.block2 {
  background-color: antiquewhite;
  /* 
  float: left;
  float: right; 
  */
}
```

## clear

Faz com que o elemento não seja afetado pelo efeito colateral do float de elementos vizinhos

```css
.block3 {
  background-color: aquamarine;
  /* 
  clear: right;
  clear: left;
  clear: both; 
  */
}
```

- clear: right: Ignora o efeito colateral do float right dos elementos vizinhos
- clear: left: Ignora o efeito colateral do float left dos elementos vizinhos
- clear: both: Ignora o efeito colateral do float left e right dos elementos vizinhos