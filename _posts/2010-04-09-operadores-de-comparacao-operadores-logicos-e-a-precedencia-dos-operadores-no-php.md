---
layout: post
title: Operadores de comparação, operadores lógicos e a precedência dos operadores  no PHP
meta_description: Aprenda um pouco sobre os operadores de comparação e os operadores lógicos no PHP, além da precedência dos operadores qual tem maior precedência o de divisão ou o de soma qual o PHP avalia primeiro?
meta_keywords: PHP, operadores de comparação, operadores lógicos, precedência dos operadores, comparacao, logicos, precedencia, operadores
summary: Aprenda um pouco sobre os operadores de comparação e os operadores lógicos no PHP, além da precedência dos operadores qual tem maior precedência o de divisão ou o de soma qual o PHP avalia primeiro?
tags: [Tipos de dados, Operadores]
---
<p>Como foi dito no artigo de <a href="/artigo/operadores-no-php">operadores no PHP</a> quando chegássemos a  estruturas de controle no PHP voltaríamos a abordar alguns novos operadores,  pois são diretamente ligados as estruturas de controle. Então primeiro veremos  dois novos operadores e em seguida entraremos nas estruturas de controle.</p>
<h2>Operadores de comparação</h2>
<p>Operadores de  comparação como o próprio nome já diz compara dois valores retornando  verdadeiro (<code>TRUE</code>) ou falso (<code>FALSE</code>).</p>
<p>Veja uma tabela com  os operadores de comparação.</p>
<table>
  <thead>
    <tr>
      <th>Operador</th>
      <th>Nome</th>
            <th>Exemplo</th>
      <th>Resultado</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>==</code></td>
      <td>Igual</td>
      <td><code>$a == $b</code></td>
            <td>Verdadeiro se <code>$a</code> for igual a <code>$b</code></td>
    </tr>
        <tr>
      <td><code>!=</code></td>
      <td>Diferente</td>
      <td><code>$a != $b</code></td>
            <td>Verdadeiro se <code>$a</code> <strong>não</strong> for igual a <code>$b</code></td>
    </tr>
        <tr>
      <td><code>&lt;&gt;</code></td>
      <td>Diferente</td>
      <td><code>$a &lt;&gt; $b</code></td>
            <td>Verdadeiro se <code>$a</code> <strong>não</strong> for igual a <code>$b</code></td>
    </tr>
        <tr>
      <td><code>===</code></td>
      <td>Idêntico</td>
      <td><code>$a === $b</code></td>
            <td>Verdadeiro se <code>$a</code> for igual a <code>$b</code> e for do mesmo <a href="/artigo/tipos-de-dados-no-php"><strong>tipo</strong></a></td>
    </tr>
        <tr>
      <td><code>!==</code></td>
      <td>Não idêntico</td>
      <td><code>$a !== $b</code></td>
            <td>Verdadeiro se <code>$a</code> <strong>não</strong> for igual a <code>$b</code>, ou eles  não são do mesmo <a href="/artigo/tipos-de-dados-no-php"><strong>tipo</strong></a></td>
    </tr>
        <tr>
      <td><code>&lt;</code></td>
      <td>Menor que</td>
      <td><code>$a &lt; $b</code></td>
            <td>Verdadeiro se <code>$a</code> for menor que <code>$b</code></td>
    </tr>
        <tr>
      <td><code>&gt;</code></td>
      <td>Maior que</td>
      <td><code>$a &gt; $b</code></td>
            <td>Verdadeiro se <code>$a</code> for maior que <code>$b</code></td>
    </tr>
        <tr>
      <td><code>&lt;=</code></td>
      <td>Menor ou igual</td>
      <td><code>$a &lt;= $b</code></td>
            <td>Verdadeiro se <code>$a</code> for menor ou igual a <code>$b</code>.</td>
    </tr>
        <tr>
      <td><code>&gt;=</code></td>
      <td>Maior ou igual</td>
      <td><code>$a &gt;= $b</code></td>
            <td>Verdadeiro se <code>$a</code> for maior ou igual a <code>$b</code>.</td>
    </tr>
  </tbody>
</table>
<p>Veja um exemplo com  cada um dos operadores, utilizaremos a função <code>var_dump()</code>, para retornar o  resultado.</p>
<pre class="brush: php;">
&lt;?php
/**
 * Igual
 */
var_dump( 7 == 7 ); // TRUE, são iguais

var_dump( 7 == 6 ); // FALSE, são diferentes

/**
 * Diferente
 */
var_dump( 7 != 7 ); // FALSE, pois não são diferentes

var_dump( 7 != 6 ); // TRUE, pois são diferentes

// Segundo operador diferente
var_dump( 7 &lt;&gt; 7 ); // FALSE, pois não são diferentes

var_dump( 7 &lt;&gt; 6 ); // TRUE, pois são diferentes

/**
 * Idêntico
 */
var_dump( 7 === 7 ); // TRUE, pois são iguais e do mesmo tipo, inteiros

var_dump( 7 === 7.0 ); // FALSE, pois não são do mesmo tipo

/**
 * Não idêntico
 */
var_dump( 7 !== 7 ); // FALSE, pois são iguais e do mesmo tipo, inteiros

var_dump( 7 !== 7.0 ); // TRUE, pois não são do mesmo tipo

/**
 * Menor que
 */
var_dump( 7 &lt; 8 ); // TRUE, 7 é menor que 8

var_dump( 7 &lt; 6 ); // FALSE, 7 não é menor que 6

/**
 * Maior que
 */
var_dump( 7 &gt; 6 ); // TRUE, 7 é maior que 6

var_dump( 7 &gt; 8 ); // FALSE, 7 não é maior que 8

/**
 * Menor ou igual
 */
var_dump( 7 &lt;= 7 ); // TRUE, 7 é igual a 7

var_dump( 7 &lt;= 6 ); // FALSE, 7 não é menor nem igual a 6

var_dump( 3 &lt;= 7 ); // TRUE, 3 é menor que 7

/**
 * Maior ou igual
 */
var_dump( 7 &gt;= 7 ); // TRUE, 7 é igual a 7

var_dump( 7 &gt;= 8 ); // FALSE, 7 não é maior nem igual a 8

var_dump( 10 &gt;= 7 ); // TRUE, 10 é maior que 7

?&gt;
</pre>
<p>Observe que não  definimos variáveis por questões didáticas comparamos valores diretos mais não  se esqueça que você pode comparar variável com variável e variável com valores  fixos ou ainda como fizemos para exemplificar apenas os valores, resumindo  qualquer tipo de dado pode ser comparado. E como foi dito anteriormente o  resultado sempre será verdadeiro ou falso, neste ponto pode parecer inútil mais  daqui a pouco fará mais sentido o retorno destes resultados. E não se esqueça que as <a href="/artigo/conversao-de-tipos-de-dados-no-php">conversões de dados</a> são válidas aqui os valores são convertidos  automaticamente quando comparados.</p>
<h2>Operadores lógicos</h2>
<p>Os operadores  lógicos realizam comparação entre expressões, exceto o <code>!</code> que compara apenas um  valor,  e como os operadores de  comparação retornam verdadeiro (<code>TRUE</code>) ou falso (<code>FALSE</code>).</p>
<p>Observe a tabela  com os operadores lógicos.</p>
<table>
  <thead>
    <tr>
      <th>Operador</th>
      <th>Nome</th>
            <th>Exemplo</th>
            <th>Resultado</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>AND</code></td>
      <td>E</td>
      <td><code>( 10 &gt; 7 ) AND ( 9 == 9 )</code></td>
      <td>Verdadeiro se 10 for maior que 7 <strong>e</strong> 9 for igual a 9</td>
    </tr>
        <tr>
      <td><code>OR</code></td>
      <td>Ou</td>
      <td><code>( 10 &gt; 7 ) OR ( 9 == 9 )</code></td>
      <td>Verdadeiro se 10 for maior que 7 <strong>ou</strong> 9 for igual a 9</td>
    </tr>
        <tr>
      <td><code>XOR</code></td>
      <td>Ou exclusivo</td>
      <td><code>( 10 &gt; 7 ) XOR ( 9 == 9 )</code></td>
      <td>Verdadeiro se 10 for maior que 7 <strong>ou</strong> 9 for igual a 9, mais não se ambos forem verdadeiro</td>
    </tr>
        <tr>
      <td><code>!</code></td>
      <td>Negação</td>
      <td><code>! ( 10 &gt; 7 )</code></td>
      <td>Verdadeiro se 10 for menor que 7</td>
    </tr>
        <tr>
      <td><code>&amp;&amp;</code></td>
      <td>E</td>
      <td><code>( 10 &gt; 7 ) &amp;&amp; ( 9 == 9 )</code></td>
      <td>Verdadeiro se 10 for maior que 7 <strong>e</strong> 9 for igual a 9  </td>
    </tr>
        <tr>
      <td><code>||</code></td>
      <td>Ou</td>
      <td><code>( 10 &gt; 7 ) || ( 9 == 9 )</code></td>
      <td>Verdadeiro se 10 for maior que 7 <strong>ou</strong> 9 for igual a 9</td>
    </tr>
  </tbody>
</table>
<p>Veja um exemplo com  cada um dos operadores, e como nos operadores de comparação utilizaremos a  função <code>var_dump()</code>, para retornar o resultado.</p>
<pre class="brush: php;">
&lt;?php
/**
 * AND
 */
var_dump(  7 == 7  AND 9 &gt; 7  ); // TRUE, ambas as expressões são verdadeiras

var_dump(  7 == 7  AND 9 &lt; 7  ); // FALSE, apenas a primeira expressão é verdadeira

/**
 *  OR
 */
var_dump(  7 == 7  OR 9 &gt; 7  ); // TRUE, ambas as expressões são verdadeiras

var_dump(  7 != 7  OR 9 &gt; 7  ); // TRUE, a segunda expressão é verdadeira

var_dump(  7 != 7  OR 9 &lt; 7  ); // FALSE, ambas as expressões são falsas

/**
 * XOR
 */
var_dump(  7 == 7  XOR 9 &gt; 7  ); // FALSE, ambas as expressões são verdadeiras

var_dump(  7 == 7  XOR 9 &lt; 7  ); // TRUE, a primeira expressão é verdadeira

var_dump(  7 &lt; 7  XOR 9 &gt; 7  ); // TRUE, a segunda expressão é verdadeira

/**
 * !
 */
var_dump(  ! 9 &lt; 7  ); // TRUE, 9 NÃO é menor que 7

var_dump(  ! 9 &gt; 7  ); // FALSE, 9 é maior que 7

/**
 * &amp;&amp;
 */
var_dump(  7 == 7  &amp;&amp; 9 &gt; 7  ); // TRUE, ambas as expressões são verdadeiras

var_dump(  7 == 7  &amp;&amp; 9 &lt; 7  ); // FALSE, apenas a primeira expressão é verdadeira

/**
 *  ||
 */
var_dump(  7 == 7  || 9 &gt; 7  ); // TRUE, ambas as expressões são verdadeiras

var_dump(  7 != 7  || 9 &gt; 7  ); // TRUE, a segunda expressão é verdadeira

var_dump(  7 != 7  || 9 &lt; 7  ); // FALSE, ambas as expressões são falsas

?&gt;
</pre>
<p>Novamente não  utilizamos variáveis por questões didáticas, as mesmas regras dos tipos de  dados em operadores de comparação são validas aqui. Experimente agora que já  sabe utilizar variáveis, ao invés de valores como inserirmos experimente substituir por variáveis.</p>
<h2>Precedência de operadores no PHP</h2>
<p>Agora você já  conhece uma boa quantidade de <a href="/artigo/operadores-no-php">operadores no PHP</a> temos que conhecer a precedência, ou seja,  quem é mais importante qual operador é avaliado primeiro e qual é avaliado em  seguida. Observe o seguinte exemplo:</p>
<pre class="brush: php;">
&lt;?php

echo 5 + 2 * 3;

?&gt;
</pre>
<p>O resultado será <strong>11</strong>, pois o operador <code>*</code> tem maior  precedência em relação ao operador <code>+</code>. Caso desejar realizar a operação com o operador <code>+</code> para só em seguida realizar a operação com o operador <code>*</code>. Observe o  exemplo:</p>
<pre class="brush: php;">
&lt;?php

echo (5 + 2) * 3;

?&gt;
</pre>
<p>Observe que  utilizamos os parênteses para determinarmos quem deve ser executado primeiro,  assim alterando o resultado para <strong>21</strong>.</p>
<p>A tabela seguinte mostra a precedência dos  operadores, da maior precedência no começo para os de menor precedência.</p>
<table>
  <thead>
    <tr>
      <th>Operador</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>- ! ++ --</code></td>
      <td>Negativo, negação, incremento e decremento</td>
    </tr>
        <tr>
      <td><code>* / %</code></td>
      <td>Multiplicação, divisão e resto da divisão</td>
    </tr>
        <tr>
      <td><code>+ - .</code></td>
      <td>Adição, subtração e concatenação</td>
    </tr>
        <tr>
      <td><code>&gt;  &lt;  &gt;= &lt;=</code></td>
      <td>Maior que, menor que, maior ou igual e menor ou igual</td>
    </tr>
        <tr>
      <td><code>== != &lt;&gt;</code></td>
      <td>Igual e diferente</td>
    </tr>
        <tr>
      <td><code>&amp;&amp;</code></td>
      <td>E</td>
    </tr>
        <tr>
      <td><code>||</code></td>
      <td>Ou</td>
    </tr>
        <tr>
      <td><code>= += -= *= /= %=</code></td>
      <td>Operadores de atribuição</td>
    </tr>
        <tr>
      <td><code>AND</code></td>
      <td>E com menor prioridade</td>
    </tr>
        <tr>
      <td><code>XOR</code></td>
      <td>Ou exclusivo</td>
    </tr>
        <tr>
      <td><code>OR</code></td>
      <td>Ou com menor prioridade</td>
    </tr>
  </tbody>
</table>
<p>É importante lembrar que primeiro o PHP executará todas as  operações que estiverem entre parênteses, se dentro dos parênteses houver  diversas operações a precedência dos operadores será utilizada para definir a  ordem, após resolver todas as operações dos parentes, o PHP volta a resolver o  que esta fora dos parênteses baseando-se na tabela de precedência de  operadores, havendo operadores de mesma prioridade o PHP resolverá a operação  da esquerda para direita. Uma tabela mais completa, pois aqui exibimos apenas  dos operadores que aprendemos, pode ser encontrada diretamente no <a href="http://www.php.net/manual/pt_BR/language.operators.precedence.php">manual do PHP</a>.</p>
<div class="destaque">
  <p>Abordamos os operadores de comparação e lógicos além da precedência dos operadores neste artigo, no artigo seguinte sobre estruturas de controle serão bastante utilizados os temas abordados neste artigo por isso sempre que houver necessidade volte para tirar duvida sobre algo.</p>
</div>