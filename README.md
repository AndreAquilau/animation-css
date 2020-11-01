## Documentação de Como Criar Animações com CSS.

#### * Keyframes
#### * Animation
#####   * [Animation-name]()
#####   * [Animation-duration]()
#####   * [Animation-timing-function]()
#####   * [Animation-delay]()
#####   * [Animation-interation-count]()
#####   * [Animation-direction]()
#####   * [Animation-fill-mode]()
#####   * [Animation-play-state]()
#####   * [Animation References]()


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
* Aceita valores em segundos com a letra "s" e milissegundos com a letra "ms".
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
    * Também podemos utilizar o steps pra trabalhar com quadros por segundos ou milissegundos.
    * steps(3) sera exibido 3 frames assim fica possivel criar cenas animadas com essa propriedade.
    * steps(3, jump-start) e steps(3, jump-end).


#### Animation-delay
* Especifica a quantidade de tempo de espera para animação iniciar.
* Aceita segundos e milissegundos.
~~~css
.element {
  animation-delay: 2s;
}
~~~


#### Animation-interation-count
* Define quantas vezes a animação vai ser executada.
~~~css
.element {
  animation-iteration-count: 3;
  animation-iteration-count: 3.5;
  animation-iteration-count: infinite;
}
~~~

#### Animation-direction
* Define a direção que a animação será executada.
~~~css
.element {
  animation-direction: reverse;
  animation-direction: alternate;
  animation-direction: alternate-reverse;
}
~~~
* Opções
    * reverse: a animação será executada do final para o inicio.
    * alternate: a animação será executada do inicio para o final e depois do final para o inicio.
    * alternate-reverse: a animação será iniciada do final para o inicio e depois alternando.


#### Animation-fill-mode
* Define quais valores serão aplicado ao elemento no inicio ou no final da animação.
* Podemos definir o ultimo estado do elemeto e o primeiro estado do elemento.
~~~css
.element {
  animation-fill-mode: forwords;
  animation-fill-mode: backwords;
  animation-fill-mode: both;
}
~~~
* Opções
    * forwords: a animação não retorna os valores de suas propriedades para o inicio ao finalizar sua execução.
    * backwords: a animação retorna para os valores iniciais do elemento.
    * both: é a união dos valores forwords com backwords.

#### Animation-play-state
* Define se a animação está sendo executada ou pausada.
~~~css
.element {
  animation-play-state: running;
  animation-play-state: paused;
}
~~~
* Opções
    * running: a animção executa normalmente.
    * paused: a animação será pausada.
#### Animation References
* [Easing functions](https://easings.net/)
* [cubic-bezier](https://cubic-bezier.com/)
* [Animista: scale-up, scale-down, rotate, rotate-scale, rotate-90, flip, slide, text, background...](https://animista.net/)
* [Animatable CSS properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties)
* [Princípios Jedi de Motion UI (parte 1): tipos de animação de interface](https://desenvolvimentoparaweb.com/ux/motion-ui-principios-tipos-animacao-interface/)
* [Jumps: o novo steps() em Web Animation
](https://desenvolvimentoparaweb.com/css/jumps-steps-css-web-animation/)
