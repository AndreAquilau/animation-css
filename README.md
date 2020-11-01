## Documentação de Como Criar Animações com CSS.

* ### Animation
    * [Animation-name](https://github.com/AndreAquilau/animation-css#animation-name)
    * [Animation-duration](https://github.com/AndreAquilau/animation-css#animation-duration)
    * [Animation-timing-function](https://github.com/AndreAquilau/animation-css#animation-timing-function)
    * [Animation-delay](https://github.com/AndreAquilau/animation-css#animation-delay)
    * [Animation-interation-count](https://github.com/AndreAquilau/animation-css#animation-interation-count)
    * [Animation-direction](https://github.com/AndreAquilau/animation-css#animation-direction)
    * [Animation-fill-mode](https://github.com/AndreAquilau/animation-css#animation-fill-mode)
    * [Animation-play-state](https://github.com/AndreAquilau/animation-css#animation-play-state)
    * [Animation References](https://github.com/AndreAquilau/animation-css#animation-references)
* ### Transform
    > [Roate](https://github.com/AndreAquilau/animation-css#rotate)</span>,
    > [RotateZ](https://github.com/AndreAquilau/animation-css#rotatez),
    > [RotateX](https://github.com/AndreAquilau/animation-css#rotatex),
    > [RotateY](https://github.com/AndreAquilau/animation-css#rotatey),
    > [Rotate3D](https://github.com/AndreAquilau/animation-css#rotate3d).
    --------------------------------------------------------------------
    > [Skew](https://github.com/AndreAquilau/animation-css#skew),
    > [SkewX](https://github.com/AndreAquilau/animation-css#skewx),
    > [SkewY](https://github.com/AndreAquilau/animation-css#skewy).
    --------------------------------------------------------------------
    > [Scale](https://github.com/AndreAquilau/animation-css#scale),
    > [ScaleX](https://github.com/AndreAquilau/animation-css#scalex),
    > [ScaleY](https://github.com/AndreAquilau/animation-css#scaley),
    > [ScaleZ](https://github.com/AndreAquilau/animation-css#scalez),
    > [Scale3d](https://github.com/AndreAquilau/animation-css#scale3d).
    --------------------------------------------------------------------
    > [Translate](https://github.com/AndreAquilau/animation-css#translate),
    > [TranslateX](https://github.com/AndreAquilau/animation-css#translatex),
    > [TranslateY](https://github.com/AndreAquilau/animation-css#translatey),
    > [TranslateZ](https://github.com/AndreAquilau/animation-css#translatez).


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
~~~css
.element {
  animation: name duration delay fill-mode timing-function interation-count direction;
}
~~~
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


### Transform
* A propriedade transform e uma propriedade de transformação do elemento e pode aceita mais de um valor.
#### Rotate
* Rotação no eixo Z no sentido horário e anti-horário.
* Aceita valores em deg = grau ou turn = volta.
* deg >= 0 ou deg <= 0.
* turn >= 0 ou turn < 0.
* 360deg === 1turn.
~~~css
.element {
  transform: rotate(360deg) rotate(0.5turn);
}
~~~

#### RotateZ
* Rotação no eixo Z no sentido horário e anti-horário.
* Aceita valores em deg = grau ou turn = volta.
* deg >= 0 ou deg <= 0.
* turn >= 0 ou turn < 0.
* 360deg === 1turn.
~~~css
.element {
  transform: rotateZ(360deg) rotateZ(0.5turn);
}
~~~


#### RotateX
* Rotação no eixo X no sentido horário e anti-horário.
* Aceita valores em deg = grau ou turn = volta.
* deg >= 0 ou deg <= 0.
* turn >= 0 ou turn < 0.
* 360deg === 1turn.
~~~css
.element {
  transform: rotateX(360deg) rotateX(0.5turn);
}
~~~

#### RotateY
* Rotação no eixo Y no sentido horário e anti-horário.
* Aceita valores em deg = grau ou turn = volta.
* deg >= 0 ou deg <= 0.
* turn >= 0 ou turn < 0.
* 360deg === 1turn.
~~~css
.element {
  transform: rotateY(360deg) rotateY(0.5turn);
}
~~~


#### Rotate3d
* Rotação nos três eixos X, Y, Z no sentido horário e anti-horário.
* recebe 4 parâmetros.
* os três primeiros parâmetros são referentes ao eixo x, y, z e recebi apenas dois valores "1" haverá rotação, "0" não haverá rotação.
* o quarto parâmetro é referente a rotção do elemento.
~~~css
.element {
  transform: rotate3d(x = 0 || 1, y = 0 || 1, z = 0 || 1, deg || turn)
}
~~~


#### Skew
* Skew é uma propriedade de inclinação do elemento no eixo x e y.
* Aceita os seguintes valores em deg ou turn.
~~~css
.element {
  transform: skew(1turn || 360deg);
}
~~~

#### SkewX
* SkewX é uma propriedade de inclinação do elemento no eixo x.
* Aceita os seguintes valores em deg ou turn.
~~~css
.element {
  transform: skewX(1turn || 360deg);
}
~~~

#### SkewY
* SkewX é uma propriedade de inclinação do elemento no eixo Y.
* Aceita os seguintes valores em deg ou turn.
~~~css
.element {
  transform: skewY(1turn || 360deg);
}
~~~

#### Scale
* Scale é uma propriedade referente ao tamanho do elemento tando em uma visão 2D ou 3D.
* Aceita valores numéricos onde 1 e a mante todas as dimenções do elemento tanto altura, largura e profundidade.
~~~css
.element {
  transform: scale(2);
}
~~~

#### ScaleX
* ScaleX é uma propriedade referente a lagura do elemento tando em uma visão 2D ou 3D.
* Aceita valores numéricos onde 1 e a mante todas as dimenções do elemento tanto altura, largura e profundidade.
~~~css
.element {
  transform: scaleX(2);
}
~~~

#### ScaleY
* ScaleY é uma propriedade referente a altura do elemento tando em uma visão 2D ou 3D.
* Aceita valores numéricos onde 1 e a mante todas as dimenções do elemento tanto altura, largura e profundidade.
~~~css
.element {
  transform: scaleY(2);
}
~~~

#### ScaleZ
* ScaleZ é uma propriedade referente a profundidade do elemento tando em uma visão 2D ou 3D.
* Aceita valores numéricos onde 1 e a mante todas as dimenções do elemento tanto altura, largura e profundidade.
~~~css
.element {
  transform: scaleZ(2);
}
~~~

#### Scale3d
* Scale3d é uma propriedade referente a altura, largura, profundidade do elemento tando em uma visão 2D ou 3D.
* Aceita valores numéricos onde 1 e a mante todas as dimenções do elemento tanto altura, largura e profundidade.
* Recebi 3 parâmetros scale(eixoX: number, eixoY: number, eixoZ: number)
~~~css
.element {
  transform: scale3d(2, 2, 2);
}
~~~

#### Translate
* A propriedade translate e referente a movimentação do elemento no eixo X, Y e Z.
* Aceita valores em px, vw, vh e %.
* Aceita valores positivos e negativos.
~~~css
.element {
  transform: translate(10px) /*eixo X e Y*/;
}
~~~

#### TranslateX
* A propriedade translate e referente a movimentação do elemento no eixo X.
* Aceita valores em px, vw, vh e %.
* Se movimenta para a esquerda ou  a direita.
~~~css
.element {
  transform: translateX(10px) /*eixo X*/;
}
~~~

#### TranslateY
* A propriedade translate e referente a movimentação do elemento no eixo Y.
* Aceita valores em px, vw, vh e %.
* Se movimenta para cima ou para baixo.
~~~css
.element {
  transform: translateY(10px) /*eixo Y*/;
}
~~~

#### TranslateZ
* A propriedade translate e referente a movimentação do elemento no eixo Z.
* Se movimenta para frente ou para tras.
* Aceita valores em px, vw, vh e %.
~~~css
.element {
  transform: translateZ(10px) /*eixo Z*/;
}
~~~

### Background-Animation
#### linear-gradient
* O linear gradient é um propriedade de fundo onde definimos cores a serem mostradas
* O primeiro parâmetro é o ângulo que as cores irá se iniciar.
~~~css
body {
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab) no-repeat;
            background-size: 300% 300%;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 300vh;
            animation: gradient 10s cubic-bezier(.17,.67,.83,.67) infinite alternate;
        }

        @keyframes gradient {
            0%{
                background-position: 0% 50%;
            }
            50%{
                background-position: 100% 50%;
            }
            100%{
                background-position: 0% 50%;
            }
        }
~~~
#### radial-gradient
* O linear gradient radial é um propriedade de fundo onde definimos cores a serem mostradas
* Recebi como parâmetro apenas cores, as cores começa a ser mostrada do centro para as bordas.
~~~css
 body {
            background: radial-gradient(#ee7752, #e73c7e, #23a6d5, #23d5ab) no-repeat;
            background-size: 300% 300%;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 300vh;
            animation: gradient 10s cubic-bezier(.17,.67,.83,.67) infinite alternate;
        }

        @keyframes gradient {
            0%{
                background-position: 0% 50%;
            }
            50%{
                background-position: 100% 50%;
            }
            100%{
                background-position: 0% 50%;
            }
        }
~~~

