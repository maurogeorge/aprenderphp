---
layout: post
title: O loop for, as  estruturas de controle aninhadas, o break e o continue no PHP
meta_description: Neste artigo entenda o funcionamento do looping for. Saiba o que significa, e como fazer, o aninhamento de estruturas no PHP, alem dos comandos break e continue.
meta_keywords: PHP, looping, for, while, do-while, switch, estruturas de controle, aninhamento, aninhar, aninhada, break, continue
summary: Neste artigo entenda o funcionamento do looping for. Saiba o que significa, e como fazer, o aninhamento de estruturas no PHP, alem dos comandos break e continue.
tags: [Tipos de dados, Operador de incremento, Operador de decremento, Algoritmo, Estruturas de controle]
---
<h2>Introdução</h2>
<p>No artigo anterior  aprendemos como utilizar os <a href="/artigo/lacos-de-repeticao-while-e-do-while-no-php">laços de repetição while e do while  no PHP</a> para realizarmos rotinas  que deviam ser executadas um certo numero de vezes. Porém existe uma  possibilidade de facilitar o uso de contadores finitos, sem utilizarmos o uso  do <code>while</code> e do <code>do while</code>. E está possibilidade é o que veremos agora com a  estrutura de controle <code>for</code>.</p>
<h2>Problema</h2>
<p>Vamos continuar com  o mesmo problema do <a href="/artigo/lacos-de-repeticao-while-e-do-while-no-php">artigo anterior sobre while e do while</a> para quem não se lembra do problema: Bart  Simpson ficou novamente na detenção no final da aula. E como punição terá que  escrever: “Estou aprendendo loopings no Aprender PHP” 100 vezes no quadro, ou  no nosso caso na tela.</p>
Sabemos que com o <code>while</code> e o <code>do while</code> podemos  resolver este problema facilmente, no entanto agora vamos ver uma abordagem  diferente com o uso do looping <code>for</code>.
<h2>O looping for no PHP</h2>
<p>Assim como o <code>while</code>  e o <code>do-while</code> o <code>for</code> é uma estrutura de controle responsável pela realização de  loopings no PHP.</p>
<p>O comando for  aceita 3 expressões na sua declaração sendo elas:</p>
<ol>
    <li>Expressão  que é avaliada apenas <strong>uma vez</strong> na  primeira iteração, volta, do looping. Geralmente a utilizamos para iniciar a  nossa variável de controle, contador, como por exemplo <code>$i = 1</code>.</li>
    <li>Expressão  que é avaliada <strong>no inicio</strong> de cada  iteração do looping, e caso retorne falso, o looping for será encerrado. A  segunda expressão como você pode ver pode ser considerada a condicional do  nosso looping, assim como tínhamos no <code>while</code> e no <code>do while</code>. Um exemplo seria <code>$i  &lt;= 100</code>.</li>
    <li>Expressão  que é avaliada <strong>no final</strong> de cada  iteração do looping, normalmente utilizada para alterar o valor da variável de  controle. Como por exemplo utilizar o operador de incremento <code>$i++</code>.</li>
</ol>
<h3>Diagrama de bloco</h3>
<p>Observe como seria  a representação do problema de Bart Simpson utilizando o <code>for</code>.</p>
<p class="center">
    <img src="/img/artigos/o-loop-for-as-estruturas-de-controle-aninhadas-o-break-e-o-continue-no-php/looping-for-no-php-representacao-em-diagrama-de-blocos.jpg" alt="Looping for no php representação em diagrama de blocos" />
</p>
<p>Iniciamos  com o <a href="/artigo/o-algoritmo-o-diagrama-de-blocos-e-o-php">bloco de processamento de dados</a> que já é conhecido nosso para criarmos a  mensagem que vai ser exibida e atribuímos o valor a variável <code>$mensagem</code>. Em  seguida para representarmos o loop utilizamos o símbolo denominado <strong>Processamento predefinido ou Preparação</strong> com os valores da expressão do for o inicio, meio e fim, que foram apresentados  a você no tópico anterior. Também utilizamos as setas para indicar o  processamento e as letras S e N em que S representa o caminho a ser seguido caso a condição seja verdadeira e N caso a condição seja falsa.</p>
<h3>No PHP</h3>
<p>Agora vejamos como seria a representação em PHP  da nossa estrutura de controle for para resolvermos o problema de Bart Simpson.</p>
<pre class="brush: php;">
&lt;?php
$mensagem = 'Estou aprendendo loopings no Aprender PHP';

for( $i = 1; $i &lt;= 100; $i++ ){

  echo $i . ' - ' .$mensagem . '&lt;br /&gt;' . PHP_EOL ;

}

?&gt;
</pre>
<p>Como  você pode observar diferentemente do <a href="/artigo/lacos-de-repeticao-while-e-do-while-no-php">while e do do-while</a> não necessitamos incrementar o contador dentro  do nosso looping pois isto já fica implícito na própria declaração do <code>for</code>. E  detalhe que o separador de instruções, expressões, no <code>for</code> é o ;(ponto e  virgula).</p>
<div class="dica">
    <p>Em relação à estrutura de controle for:</p>
    <ul>
        <li>Declara-se 3 expressões no inicio do for
            <ul>
                <li>Sendo a 1ª expressão avaliada apenas <strong>uma vez</strong>. Normalmente utilizada para  criação da variável de controle.</li>
                <li>2ª expressão é avaliada no inicio de cada  iteração, caso esta expressão retorne falso o looping é encerrado. Podendo ser  considerada a condicional do for.</li>
                <li>3ª Expressão é avaliada no final de cada  iteração, normalmente utilizada para alterar o valor da variável de controle.</li>
            </ul>
        </li>
        <li>Separa-se as expressões utilizando o ;(ponto e virgula).</li>
        <li>O looping é executado enquanto a condição da 2ª  expressão for verdadeira (True)</li>
        <li>Quando  a condição da 2ª expressão for avaliada como falsa (False) o processamento da  rotina é desviado para fora do looping</li>
        <li>O bloco de código referente ao looping deve ser  delimitado por chaves {}</li>
        <li>Endente o código referente ao bloco em 4 espaços  por questões de legibilidade, a como configurar o seu editor de texto para  transformar Tabs em espaços</li>
        <li>Utilizamos um contador para o looping não ficar  um looping infinito, este declarado na 1ª expressão</li>
    <li>Não se esqueça de alterar o valor do contador,  na 3ª expressão, para não cairmos em um looping infinito.</li>
    </ul>
</div>
<h2>Estruturas de controle aninhadas</h2>
<p>Antes de  continuarmos com as estruturas de controle <code>break</code> e <code>continue</code> devemos saber um  conceito importante as estruturas de controle aninhadas.</p>
<p>Também conhecido como desvio condicional  encadeado, as estruturas de controle aninhadas são utilizadas em casos em que é  necessário estabelecer verificações de condições sucessivas, ou seja, condições  dentro de condições.  Este tipo de  estrutura pode possuir diversos níveis de condições aninhadas. Vamos a um  exemplo.</p>
<h3>Problema</h3>
<p>Como acabamos de  aprender o looping <code>for</code> utilizaremos ele neste exemplo. Nosso problema é o seguinte:</p>
<ul>
    <li>criar  um programa que escreve de 1 a 100</li>
    <li>imprimir  todos os números</li>
    <li>ao lado  de todos os número mostrar se o número é par ou impar</li>
</ul>
<h3>Diagrama de bloco</h3>
<p>Observe como seria no diagrama de blocos a resolução do  nosso problema.</p>
<p class="center">
    <img src="/img/artigos/o-loop-for-as-estruturas-de-controle-aninhadas-o-break-e-o-continue-no-php/diagrama-de-blocos-de-estruturas-aninhadas-no-php.jpg" alt="Diagrama de blocos de estruturas aninhadas no php" />
</p>
<p>Como  você deve ter observado não possuímos nenhum símbolo novo no nosso <a href="/artigo/o-algoritmo-o-diagrama-de-blocos-e-o-php">diagrama de blocos</a>.  Iniciamos a resolução do nosso problema com o símbolo denominado <strong>Processamento predefinido ou Preparação</strong> para representarmos o looping <code>for</code>, onde inserimos a sua lógica. Caso o for  retorne falso o processamento é encerrado e nada é exibido. Caso retorne  verdadeiro iniciamos o looping e nos deparamos com uma estrutura aninha que é  representada por um <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">símbolo de  decisão, o losango</a>. No símbolo de decisão a lógica é avaliada, caso o valor  retornado seja verdadeiro exibe o número e diz que é par, caso retorne falso o  número é exibido e diz-se que é impar. Após exibirmos o valor utilizamos o <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">pequeno  circulo, o conector</a>, que foi utilizado para conectar as condições e todas  levarem para um mesmo destino, o inicio do looping for.</p>
<h3>No PHP</h3>
<p>Agora vamos ver no  PHP como ficaria no PHP a representação do diagrama de blocos anterior.</p>
<pre class="brush: php;">
&lt;?php

for( $i = 1; $i &lt;= 100; $i++ ){

  if ( $i % 2 == 0 ){
    echo $i . ' é par ' . '&lt;br /&gt;' . PHP_EOL;
  } else {
    echo $i . ' é impar ' . '&lt;br /&gt;' . PHP_EOL;
  }

}

?&gt;
</pre>
<p>Inicialmente o  mesmo looping <code>for</code> que aprendemos, no entanto observe que dentro do looping  surgiu uma <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">condicional if</a> que é a nossa estrutura de controle  aninhada, pois se encontra dentro do looping <code>for</code>.</p>
<p>A nossa lógica do <code>if</code> é: se <code>$i</code> módulo de 2 for  igual a zero retorna verdadeiro caso contrário falso. Ou seja se dividir <code>$i</code> por  2 e não houver resto significa que <code>$i</code> é par se não é impar.</p>
<div class="destaque">
    <p>Caso esteja em  dúvida com a <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">estrutura de controle if</a> ou o com o <a href="/artigo/operadores-no-php">operador  de módulo</a> acesse seus  respectivos artigos.</p>
    <ul>
        <li><a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">If, else e elseif as estruturas de controle  no PHP</a></li>
        <li><a href="/artigo/operadores-no-php">Operadores no PHP</a></li>
    </ul>
</div>
<h4>No PHP aninhando um pouco mais</h4>
<p>Agora que já temos  o conceito de estruturas de controle aninhadas mostrarei mais um exemplo  prático no PHP, com mais de um nível de aninhamento.</p>
<div class="observacao">
  <p>Mostrarei  direto no PHP, no entanto ele também pode ser representado no diagrama de  blocos, não o representarei no diagrama de blocos, pois o conceito no diagrama  de blocos foi explicado no exemplo anterior.</p>
</div>
<h5>Problema</h5>
<ul>
    <li>Definir  um número premiado entre 1 e 100</li>
    <li>criar  um programa que escreve de 1 a 100</li>
    <li>imprimir  todos os números</li>
    <li>Se o  número for o premiado mostrar ele com um destaque e escrever que é o premiado</li>
    <li>ao lado  de todos os número mostar se o número é par ou impar, exceto do número premiado</li>
</ul>
<p>Veja como  poderíamos resolver este problema no PHP:</p>
<pre class="brush: php;">
&lt;?php

$premiado = 77;

for( $i = 1; $i &lt;= 100; $i++ ){

  if( $i == $premiado ){

    echo '&lt;strong&gt;' .  $i . ' é o número premiado ' . '&lt;/strong&gt;&lt;br /&gt;' . PHP_EOL;

  } else {

      if ( $i % 2 == 0 ){
        echo $i . ' é par ' . '&lt;br /&gt;' . PHP_EOL;
      } else {
        echo $i . ' é impar ' . '&lt;br /&gt;' . PHP_EOL;
      }

  }

}

?&gt;
</pre>
<p>Como você deve ter  observado o programa é bem parecido com o anterior a diferença é que agora  criei uma variável com o nome de $premiado que armazenará o número premiado.<br />E dentro do looping for antes de verificar se é par ou impar, verifico primeiro  se o número é o premiado, se for o exibo e escrevo que ele é premiado dentro de  uma tag strong se não faço a mesma verificação anterior para ver se ele é par  ou impar. Sendo assim a verificação de par ou impar foi aninhada por uma  verificação para ver se é o número premiado ou não.</p>
<p>Se observar bem temos uma falha. Nada nos diz  que o número premiado deve estar entre 1 e 100 sendo assim se a pessoa colocar  um número maior que 100 não teremos nenhum premiado veja só um exemplo.</p>
<pre class="brush: php;">
&lt;?php

$premiado = 700;

for( $i = 1; $i &lt;= 100; $i++ ){

  if( $i == $premiado ){

    echo '&lt;strong&gt;' .  $i . ' é o número premiado ' . '&lt;/strong&gt;&lt;br /&gt;' . PHP_EOL;

  } else {

      if ( $i % 2 == 0 ){
        echo $i . ' é par ' . '&lt;br /&gt;' . PHP_EOL;
      } else {
        echo $i . ' é impar ' . '&lt;br /&gt;' . PHP_EOL;
      }

  }

}

?&gt;
</pre>
<p>Mais em nosso jogo  por política da casa sempre teremos um vencedor. Sendo assim temos que limitar a  escolha dos números entre 1 e 100. Abaixo como limitar a escolha entre 1 e 100  mais antes de olhar o código pare um pouco aqui e tente resolver por si só.</p>
<pre class="brush: php;">
&lt;?php

$premiado = 77;

if( $premiado &lt; 100 ){

    for( $i = 1; $i &lt;= 100; $i++ ){

      if( $i == $premiado ){

        echo '&lt;strong&gt;' .  $i . ' é o número premiado ' . '&lt;/strong&gt;&lt;br /&gt;' . PHP_EOL;

      } else {

          if ( $i % 2 == 0 ){
            echo $i . ' é par ' . '&lt;br /&gt;' . PHP_EOL;
          } else {
            echo $i . ' é impar ' . '&lt;br /&gt;' . PHP_EOL;
          }

      }

    }

} else {

  echo 'O número deve ser menor que 100';

}

?&gt;
</pre>
<p>Como você deve ter  imaginado apenas aninhamos toda a nossa estrutura anterior em uma condicional,  ou seja, antes de iniciar o looping para dizer qual o premiado, primeiro  verificamos se  o <code>$premiado</code> que foi  passado é menor que 100 se for iniciamos o mesmo processo anterior se não  retornamos uma mensagem dizendo que o número deve ser menor que 100.</p>
<div class="dica">
    <p>Em relação as estruturas de controle aninhadas:</p>
    <ul>
        <li>Podem ser aninhadas as <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">estruturas de  controle</a> como também os <a href="/artigo/lacos-de-repeticao-while-e-do-while-no-php">laços de repetições,  loopings</a></li>
        <li>Não a limite de condições que podemos aninhar</li>
        <li>No entanto o bom senso conta, não crie um  aninhamento de por exemplo 10 níveis será difícil de entender quando for ver o  código novamente</li>
        <li>Se as estruturas aninhadas estiverem com uma  grande quantidade de níveis tente rever sua lógica</li>
        <li>Endente o código referente ao bloco em 4 espaços  por questões de legibilidade, a como configurar o seu editor de texto para  transformar Tabs em espaços</li>
      <li>Cada estrutura aninhada também deve ser  endentada em 4 espaços onde a sua estrutura pai terminou, veja nos exemplos  anteriores</li>
    </ul>
</div>
<h2>Break</h2>
<p>A instrução <code>break</code> é  utilizada para encerrar a execução dos comandos <code>for</code>, <code>foreach</code>, falaremos deste  posteriormente, <code>while</code>, <code>do-while</code> e <code>switch</code>. Permitindo que encerremos a instrução  a qualquer momento que desejarmos, sendo assim podemos avaliar uma expressão e  de acordo com o seu resultado encerrar a instrução.</p>
<h3>Problema</h3>
<ul>
    <li>Utilizar  o código criado anteriormente, no entanto agora ao chegar ao número premiado o  looping é encerrado.</li>
</ul>
<h3>No PHP</h3>
<p>Para resolvermos o  problema com o conhecimento que possuímos até aqui sem o uso do <code>break</code> poderíamos simplesmente fazer do seguinte modo:</p>
<pre class="brush: php;">
&lt;?php

$premiado = 77;

if( $premiado &lt; 100 ){

    for( $i = 1; $i &lt;= 100; $i++ ){

      if( $i == $premiado ){

        echo '&lt;strong&gt;' .  $i . ' é o número premiado ' . '&lt;/strong&gt;&lt;br /&gt;' . PHP_EOL;
        $i = 100;

      } else {

          if ( $i % 2 == 0 ){
            echo $i . ' é par ' . '&lt;br /&gt;' . PHP_EOL;
          } else {
            echo $i . ' é impar ' . '&lt;br /&gt;' . PHP_EOL;
          }

      }

    }

} else {

  echo 'O número deve ser menor que 100';

}

?&gt;
</pre>
<p>Simplesmente  fizemos a condição do looping retornar falso, para isso definimos <code>$i</code> com o  valor de 100 pois a condição do looping dizia que ele operaria até <code>$i</code> for menor  ou igual a 100.</p>
<div class="destaque">
    <p>Caso esteja em  dúvida com o looping for volte um pouco e recapitule o que cada uma de suas  expressões representam.</p>
</div>
<p>Agora veja um  exemplo de como podemos usar o <code>break</code> para resolver o mesmo problema.</p>
<pre class="brush: php;">
&lt;?php

$premiado = 77;

if( $premiado &lt; 100 ){

    for( $i = 1; $i &lt;= 100; $i++ ){

      if( $i == $premiado ){

        echo '&lt;strong&gt;' .  $i . ' é o número premiado ' . '&lt;/strong&gt;&lt;br /&gt;' . PHP_EOL;
        break;

      } else {

          if ( $i % 2 == 0 ){
            echo $i . ' é par ' . '&lt;br /&gt;' . PHP_EOL;
          } else {
            echo $i . ' é impar ' . '&lt;br /&gt;' . PHP_EOL;
          }

      }

    }

} else {

  echo 'O número deve ser menor que 100';

}

?&gt;
</pre>
<p>Simplesmente  substituímos à atribuição de um valor a <code>$i</code> para tornar a condição do looping  falsa por uma instrução <code>break</code>. Sendo assim ao utilizar o <code>break</code> automaticamente  o looping é encerrado e o processamento continua fora do looping.</p>
<h3>Break e o seu valor opcional</h3>
<p>O break pode receber um valor opcional indicando  quantos níveis devem ser encerrados, caso possua estruturas de controle  aninhadas.</p>
<h4>Problema</h4>
<ul>
    <li>Programa  que escreva de 1 a 100</li>
    <li>E  abaixo de cada número exiba a frase “Contando...” e os 5 próximos números</li>
    <li>E  quando o número da contagem for igual a 7 <strong>parar  todo o processamento</strong></li>
</ul>
<h4>No PHP</h4>
<p>Veja como poderíamos resolver este problema</p>
<pre class="brush: php;">
&lt;?php

for( $i = 1; $i &lt;= 100; $i++ ){

  echo '&lt;br /&gt;' . $i . '&lt;br /&gt;' . PHP_EOL;
  echo 'Contando...';

  for( $j = $i + 1; $j &lt;= $i + 5; $j++ ){

    if( $j != $i + 5 ){
      echo $j . ', ';
    } else {
      echo $j;
    }

    if($j == 7){
      break 2;
    }

  }

}


?&gt;
</pre>
<p>Primeiro criamos um  for para mostra os números de 1 a 100 e a frase “Contando...”, dentro deste looping  criamos outro looping for, observe que neste utilizamos como contador <code>$j</code> que  possui o valor de <code>$i + 1</code> e como é para mostrar os 5 números próximos a partir  do número antes do contando utilizamos o valor <code>$i + 5</code> e incrementamos <code>$j</code>.  Utilizamos <code>$i</code> para atribuir os valores a <code>$j</code> devido a <code>$i</code> ser trocado em toda  volta sendo assim sempre teremos <code>$j</code> dinâmico de acordo com o valor de <code>$i</code>.  Dentro do looping possuímos um <code>if</code> que verifica se <strong>não</strong> é a ultima volta do looping se não for coloca virgula quando  for a ultima não coloca a virgula. E o outro <code>if</code> é quando verificamos se <code>$j</code> é  igual a 7 se for utilizamos <code>break 2</code>. Utilizamos o <code>break</code> com o valor de 2  dizendo para ele encerrar 2 níveis, sendo primeiro o looping de <code>$j</code> e depois o  looping de <code>$i</code>.</p>
<p>Observe como seria  se utilizássemos apenas o break.</p>
<pre class="brush: php;">
&lt;?php

for( $i = 1; $i &lt;= 100; $i++ ){

  echo '&lt;br /&gt;' . $i . '&lt;br /&gt;' . PHP_EOL;
  echo 'Contando...';

  for( $j = $i + 1; $j &lt;= $i + 5; $j++ ){

    if( $j != $i + 5 ){
      echo $j . ', ';
    } else {
      echo $j;
    }

    if($j == 7){
      break;
    }

  }

}


?&gt;
</pre>
<p>Conseguimos  encerrar o looping de <code>$j</code> quando fosse o valor 7 no entanto observe que o  looping de <code>$i</code> é executado. Está é a utilidade de adicionar um valor ao <code>break</code>,  pois assim você consegue encerrar quantos níveis forem necessários passando o  valor para o <code>break</code>.</p>
<div class="dica">
    <p>Em relação ao <code>break</code>:</p>
    <ul>
        <li>É utilizado nos comandos <code>for</code>, <code>foreach</code>, falaremos deste posteriormente,  <code>while</code>, <code>do-while</code> e <code>switch</code>.</li>
        <li>Sua função é finalizar uma instrução, das  citadas anteriormente.</li>
        <li>Pode receber um valor adicional indicando  quantos níveis devem ser encerrados.</li>
      <li>Para o break receber um valor adicional o mesmo  deve está dentro de uma estrutura aninhada</li>
    </ul>
</div>
<h2>Continue</h2>
<p>Bastante parecido com o <code>break</code>, a instrução <code>continue</code> permite que a execução do looping seja alterada, no entanto não  encerramos o looping, apenas encerramos a <strong>iteração</strong>,  volta do looping, atual e iniciamos a próxima.</p>
<h3>Problema</h3>
<ul>
    <li>Um  looping for, predefinido terá que ser utilizado, este looping exibe os números  de 1 a 100.</li>
    <li>Dentro  deste looping exiba apenas os números pares</li>
</ul>
<h3>No PHP</h3>
<p>Veja a nossa  possível solução para este problema no PHP.</p>
<pre class="brush: php;">
&lt;?php

for( $i = 1; $i &lt;= 100; $i++ ){

  if( $i % 2 != 0 ){
    continue;
  }

  echo $i . '&lt;br /&gt;' . PHP_EOL;

}


?&gt;
</pre>
<p>Mantemos  o looping do problema e dentro dele criamos um <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">if</a> em que se módulo de <code>$i</code> <strong>não</strong> for igual a 0, ou seja não é par, utilizamos o continue para  irmos para próxima volta do looping.</p>
<h3>Continue e o seu valor opcional</h3>
<p>Assim como o <code>break</code> o <code>continue</code> também pode receber um valor opcional indicando quantos níveis devem ser  encerrados. Lembrando que deve possuir estruturas de controle aninhadas.</p>
<h4>Problema</h4>
<ul>
    <li>Programa  que escreva de 1 a 100</li>
    <li>E  abaixo de cada número exiba a frase “Contando...” e os 5 próximos números</li>
    <li>Quando  o número da contagem for igual a sete ele deve ser ignorado, se houver mais <strong>números</strong> depois dele <strong>não</strong> deve ser exibido também</li>
</ul>
<h4>No PHP</h4>
<p>Veja como  poderíamos resolver este problema:</p>
<pre class="brush: php;">
&lt;?php

for( $i = 1; $i &lt;= 100; $i++ ){

  echo '&lt;br /&gt;' . $i . '&lt;br /&gt;' . PHP_EOL;
  echo 'Contando...';

  for( $j = $i + 1; $j &lt;= $i + 5; $j++ ){

    if( $j == 7 ){
      continue 2;
    }

    if( $j != $i + 5 ){
      echo $j . ', ';
    } else {
      echo $j;
    }



  }

}


?&gt;
</pre>
<p>Como você pode ver  a lógica é a mesma que utilizamos no <code>break 2</code>, no entanto observe que usamos o  continue com o valor 2. Sendo assim sempre que houver um 7 na contagem saímos  do segundo looping e iniciamos no primeiro looping.</p>
<p>Observe como seria  se utilizássemos apenas o continue:</p>
<pre class="brush: php;">
&lt;?php

for( $i = 1; $i &lt;= 100; $i++ ){

  echo '&lt;br /&gt;' . $i . '&lt;br /&gt;' . PHP_EOL;
  echo 'Contando...';

  for( $j = $i + 1; $j &lt;= $i + 5; $j++ ){

    if( $j == 7 ){
      continue;
    }

    if( $j != $i + 5 ){
      echo $j . ', ';
    } else {
      echo $j;
    }

  }

}


?&gt;
</pre>
<p>Encerramos a iteração, a volta, do looping de <code>$j</code> quando o  valor fosse igual a 7 no entanto retornamos para o looping de <code>$j</code> já com o valor  do continue conseguimos encerrar quantos níveis forem necessários.</p>
<div class="dica">
    <p>Em relação ao <code>continue</code>:</p>
    <ul>
        <li>É utilizado nos comandos <code>for</code>, <code>foreach</code>, falaremos deste posteriormente,  <code>while</code>, <code>do-while</code> e <code>switch</code>.</li>
        <li>Sua função é finalizar uma iteração, volta, das  citadas anteriormente.</li>
        <li>Pode receber um valor adicional indicando  quantos níveis o <code>continue</code> deve considerar para encerrar a iteração.</li>
        <li>Para o <code>continue</code> receber um valor adicional o  mesmo deve está dentro de uma estrutura aninhada</li>
    </ul>
</div>