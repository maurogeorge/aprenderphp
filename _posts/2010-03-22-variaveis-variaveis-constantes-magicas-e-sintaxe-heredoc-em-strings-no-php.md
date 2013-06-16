---
layout: post
title: Variáveis variáveis, constantes mágicas e sintaxe heredoc em strings no PHP
meta_description: Entenda o que são variáveis variáveis e aprenda a utiliza-las em prática, conheça também as constantes mágicas e veja a sua utilização e descubra mais um modo de declarar as suas strings com a declaração de sintaxe heredoc em strings no PHP.
meta_keywords: PHP, variavel, variáveis variáveis, constantes mágicas, sintaxe heredoc, strings, constantes
summary: Entenda o que são variáveis variáveis e aprenda a utiliza-las em prática, conheça também as constantes mágicas e veja a sua utilização e descubra mais um modo de declarar as suas strings com a declaração de sintaxe heredoc em strings no PHP.
tags: [Variável, Constantes, String]
---
<p>Agora que já possui certo conhecimento em variáveis, tipos  de dados e em alguns operadores iremos nos aprofundar um pouco mais em alguns  itens antes de entrarmos nas estruturas de controle.</p>
<h2>Variáveis variáveis, variáveis dinâmicas ou ainda variáveis criadas durante  a execução no PHP</h2>
<p>Independente do nome que encontrar por aí em livros ou mesmo  pela internet, é um recurso que nos permite a criação de uma variável através  do conteúdo de outra variável.</p>
<p>Para criar uma variável variável utiliza-se de uma variável  para servir de identificador para outra que é criada. Para isso utiliza-se duas  vezes o símbolo de <code>$</code>, ou seja,  devemos utilizar <code>$$</code>. Veja no exemplo a seguir.</p>
<pre class="brush: php;">
&lt;?php

// Declarando o valor da variável $a
$a = 'nome';

/**
 * Criamos $$a, que como possui dois $
 * também pode ser chamada pelo valor da
 * variável $a ou seja "nome"
 */
$$a = 'Mauro';

// Exibo $a e $nome que foi criada dinâmicamente
echo $a . ' : ' . $nome;

?&gt;
</pre>
<p>Como você pode ver no exemplo podemos criar a variável a  partir do valor de outra variável. O contrário também é válido ao invés de  criarmos a variável, em nosso caso, <code>$nome</code> dinamicamente definimos seu valor  normalmente no entanto quando formos exibir seu resultado em tela podemos  acessar seu valor através de <code>$$a</code>, lembrando que para que isto funcione <code>$a</code> deve  possuir o mesmo valor da variável que será criada em nosso caso “nome”. Observe  o exemplo:</p>
<pre class="brush: php;">
&lt;?php

// Declarando o valor da variável $a
$a = 'nome';

/**
 * Criamos $nome, que é
 * o mesmo valor de $a em
 * sua declaração
 */
$nome = 'Mauro';

/**
 *  Exibo $a e $$a que foi criada
 *  dinâmicamente e é o equivalente a acessar
 *  a variável $nome
 */
echo $a . ' : ' . $$a;

?&gt;
</pre>
<h2>Constantes Mágicas no PHP</h2>
<p>O PHP fornece um grande número de <a href="http://www.php.net/manual/pt_BR/reserved.constants.php">constantes predefinidas</a>. Entretanto a maioria dessas constantes são criadas por várias extensões, e somente estarão presentes quando essas extensões estiverem disponíveis. <a href="http://www.php.net/manual/pt_BR/reserved.constants.php">Aqui  você pode ver as constantes predefinidas</a>, lembrando que para visualizar seu conteúdo apenas seguindo a regra de que elas são dependentes de extensões.</p>
<p>As constantes mágicas não possuem dependências, no entanto seus valores mudam dependendo de onde elas são executadas. Veja uma tabela com  as 7 constantes mágicas que o PHP possui:</p>
<table>
  <thead>
    <tr>
      <th>Constante</th>
      <th>Valor retornado</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>__LINE__</code></td>
      <td>A linha atual do script.</td>
    </tr>
    <tr>
      <td><code>__FILE__</code></td>
      <td>O caminho completo e nome do arquivo.</td>
    </tr>
    <tr>
      <td><code>__DIR__</code></td>
      <td>O diretório do arquivo.</td>
    </tr>
    <tr>
      <td><code>__FUNCTION__</code></td>
      <td>O nome da função.</td>
    </tr>
    <tr>
      <td><code>__CLASS__</code></td>
      <td>O nome da classe.</td>
    </tr>
    <tr>
      <td><code>__METHOD__</code></td>
      <td>O nome do método de classe.</td>
    </tr>
    <tr>
      <td><code>__NAMESPACE__</code></td>
      <td>O nome do atual namespace.</td>
    </tr>
  </tbody>
</table>
<p>Veja um exemplo do valor retornado pelas constantes mágicas:</p>
<pre class="brush: php;">
&lt;?php

echo __LINE__ . '&lt;br /&gt;' . PHP_EOL;

echo __FILE__ . '&lt;br /&gt;' . PHP_EOL;

echo __DIR__ . '&lt;br /&gt;' . PHP_EOL;

echo __LINE__;

?&gt;
</pre>
<div class="destaque">
  <p>Utilizamos apenas as constantes mágicas no escopo do nosso  aprendizado, ou seja, não executamos a constante mágica equivalente a funções (<code>__FUNCTION__</code>)  e nem as equivalentes a classes (<code>__CLASS__</code>, <code>__METHOD__</code>, <code>__NAMESPACE__</code>).<br />
  Com o avançar de nossos estudos ao nos  aprofundarmos em funções, classes e objetos você será capaz de ver o resultado  do uso destas constantes mágicas.</p>
</div>
<h2>Sintaxe Heredoc em strings no PHP</h2>
<p>Agora que já esta familiarizado em como <a href="/artigo/tipos-de-dados-no-php#string">declarar strings</a>, com aspas simples e aspas duplas, iremos aprender um novo modo de  declarar strings, a <a href="http://www.php.net/manual/pt_BR/language.types.string.php#language.types.string.syntax.heredoc">sintaxe  heredoc</a>.</p>
<p>Para declararmos uma string com a sintaxe heredoc utiliza-se primeiro <code>&lt;&lt;&lt;</code> (três sinais de menor) e em seguida definimos o  delimitador, aí definimos o texto contido na string, em seguida finalizamos a  string com o delimitador. Veja um exemplo:</p>
<pre class="brush: php;">
&lt;?php

$texto = &lt;&lt;&lt;EOT

Eu sou uma string declarada com a sintaxe heredoc.

EOT;

echo $texto;

?&gt;
</pre>
<div class="observacao">
  <ul>
    <li>O delimitador, no nosso caso <code>EOT</code>, tem que ser  iniciados apenas com uma letra ou <code>_</code> (sublinhado) e podem ser seguido de letras  ou algarismos, ou seja, números podem aparecer em outras posições exceto na  primeira</li>
    <li>Assim como na declaração de variáveis nunca  utilize caracteres especiais em nome do delimitador como acentos (é í ó)  cedilha (ç)</li>
    <li>O delimitador final não deve ser acompanhado de  nenhum outro caractere, exceto o ponto e vírgula</li>
    <li>O delimitador final deve ser iniciado no inicio  da linha sem tabulações ou espaço, por isso <strong>nunca o endente</strong>.</li>
    <li>Resumindo o delimitador final não deve conter  nada antes e nem depois do delimitador final, exceto o ponto e vírgula após sua declaração.</li>
  </ul>
</div>
<p>Veja um exemplo de como estaríamos declarando de forma errada uma string com a sintaxe heredoc.</p>
<pre class="brush: php;">
&lt;?php

$texto = <<<7ÉOT

Eu sou uma string declarada com a sintaxe heredoc.

    7éOT; echo $texto;

?&gt;
</pre>
<p>No exemplo temos todos os erros possíveis como:</p>
<ul>
  <li>iniciar a string com caractere <strong>não</strong> alfanumérico ou underline</li>
  <li>utilizar caractere especial no nome do delimitador</li>
  <li>edentar o delimitador final</li>
  <li>definir o delimitador final, diferente do de  abertura, no exemplo o caractere “é” maiúsculo e minúsculo.</li>
  <li>Tentar escrever algo na mesma linha após o delimitador final.</li>
</ul>
<p>As strings declaradas como heredoc se comportam como as aspas duplas, exceto que você não precisa utilizar os caracteres de escape para  definir a <strong>aspas simples</strong> e as <strong>aspas duplas</strong>. E como as strings  declaradas com aspas duplas elas <strong>interpretam  as variáveis</strong> veja um exemplo:</p>
<pre class="brush: php;">
&lt;?php

$nome = 'Mauro George';

$texto = &lt;&lt;&lt;PHP

Eu me chamo {$nome}, como esta string está declarada como Heredoc eu posso exibir " e ' também sem escapar.

PHP;

echo $texto;

?&gt;
</pre>
<p>Observe que além de exibir as aspas simples e duplas sem necessitar escapar ainda pude exibir o valor de minha variável.</p>
<div class="dica">
  <p>Utilize  sempre colchetes envolvendo uma variável, como no exemplo anterior, quando ela  for interpretada dentro de outra variável, ou seja na <strong>declaração de string como heredoc</strong> e na <strong>declaração de strings com aspas duplas</strong>.</p>
</div>