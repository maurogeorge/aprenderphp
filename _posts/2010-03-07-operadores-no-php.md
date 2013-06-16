---
layout: post
title: Operadores no PHP
meta_description: Introdução aos operadores no PHP, passando pelos operadores aritméticos, os de strings além dos operadores de incremento e decremento.
meta_keywords: Operadores, Operadores aritméticos, Operadores de Atribuição, Operadores de string, Operador de incremento, Operador de decremento, Inverter o sinal no PHP, Atribuição por referência
summary: Introdução aos operadores no PHP, passando pelos operadores aritméticos, os de strings além dos operadores de incremento e decremento.
tags: [Integer, Float, String, Operadores, Operadores aritméticos, Operadores de Atribuição, Operadores de string, Operador de incremento, Operador de decremento, Inverter o sinal no PHP, Atribuição por referência]
---
<h2>Introdução aos operadores no PHP</h2>
<p>Um operador é utilizado para realizar operações entre um ou  mais valores (ou expressões, no jargão de programação) e retornar apenas um  valor final. Vamos agora aos operadores.</p>
<h2>Operadores aritméticos no PHP</h2>
<p>Neste grupo de operadores estão os operadores de operações  matemáticas básicas como adição, subtração, multiplicação e divisão. Veja a  tabela com os operadores:</p>
<table>
  <thead>
    <tr>
      <th>Operador</th>
      <th>Função</th>
      <th>Exemplo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>+</code></td>
      <td>Adição</td>
      <td><code>$a + $b</code></td>
    </tr>
    <tr>
      <td><code>-</code></td>
      <td>Subtração</td>
      <td><code>$a - $b</code></td>
    </tr>
    <tr>
      <td><code>*</code></td>
      <td>Multiplicação</td>
      <td><code>$a * $b</code></td>
    </tr>
    <tr>
      <td><code>/</code></td>
      <td>Divisão</td>
      <td><code>$a / $b</code></td>
    </tr>
    <tr>
      <td><code>%</code></td>
      <td>Módulo (resto da divisão)</td>
      <td><code>$a % $b</code></td>
    </tr>
  </tbody>
</table>
<p>Veja um exemplo com os operadores aritméticos.</p>
<div class="observacao">
  <p>A  partir deste ponto <strong>não</strong> irei incluir  todos os elementos necessários para uma página HTML bem formatada de acordo com  o W3C, apenas incluirei os códigos PHP, por ser o foco de nosso estudo, caso  ainda tenha alguma duvida sobre a integração PHP e HTML visite a página Começando  a programar em PHP.</p>
</div>
<pre class="brush: php; html-script: true">
&lt;?php
// Declarando os valores das variáveis
$a = 4;
$b = 2;

?&gt;
&lt;h2&gt;Adição&lt;/h2&gt;
&lt;p&gt;
&lt;?php

echo $a + $b;

?&gt;
&lt;/p&gt;
&lt;h2&gt;Subtração&lt;/h2&gt;
&lt;p&gt;
&lt;?php

echo $a - $b;

?&gt;
&lt;/p&gt;
&lt;h2&gt;Multiplicação&lt;/h2&gt;
&lt;p&gt;
&lt;?php

echo $a * $b;

?&gt;
&lt;/p&gt;
&lt;h2&gt;Divisão&lt;/h2&gt;
&lt;p&gt;
&lt;?php

echo $a / $b;

?&gt;
&lt;/p&gt;
&lt;h2&gt;Módulo(resto da divisão)&lt;/h2&gt;
&lt;p&gt;
&lt;?php

echo $a % $b;

?&gt;
&lt;/p&gt;
</pre>
<p>Observe que o módulo deu zero, pois utilizamos uma operação  em que a divisão em que não tinha resto. Veja agora um exemplo em que nossa  divisão gera resto.</p>
<pre class="brush: php; html-script: true">
&lt;?php
// Declarando os valores das variáveis
$a = 5;
$b = 2;

?&gt;
&lt;h1&gt;Valores&lt;/h1&gt;
&lt;p&gt;$a possui o valor de &lt;strong&gt;&lt;?php echo $a; ?&gt;&lt;/strong&gt; e $b possui o valor de &lt;strong&gt;&lt;?php echo $b; ?&gt;&lt;/strong&gt;&lt;/p&gt;
&lt;h2&gt;Módulo(resto da divisão)&lt;/h2&gt;
&lt;p&gt;
&lt;?php

echo $a % $b;

?&gt;
&lt;/p&gt;
</pre>
<h2>Operadores de Atribuição no PHP</h2>
<p>O operador de atribuição é utilizado quando queremos  atribuir o valor da expressão que esta a direita ao operando (normalmente uma  variável) que esta a sua esquerda (quase como se fosse um “igual a”, como por  exemplo x é igual a 1 e y igual a 2).</p>
<p>O operador mais básico de atribuição você já deve estar  imaginando é o sinal de igual (=) em que usamos para atribuir todas as nossas  variáveis anteriormente. Veja a seguir o uso do operador de atribuição igual e  um truque que podemos fazer utilizando <strong>operadores  aritméticos </strong>e <strong>expressões</strong>.</p>
<pre class="brush: php; html-script: true">
&lt;?php
// Declarando o valor de a com uma simples expressão
$a = 5 + 3;

echo $a; //imprime 8

?&gt;
&lt;br /&gt;
&lt;?php

// Atribuimos o valor de 2 a variavel $c e somamos com
// 5 para ser o valor de b
$b = ( $c = 2 ) + 5;

echo $b; //imprime 7

?&gt;
&lt;br /&gt;
&lt;?php

echo $c; //imprime 2

?&gt;
</pre>
<p>Observe que conseguimos declarar o valor de <code>$a</code> uma simples  expressão aritmética, lembrando que você pode utilizar todos os <strong>operadores aritméticos</strong> que aprendemos  anteriormente em sua expressão.</p>
<p>Em seguida criamos a variável <code>$b</code> e <code>$c</code>, sendo <code>$c</code> criada  dentro da atribuição de <code>$b</code> sendo assim <code>$b</code> equivale a <code>$c</code>, que equivale a 2, mais  5.</p>
<p>Além do formato de atribuição que aprendemos  podemos combinar o operador de atribuição a todos os operadores aritméticos e de  string observe a tabela a seguir:</p>
<table>
  <thead>
    <tr>
      <th>Operador</th>
      <th>Função</th>
      <th>Exemplo</th>
      <th>Equivalente a</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>+=</code></td>
      <td>Atribuição e adição</td>
      <td><code>$a += $b</code></td>
      <td><code>$a = $a + $b</code></td>
    </tr>
    <tr>
      <td><code>-=</code></td>
      <td>Atribuição e Subtração</td>
      <td><code>$a -= $b</code></td>
      <td><code>$a = $a - $b</code></td>
    </tr>
    <tr>
      <td><code>*=</code></td>
      <td>Atribuição e Multiplicação</td>
      <td><code>$a *= $b</code></td>
      <td><code>$a = $a * $b</code></td>
    </tr>
    <tr>
      <td><code>/=</code></td>
      <td>Atribuição e Divisão</td>
      <td><code>$a /= $b</code></td>
      <td><code>$a = $a / $b</code></td>
    </tr>
    <tr>
      <td><code>%=</code></td>
      <td>Atribuição e Módulo</td>
      <td><code>$a %= $b</code></td>
      <td><code>$a = $a % $b</code></td>
    </tr>
    <tr>
      <td><code>.=</code></td>
      <td>Atribuição e concatenação</td>
      <td><code>$a .= $b</code></td>
      <td><code>$a = $a . $b</code></td>
    </tr>
  </tbody>
</table>
<div class="observacao">
  <p>Você ainda provavelmente não conhece o operador de concatenação mais não se preocupe, eles serão explicados detalhadamente a seguir.</p>
</div>
<p>Veja agora um exemplo utilizando <strong>operadores de atribuição</strong> em conjunto com os <strong>operadores aritméticos.</strong></p>
<pre class="brush: php;">
&lt;?php
// Declarando o valor de a
$a = 5;
// Atribuindo e somando 3 em $a
// ou seja $a = 5 + 3;
$a += 3;

echo $a //imprime 8

?&gt;
</pre>
<p>Definimos o valor de $a com utilizando o operador de  atribuição e adição em conjunto. No entanto observe o exemplo a seguir:</p>
<pre class="brush: php;">
&lt;?php
// Declarando o valor de a
$a = 5;

// Redeclarando o valor de a
$a = 3;

echo $a //imprime 3
// Caso quisessemos somar 3 a $a poderiamos utilizar
// $a = 3
// $a += 5;
//
// Ou ainda
// $a = 5 + 3;

?&gt;
</pre>
<p>Neste exemplo declaramos <code>$a</code> e em seguida a redeclaramos, não  confundir este comportamento ao tentar utilizar os <strong>operadores de atribuição</strong> em conjunto com os <strong>operadores aritméticos</strong>. Pois como vimos podemos atribuir valores  utilizando os operadores aritméticos ou com operadores de atribuição em  conjunto com os operadores aritméticos.</p>
<h2>Operadores de string no PHP</h2>
<p>O único operador de string que possuímos no PHP é o operador  de concatenação, além do que falamos anteriormente que é o de atribuição e concatenação, que é representado pelo <code>.</code> (ponto). O operador de concatenação tem  por finalidade unir o conteúdo de duas strings, veja o exemplo:</p>
<pre class="brush: php;">
&lt;?php
// Declaro a variável $titulo
$titulo = 'Operadores de string no PHP';
// Concateno $titulo a $texto
$texto = 'Estou aprendendo sobre ' . $titulo;

echo $texto;

echo '<br />' . PHP_EOL;

// Mesmo exemplo anterior porém utilizando atribuição e concatenação
$texto = 'Estou aprendendo sobre ';
$texto .= $titulo;

echo $texto;
?&gt;
</pre>
<h2>Operador de incremento/decremento no PHP</h2>
<p>Os operadores de incremento e decremento são muito parecidos  com os <strong>operadores aritméticos</strong>. Eles  permitem que sejam feitas adições (incremento) e subtrações (decremento) direto  na variável informada, mas sempre operações unitárias, isto é, soma se 1 ou subtrai  se 1 da variável. Os operadores de incremento e decremento são respectivamente  <code>++</code> e <code>--</code>.</p>
<p>Existem duas formas de incremento/decremento: Pós e Pré.</p>
<h3>Pós incremento/decremento no PHP</h3>
<p>No pós incremento/decremento o PHP retorna o valor da  variável para só depois então a incrementá-la/decrementá-la. Veja o exemplo:</p>
<pre class="brush: php;">
&lt;?php

$a = 10;
$b = $a++; // Primeiro $a é atribuido a $b para só então ser incrementada
$a++;

echo '$a = ' . $a . ' | $b = ' . $b;

?&gt;
</pre>
<p>Atribuímos o valor de <code>$a++</code> a variável <code>$b</code>, no entanto como no  pós incremento/decremento primeiro retorna o valor para só depois ocorrer o  incremento/decremento <code>$b</code> ficou com o valor de <code>$a</code> inicial, ou seja 10, e <code>$a</code> foi  incrementado 2 vezes ficando com o valor de 12.</p>
<h3>Pré incremento/decremento no PHP</h3>
<p>No pré incremento/decremento o PHP primeiro  incrementa/decrementa a variável e depois retorna o seu valor. Observe  alterando o exemplo anterior:</p>
<pre class="brush: php;">
&lt;?php

$a = 10;
$b = ++$a; // Primeiro $a é incrementada e só depois é atribuido a $b
++$a;

echo '$a = ' . $a . ' | $b = ' . $b;

?&gt;
</pre>
<p>Atribuímos o valor de <code>++$a</code> a variável <code>$b</code>, no entanto como no  pré incremento/decremento primeiro ocorre o incremento/decremento em seguida  retorna o valor para <code>$b</code>, que ficou com o valor de <code>$a</code> inicial incrementado, ou  seja 11, e <code>$a</code> foi incrementada novamente ficando com o valor de 12.</p>
<h3>Inverter o sinal no PHP</h3>
<p>Além de incremento/decremento podemos inverter o sinal de um  operador com o sinal de –(menos) veja a seguir:</p>
<pre class="brush: php;">
&lt;?php

$a = 10;
$b = -$a; // Inverte o sinal de $a e atribui a $b


echo '$a = ' . $a . ' | $b = ' . $b;

?&gt;
</pre>
<p>Como você pode observar apenas alterou o sinal de positivo  para negativo, o inverso também é possível.</p>
<p>Fique agora com uma tabela para uma consulta caso tenha  duvida nos operadores de incremento e decremento.</p>
<table>
  <thead>
    <tr>
      <th>Operador</th>
      <th>Nome</th>
      <th>Função</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>++$a</code></td>
      <td>Pré-incremento</td>
      <td>Incrementa <code>$a</code> em um, e então retorna <code>$a</code>.</td>
    </tr>
    <tr>
      <td><code>$a++</code></td>
      <td>Pós-incremento</td>
      <td>Retorna <code>$a</code>, e então incrementa <code>$a</code> em um.</td>
    </tr>
    <tr>
      <td><code>--$a</code></td>
      <td>Pré-decremento</td>
      <td>Decrementa <code>$a</code> em um, e então retorna <code>$a</code>.</td>
    </tr>
    <tr>
      <td><code>$a--</code></td>
      <td>Pós-decremento</td>
      <td>Retorna <code>$a</code>, e então decrementa <code>$a</code> em um.</td>
    </tr>
    <tr>
      <td><code>-$a</code></td>
      <td>Inverter o sinal</td>
      <td>Inverte o sinal de <code>$a</code> e retorna <code>$a</code>.</td>
    </tr>
  </tbody>
</table>
<h2>Atribuição por referência</h2>
<p>Outro meio de atribuir valores a variáveis que o PHP nos  fornece é a atribuição por referência.  Ou seja, a nova variável será uma referência,  um apelido, a variável original sendo assim qualquer alteração na variável  original alterará a variável de referencia como qualquer alteração na variável  de referência alterara a variável original. Observe:</p>
<pre class="brush: php;">
&lt;?php

// Criamos a variável $b
$b = 'Estamos aprendendo sobre';

// Atribuimos por referência o valor de $b a $a,
// ou seja, ambas agora possuem o mesmo valor
$a = &amp;$b;

// Altero o valor de $a concatenando o com uma string
// caso não tenha entendido a concatenação volte a operadores de string
$a .= ' Atribuição por referência no PHP';

// Exibo $a e $b pulando linhas para melhor vizualização
echo $a;

echo '&lt;br /&gt;' . PHP_EOL;

echo $b;

echo '&lt;br /&gt;' . PHP_EOL;

// Alterei o valor de $b e como $b foi atribuido por referência a $a
// agora quando altero $b o valor de $a muda também
$b = 'Alterei o valor de $b e sabia que o de $a muda também?';

echo $a;

echo '&lt;br /&gt;' . PHP_EOL;

echo $b;

?&gt;
</pre>
<div class="destaque">
  <p>Caso você já tenha programado em PHP ou mesmo em outra linguagem deve estar se perguntado sobre os operadores de comparação, os operadores lógicos e até mesmo o operador ternário. Não se preocupe quando chegarmos em estruturas de controle voltaremos a falar sobre operadores.</p>
</div>