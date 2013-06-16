---
layout: post
title: Conversão de tipos de dados no PHP
meta_description: Entenda a conversão de tipos de dados no PHP, é possível somar uma string com um inteiro? E com um float? E se diminuir um inteiro de um booleano? Essas e outras conversões serão explicadas no artigo.
meta_keywords: Conversão, convercao,  tipos de dados, tipos,  integer,  float,  string, boolean, conversão automática, automática, inteiro, real, ponto flutuante
summary: Entenda a conversão de tipos de dados no PHP, é possível somar uma string com um inteiro? E com um float? E se diminuir um inteiro de um booleano? Essas e outras conversões serão explicadas no artigo.
tags: [Tipos de dados, Integer, Float, String, Boolean]
---
<p>No PHP é possível <a href="http://www.php.net/manual/pt_BR/language.types.type-juggling.php#language.types.typecasting">converter  a variável de um tipo para outro</a>. Para isso devemos utilizar os conversores  de tipos, para fazer a conversão devemos utilizar o tipo pra qual devemos  converter entre parênteses antes do nome da variável em que se deseja  converter. No PHP possuímos os seguintes conversores:</p>
<table>
  <thead>
    <tr>
      <th>Conversor</th>
      <th>Função</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>(int)</code>, <code>(integer)</code></td>
      <td>converte para inteiro</td>
    </tr>
        <tr>
      <td><code>(bool)</code>, <code>(boolean)</code></td>
      <td>converte para booleano</td>
    </tr>
        <tr>
      <td><code>(float)</code>, <code>(double)</code>, <code>(real)</code></td>
      <td>converte para float</td>
    </tr>
        <tr>
      <td><code>(string)</code></td>
      <td>converte para string</td>
    </tr>
        <tr>
      <td><code>(array)</code></td>
      <td>converte para array</td>
    </tr>
        <tr>
      <td><code>(object)</code></td>
      <td>converte para objeto</td>
    </tr>
  </tbody>
</table>
<h2>Conversão de dados para inteiros no PHP</h2>
<p>Para converter um valor para inteiro como foi visto anteriormente basta utilizarmos um dos conversores de inteiro antes do valor.  Observe o exemplo:</p>
<h3>Conversão de float em inteiro</h3>
<p>Quando convertemos um número de float, ponto flutuante, para inteiro ele sempre terá o seu valor truncado, ou seja, arredondado para baixo.  Observe:</p>
<pre class="brush: php;">
&lt;?php

$float = (int) 10.9;

var_dump( $float );

echo '&lt;br /&gt;' . PHP_EOL;

$float2 = (int) 10.1;

var_dump( $float2 );

?&gt;
</pre>
<p>Como você pode observar ambos os valores 10.9 e 10.1 foram convertidos para 10.</p>
<div class="dica">
  <p>A função <code>var_dump()</code> utilizada anteriormente além de exibir o valor da variável mostrará também o tipo da variável como você verá ao testar os exemplos, como estamos trabalhando com tipos de dados é ideal sabermos se o valor foi convertido ou não. </p>
</div>
<h3>Conversão de string em inteiro</h3>
<p>A conversão de string para inteiro depende do formato da  string, assim o PHP avalia o formato da string caso <strong>não</strong> possua nenhum valor numérico será convertido para 0(zero). Caso  possua <strong>valor numérico em sua primeira  posição</strong> o valor será considerado caso o valor não seja na primeira posição será desconsiderado. Veja o exemplo:</p>
<pre class="brush: php;">
&lt;?php

$string = (int) 'Muitas casas';

var_dump( $string ); // int(0)

echo '&lt;br /&gt;' . PHP_EOL;

$string2 = (int) '10 casas aproximadamente';

var_dump( $string2 ); // int(10)

echo '&lt;br /&gt;' . PHP_EOL;

$string3 = (int) 'Exatamente 10 casas';

var_dump( $string3 ); // int(0)

?&gt;
</pre>
<h3>Conversão de booleano em inteiro</h3>
<p>A conversão de booleano para string segue uma regra simples em que o valor <code>TRUE</code> é definido como 1(um) e o valor <code>FALSE</code> é definido como  0(zero). Observe:</p>
<pre class="brush: php;">
&lt;?php

$bool = (int) TRUE;

var_dump( $bool );

echo '&lt;br /&gt;' . PHP_EOL;

$bool2 = (int) FALSE;

var_dump( $bool2 );

?&gt;
</pre>
<h2>Conversão de dados para float no PHP</h2>
<p>A conversão para float como pode ser observado anteriormente na tabela é feita pelos conversores <code>(float)</code>, <code>(double)</code> ou  <code>(real)</code>. As regras de conversão para float <strong>seguem  as mesmas que você acabou de ver na conversão de dados para inteiros</strong>.  Exceto na conversão para strings.</p>
<h3>Conversão de string em float</h3>
<p>Na conversão para float a string  será avaliada como um ponto flutuante se conter  qualquer um dos caracteres '<code>.</code>', '<code>e</code>', ou '<code>E</code>', lembrando que a string deve ser  iniciada com um número. Caso contrário será convertido para 0(Zero), lembrando  que este zero será um float devido a conversão. Observe:</p>
<pre class="brush: php;">
&lt;?php

$string = (float) '1.75cm';

var_dump( $string ); // float(1.75)

echo '&lt;br /&gt;' . PHP_EOL;

$string2 = (float) 'Ele possuia 1.75cm';

var_dump( $string2 ); // float(0)

?&gt;
</pre>
<h2>Conversão de dados para strings no PHP</h2>
<p>Para converter um dado para string você já deve estar  imaginando que basta utilizar o conversor <code>(string)</code> e é exatamente isto.</p>
<h3>Conversão de booleano em string</h3>
<p>Quando convertemos um valor booleano para string ocorre uma  simples regra o valor <code>TRUE</code> será convertido na string 1 e o valor <code>FALSE</code> será  convertido em uma string vazia. Observe:</p>
<pre class="brush: php;">
&lt;?php

$bool = (string) TRUE;

var_dump( $bool ); // string(1) "1"

echo '&lt;br /&gt;' . PHP_EOL;

$bool2 = (string) FALSE;

var_dump( $bool2 ); // string(0) ""

?&gt;
</pre>
<h3>Conversão de inteiro e float em string</h3>
<p>Na conversão de inteiro e float o número será convertido  para string mantendo a sua representação. Observe:</p>
<pre class="brush: php;">
&lt;?php

$inteiro = (string) 150;

var_dump( $inteiro ); // string(3) "150"

echo '&lt;br /&gt;' . PHP_EOL;

$float = (string) 1.77;

var_dump( $float ); // string(4) "1.77"

?&gt;
</pre>
<h2>Conversão de dados para booleano no PHP</h2>
<p>Na conversão de dados para booleano os seguintes valores  serão considerados <code>FALSE</code> (falso):</p>
<ul>
    <li>O próprio booleano <code>FALSE</code></li>
    <li>O inteiro 0 (zero)</li>
    <li>O ponto flutuante 0.0 (zero)</li>
    <li>Uma string vazia e a string &quot;0&quot;</li>
</ul>
<p>Qualquer outro valor será convertido em <code>TRUE</code> (verdadeiro),  observe:</p>
<pre class="brush: php;">
&lt;?php

$bool = (bool) FALSE;

var_dump( $bool ); // bool(false)

echo '&lt;br /&gt;' . PHP_EOL;

$inteiro = (bool) 0;

var_dump( $inteiro ); // bool(false)

echo '&lt;br /&gt;' . PHP_EOL;

$float = (bool) 0.0;

var_dump( $float ); // bool(false)

echo '&lt;br /&gt;' . PHP_EOL;

$string = (bool) '';

var_dump( $string ); // bool(false)

echo '&lt;br /&gt;' . PHP_EOL;

$inteiro = (bool) 10;

var_dump( $inteiro ); // bool(true)

echo '&lt;br /&gt;' . PHP_EOL;

$float = (bool) 1.0;

var_dump( $float ); // bool(true)

echo '&lt;br /&gt;' . PHP_EOL;

$string = (bool) 'Uma string';

var_dump( $string ); // bool(true)

?&gt;
</pre>
<h2>Conversão automática de tipos de dados no PHP</h2>
<p>Apesar de existirem os conversores que acabamos  de ver o PHP também possui a conversão automática de tipos que funciona  seguindo as mesmas regras que acabamos de ver observe.</p>
<pre class="brush: php;">
&lt;?php

$soma = 10 + 3.5;

var_dump( $soma ); // float(13.5)

echo '&lt;br /&gt;' . PHP_EOL;

$soma = 10 + 7.0;

var_dump( $soma ); // float(17)

echo '&lt;br /&gt;' . PHP_EOL;

$soma = 10 + FALSE;

var_dump( $soma ); // int(10)

echo '&lt;br /&gt;' . PHP_EOL;

$soma = 1 + '7.5';

var_dump( $soma ); // float(8.5)

echo '&lt;br /&gt;' . PHP_EOL;

$soma = 1 + '-7.5 graus celcius';

var_dump( $soma ); // float(-6.5)

echo '&lt;br /&gt;' . PHP_EOL;

$soma = 1 + 'Luanito 20 anos';

var_dump( $soma ); // int(1)

echo '&lt;br /&gt;' . PHP_EOL;

$soma = '20 anos de carreira' + 1;

var_dump( $soma ); // int(21)

?&gt;
</pre>
<p>Como você pode observar se utilizarmos float e inteiro em  uma operação o resultado final será float, o valor <code>FALSE</code> possui o valor 0  (zero) os dados seguiram se as mesmas regras de conversão, inclusive as strings  que só as iniciadas com valores numéricos são validas para operações  matemáticas, ou seja as regras válidas nas conversões de dados também são  aplicadas aqui na conversão automática de tipos.</p>
<div class="destaque">
  <p>Não  utilizamos os conversores para array e nem para objeto como você pode observar,  mais não se preocupe assim que estes dados forem estudados mostraremos a  conversão dos mesmos.</p>
</div>