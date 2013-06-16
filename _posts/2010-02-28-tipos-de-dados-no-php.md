---
layout: post
title: Tipos de dados no PHP
meta_description: Conheça os diferentes tipos de dados suportados pelo PHP, os quatro tipos básicos, os dados escalares integer, float , string e boolean. Os tipos compostos array e object e os dois tipos especiais resource e NULL.
meta_keywords: Tipos de dados, Integer, Float, String, Boolean, NULL, array, object
summary: Conheça os diferentes tipos de dados suportados pelo PHP, os quatro tipos básicos, os dados escalares integer, float , string e boolean. Os tipos compostos array e object e os dois tipos especiais resource e NULL.
tags: [Tipos de dados, Integer, Float, String, Boolean, NULL]
---
<h2>Introdução aos tipos de dados no PHP</h2>
<p>Agora que você já sabe como criar variáveis e constantes no  PHP, e sabe exibir os dados no browser iremos nos aprofundar-nos diferentes  tipos de dados suportados pelo PHP.</p>
<div class="dica">
  <p>Caso  você já tenha programado em outra linguagem como C, deve achar estranho não ser  necessário a declaração de uma variável, no PHP basta-lhe atribuir um valor  diretamente, pois é decidido em tempo de execução pelo PHP, dependendo do  contexto na qual a variável é usada.</p>
</div>

<h2>Diferentes tipos de dados suportados pelo PHP</h2>
<p>O PHP suporta oito tipos de dados primitivos divididos em  três grupos:</p>
<ol>
  <li>Quatro tipos básicos, os dados escalares
    <ul>
      <li><a href="#integer">integer</a></li>
      <li><a href="#float">float (número de ponto flutuante, ou também  double)</a></li>
      <li><a href="#string">string</a></li>
      <li><a href="#boolean">boolean</a></li>
    </ul>
  </li>
  <li>Dois tipos compostos
    <ul>
      <li>array</li>
      <li>object</li>
    </ul>
  </li>
  <li>Dois tipos especiais:
    <ul>
      <li>resource</li>
      <li><a href="#null">NULL</a></li>
    </ul>
  </li>
</ol>

<h2 id="integer">O tipo integer, inteiro, no PHP</h2>
<p>Um <a href="http://pt.wikipedia.org/wiki/Inteiro">inteiro</a> é qualquer numero sem decimais, positivou ou negativo. Englobando todos os  números do conjunto Z(os números inteiros).</p>
<pre class="brush: php; html-script: true">
&lt;?php

// Declaração de uma variavel como inteiro
$ano_nascimento = 1989;

?>
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;Tipo Inteiro no PHP&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;Eu nasci no ano de &lt;?php echo $ano_nascimento; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<h2 id="float">O tipo float ou double, número de ponto flutuante, no PHP</h2>
<p>Float, Double ou ainda números de ponto flutuante são os <a href="http://pt.wikipedia.org/wiki/N%C3%BAmeros_reais">números reais</a>.</p>
<pre class="brush: php; html-script: true">
&lt;?php

// Declaração de uma variavel como float, armazenando o valor de pi
$pi = 3.14159265;

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;Tipo float, double ou número de ponto flutuante no PHP&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;O valor de pi é &lt;?php echo $pi; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<h2 id="string">O tipo string no PHP</h2>
<p>Uma string é uma série de caracteres, um texto por exemplo.  Para declararmos strings podemos utilizar as <strong>aspas simples (apóstrofos)</strong> e as <strong>aspas duplas</strong>.</p>
<h3>String com aspas simples (apóstrofos) no PHP</h3>
<p>Para definirmos uma string com aspas simples basta  delimitarmos o texto com aspas simples (<code>'</code>).</p>
<pre class="brush: php; html-script: true">
&lt;?php

// Declaração de uma variavel com string com aspas simples
$texto = 'O PHP é uma linguagem server-side.';

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;String com aspas simples no PHP&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;&lt;?php echo $texto; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<p>Agora uma pergunta. E se eu quiser definir uma aspa simples  no meu texto o que farei? Já que as aspas simples são os delimitadores de  string. Veja o exemplo do que acontece se eu apenas inserir uma aspa simples no  meio da minha string.</p>
<pre class="brush: php; html-script: true">
&lt;?php

// Declaração de uma variavel com string com aspas simples
$texto = 'Ele comprou uma pizza no Joey's.';

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;String com aspas simples no PHP&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;&lt;?php echo $texto; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<p>Sim! Como você deve ter imaginado foi gerado um erro já que a aspa simples é o delimitador de string. Para especificar uma aspa simples (apóstrofo) no meio de  uma string você precisará &quot;escapá-la&quot; com uma contra barra (<code>\</code>)  veja a seguir.</p>
<pre class="brush: php; html-script: true">
&lt;?php

// Declaração de uma variavel com string com aspas simples
$texto = 'Ele comprou uma pizza no Joey\'s.';

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;String com aspas simples no PHP&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;&lt;?php echo $texto; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<h3>String com aspas duplas no PHP</h3>
<p>A grande diferença entre as strings declaradas com aspas  simples e as declaradas com aspas duplas está no fato de que as strings declaradas com aspas duplas <strong>interpretam  as variáveis</strong>.</p>
<pre class="brush: php; html-script: true">
&lt;?php
// Declaração de um produto
$produto = 'pizza';
// Declaração de uma variavel com string com aspas duplas
$texto = "Ele \"comprou\" uma $produto no Joey's.";

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;String com aspas duplas no PHP&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;&lt;?php echo $texto; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<p>Observe que a variável <code>$produto</code> foi interpretada dentro da  string declarada na variável <code>$texto</code>. Coisa que <strong>não ocorre nas variáveis declaradas com aspas simples</strong>. Veja o  exemplo a seguir:</p>
<pre class="brush: php; html-script: true">
&lt;?php
// Declaração de um produto
$produto = 'pizza';
// Declaração de uma variavel com string com aspas duplas
$texto = 'Ele comprou uma $produto no Joey\'s.';

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;String com aspas duplas no PHP&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;&lt;?php echo $texto; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<div class="observacao">
  <p>Assim  como tivemos que inserir uma contra barra (<code>\</code>) para declarar uma aspa  simples quando declaramos uma string entre aspas simples devemos utilizar o  mesmo caractere de escape, contra barra (<code>\</code>), para podemos inserir as  aspas duplas dentro de uma string declarada com aspas duplas.</p>
</div>
<p>Outra grande diferença entre as aspas simples e as aspas duplas é que temos uma sequência de caracteres de controle que podem ser  inserido em nossa string, veja a tabela a seguir:</p>
<table>
  <thead>
    <tr>
      <th>Seqüência</th>
      <th>Significado</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>\n</code></td>
      <td>fim de linha</td>
    </tr>
    <tr>
      <td><code>\r</code></td>
      <td>retorno de carro(carriage return)</td>
    </tr>
    <tr>
      <td><code>\t</code></td>
      <td>TAB horizontal</td>
    </tr>
    <tr>
      <td><code>\v</code></td>
      <td>TAB vertical</td>
    </tr>
    <tr>
      <td><code>\f</code></td>
      <td>form feed</td>
    </tr>
    <tr>
      <td><code>\\</code></td>
      <td>contra barra ou barra invertida</td>
    </tr>
    <tr>
      <td><code>\$</code></td>
      <td>sinal de cifrão</td>
    </tr>
    <tr>
      <td><code>\"</code></td>
      <td>Aspas</td>
    </tr>
  </tbody>
</table>
<p>Não fique preocupado em ter que decorar todas as seqüências  de caracteres de controle, pois a tabela estará aqui para quando você precisar  tirar uma duvida e a medida de sua necessidade você a ira decorando com o  passar do tempo. Veja um exemplo a seguir de alguns caracteres de controle em  seguida uma explicação sobre o exemplo:</p>
<pre class="brush: php; html-script: true">
&lt;?php
// Declaração de uma string com aspas simples mo PHP
$texto = 'Ele comprou uma
 pizza no Joey\'s e custou R$ 30,00 reais';

// Declaração de uma string com aspas duplas mo PHP
$texto2 = "Ele comprou uma \n pizza no Joey's e custou R$ 30,00 reais";

// Declaração de uma string com aspas duplas mo PHP, e utilizando a contra barra para escapar o $
$texto3 = "Você se lembra que existia aqui uma variavel de nome \$produto?";

// Repare que não precisei escapar a contra barra
$texto4 = "Não preciso escapar a \ ?";

// Aqui eu preciso
$texto5 = "O texto termina com \\";
?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;String com aspas duplas no PHP&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;&lt;?php echo $texto; ?&gt;&lt;/p&gt;
&lt;p&gt;&lt;?php echo $texto2; ?&gt;&lt;/p&gt;
&lt;p&gt;&lt;?php echo $texto3; ?&gt;&lt;/p&gt;
&lt;p&gt;&lt;?php echo $texto4; ?&gt;&lt;/p&gt;
&lt;p&gt;&lt;?php echo $texto5; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<p>Para visualizar o primeiro exemplo abra o código fonte da  página no seu browser e observe que os dois primeiros parágrafos apesar de  idênticos um foi declarado como string com aspas simples e o outro com aspas  duplas. No que foi declarado com aspas duplas repare que utilizamos o caractere  de controle <code>\n</code> para quebra linha enquanto no outro utilizamos uma quebra de  linha no próprio código fonte, é um exemplo apenas para ilustrar o  funcionamento do caractere de controle <code>\n</code>.</p>
<p>Você deve esta se perguntando como eu pude escrever o sinal de <code>$</code>, nas variáveis <code>$texto</code> e <code>$texto2</code>, normalmente se eu necessito utilizar o  caractere de controle. A resposta é que não a nenhum caractere seguido dele. Na  variável <code>$texto3</code> como a texto seguido do <code>$</code> aí sim eu deve utilizar o caractere de controle.</p>
<p>Algo parecido ocorre com a contra barra observe que na  variável <code>$texto4</code> eu não precisei escapar a contra barra, a contra barra só  precisa ser escapa no final da string assim como foi declarado na variável <code>$texto5</code>.</p>
<div class="observacao">
  <p>Caso já tenha pego algum script pela internet em PHP, talvez já tenha se deparado com <code>\r\n</code> para finalizar a linha, ou apenas <code>\n</code> no entanto <strong>não o faça</strong>. Prefira a constante do próprio PHP, PHP_EOL. Pois seu objetivo é exatamente este criar uma nova linha(new line) cross-plataforma  assim você não precisa se preocupar como é que é pra criar uma linha no Windows ou no Linux.</p>
</div>
<div class="dica">
  <p>Não  se esqueça que a sequência de caracteres de controle (escape) <strong>só é interpretada pelas strings declaradas  com aspas duplas</strong>, e que as variáveis também <strong>só são interpretadas em strings declaradas com aspas duplas</strong>.</p>
</div>
<div class="destaque">
  <p>Caso  você esteja sentindo falta da <a href="http://www.php.net/manual/pt_BR/language.types.string.php#language.types.string.syntax.heredoc">sintaxe  Heredoc</a> não se preocupe ela será abordada mais a frente, como o objetivo é  um passo a passo a idéia é você ir se acostumando com as sintaxes aqui apresentadas e mais pra frente alguns assuntos terão que ser retomados. Assim  você não sofrerá com uma grande quantidade de informação e pouco tempo de  absorção.</p>
</div>
<h2 id="boolean">O tipo boolean, booleano, no PHP</h2>
<p>O tipo booleano é muito simples pois aceita apenas os  valores <strong>verdadeiro(<code>TRUE</code>)</strong> ou <strong>falso(<code>FALSE</code>)</strong>.</p>
<pre class="brush: php;">
&lt;?php
// Declaração de uma variável booleana com o valor verdadeiro
$sim = TRUE;
// Declaração de uma variável booleana com o valor falso
$nao = FALSE;

?&gt;
</pre>
<p>Você deve ter reparado que não exibimos valores na tela,  isto porque o tipo booleano expressa um valor verdade (verdadeiro ou falso). Quando  chegarmos às estruturas de controle aí sim o valor booleano fará muito mais  sentido.</p>
<div class="dica">
  <p>O tipo booleano é case-insensitive, ou seja, não  diferencia maiúsculas de minúsculas. Isto é <code>true</code>, <code>TrUe</code> e <code>TRUE</code> são iguais assim  como <code>false</code>, <code>FaLsE</code> e <code>FALSE</code> são iguais.<br />
No entanto prefira sempre utilizar: <code>TRUE</code> e <code>FALSE</code> ou <code>true</code> e <code>false</code>.</p>
</div>
<h2 id="null">O tipo NULL no PHP</h2>
<p>Outro tipo de dado muito simples, o valor especial <code>NULL</code>,  representa que a variável não tem valor. <code>NULL</code> é o único valor possível do tipo <code>NULL</code>.</p>
<pre class="brush: php;">
&lt;?php
// Declaração de uma variável NULL
$nulo = NULL;

?&gt;
</pre>
<div class="dica">
  <p>O tipo <code>NULL</code> é case-insensitive, assim como o tipo booleano , ou seja, não  diferencia maiúsculas de minúsculas. Isto é <code>null</code>, <code>NulL</code> e <code>NULL</code> são iguais.<br />
No entanto prefira sempre utilizar: <code>NULL</code> ou <code>null</code>.</p>
</div>
<div class="destaque">
  <p>Você  deve ter reparado que não falamos dos tipos compostos (array e object) e do  tipo especial resource. Isso porque como a proposta de aprendizado é orientada  a PHP e algoritmos não a sentido me aprofundar nestes tipos de dados se você  ainda não sabe os operadores e as estruturas de controle, pois iria lhe confundir mais.<br />
Após falarmos sobre estruturas de controle retornaremos ao tipo array.</p>
</div>