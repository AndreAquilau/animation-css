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
#### Animation-duration
* Define um tempo que a animação devera ser executada.
* Aceita valores em segundos com a letra "s" e milessegundos com a letra "ms".
~~~css
.element {
  animation-duration: 1s;
}
~~~
#### Animation-timing-function
* Essa propriedade define como uma animação irá progredir ao longo da sua duração.
* É uma função de tempo aplicada na animação.
~~~css
.element {
  animation-timing-function: linear;
}
~~~
* Opções Pré-definidas.
    * ease-in: suave no inicio da animação.
    * ease-out: suave no final da animação.
    * ease-in-out: suave ao iniciar a animação e no final da animação.
    * linear: tempo uniforme sem alterar o progresso da animação.
* Opções Personalizadas com cubic-bezier:
    * É possivel criar funções de tempo personalizadas com a função cubic-bezier().
    * alguns sites já fornece alguns valores com base nos parâmetros solicitados.
    * cubic-bezier é um diferencial na animação.
* Steps().
    * Também podemos utilizar o steps pra trabalhar com quadros por segundos ou mílessegundos.
    * steps(3) sera exibido 3 frames assim fica possivel criar cenas animadas com essa propriedade.
    * steps(3, jump-start) e steps(3, jump-end).
