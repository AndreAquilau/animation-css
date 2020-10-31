## Documentação de Como Criar Animações com CSS.

### KeyFrames

* Utilizamos para definimos pontos chaves em um intervalo do inicio ao final da animação.
* Podemos usar os keyframes de três formas.
~~~~css
@keyframes name {
  from {
    transform: rotate(10de);
  }
  to {
    transform: rotate(60de);
  }
}
~~~~
~~~~css
@keyframes name {
  to {
    transform: rotate(60de);
  }
}
~~~~
~~~~css
@keyframes name {
  0%  {
    transform: rotate(10de);
  }
  25% {
    transform: rotate(20de);
  }
  50% {
    transform: rotate(30de);
  }
  75% {
    transform: rotate(40de);
  }
  100% {
    transform: rotate(60de);
  }
}
~~~~

### Animation

#### Animation-name
* Especifica o nome dado na diretiva @kayframes que descrever a animação a ser aplicada ao elemento.
~~~css
.element {
  animation-name: test;
}
~~~
#### Animation-duration:
* Define um tempo que a animação devera ser executada.
* Aceita valores em segundos com a letra "s" e milessegundos com a letra "ms".
~~~css
.element {
  animation-duration: 1s;
}
~~~
