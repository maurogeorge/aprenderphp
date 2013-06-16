---
layout: post
title: Laços de repetição while e do while no PHP
meta_description: Descubra a funcionalidade do switch uma poderosa estrutura de controle no PHP, aprenda sobre o operador ternário e entenda o que ele tem a ver com as já conhecidas estruturas de controle if e else.
meta_keywords: php, while, do-while, laços, lacos, repetição, repeticao
summary: Entenda o que são os laços de repetições através do while e do-while no PHP, além de saber  diferenciar o while para o do-while.
tags: [Operadores, Algoritmo, Estruturas de controle]
---
<h2>Introdução</h2>
<p>Quando for  necessário efetuar a repetição de um trecho de um programa um determinado  número de vezes o que você faria? Escreveria de novo? Copiaria e colaria? Bem  feio né? Afinal estamos utilizando de maquinas que são feitas para trabalhar  para nos e não o contrario. Quando encontrarmos um problema como o apresentado  anteriormente temos os laços de repetição, também conhecidos como loopings ou  laços malhas de repetição que poderão nos ajudar. Vamos a um problema para  tentarmos resolver:</p>
<h2>Problema</h2>
<p>Bart Simpson ficou  novamente na detenção no final da aula. E como punição terá que escrever:  “Estou aprendendo loopings no Aprender PHP” 100 vezes no quadro, ou no nosso  caso na tela.</p>
<p>Com o conhecimento  que aprendemos até aqui faríamos algo como:</p>
<pre class="brush: php;">
&lt;?php

$mensagem = "Estou aprendendo loopings no Aprender PHP";

echo $mensagem . '&lt;br /&gt;' . PHP_EOL ;
echo $mensagem . '&lt;br /&gt;' . PHP_EOL ;
echo $mensagem . '&lt;br /&gt;' . PHP_EOL ;

?&gt;
</pre>
<p>Até repetirmos 100 vezes. O que não é muito inteligente né?  Vamos conhecer agora a nossa primeira estrutura de repetição, o while.</p>
<h2>O while no PHP</h2>
<p>O while executa um  teste lógico, que retorne verdadeiro ou falso, no inicio do looping para  verificar se é permitido ou não executar as instruções. Traduzindo while para  português obtemos “enquanto” sendo assim as instruções serão executadas  enquanto o teste do looping for considerado verdadeiro.</p>
<p>A estrutura while  tem seu funcionamento controlado por decisões podendo executar um determinado  conjunto de instruções enquanto a condição for verdadeira (<code>True</code>) e no momento  em que a condição for avaliada como falsa (<code>False</code>) o processamento da rotina é  desviado para fora do looping. Se desde o inicio a condição for tratada como  falsa o looping não será executado.</p>
<h3>Diagrama de blocos</h3>
<p>Observe como seria  a representação do problema de Bart Simpson utilizando o while.</p>
<p class="center">
  <img alt="Diagrama de blocos do while no php" src="/img/artigos/lacos-de-repeticao-while-e-do-while-no-php/diagrama-de-blocos-do-while-no-php.jpg" />
</p>
<p>Não temos nenhum  símbolo novo no nosso <a href="/artigo/o-algoritmo-o-diagrama-de-blocos-e-o-php">diagrama</a>. Iniciamos  com 2 blocos de processamento de dados, um para o criarmos a mensagem e outro  para criar o contador, <code>$i</code>, saberá mais sobre o contador abaixo. Em seguida  criamos um <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">símbolo de decisão, o losango</a>. Se contador for menor que 100 o bloco  dentro do looping será executado que consiste em imprimir os dados na tela e  incrementar em 1 o contador e voltar ao inicio do looping. Quando o contador  for maior que 100 encerrasse o looping.</p>
<h3>No PHP</h3>
<p>Observe como  ficaria a representação em PHP da nossa estrutura while para resolver o  problema de Bart Simpson. E como Bart demorou muito ele ainda teve que numerar  para termos certeza que ele escreveu às 100 vezes. Observe o código:</p>
<pre class="brush: php;">
&lt;?php

$mensagem = "Estou aprendendo loopings no Aprender PHP";

$i = 1;
while( $i &lt;= 100 ){
  echo $i . ' - ' .$mensagem . '&lt;br /&gt;' . PHP_EOL ;
  $i++;
}

?&gt;
</pre>
<p>Iniciamos  atribuindo um valor a <a href="/artigo/comecando-a-programar-em-php">variável</a> mensagem em seguida criamos uma variável <code>$i</code> que é conhecida como  contador ou sentinela. Logo abaixo de nosso contador iniciamos o while que  avalia se <code>$i</code> é menor que 100, se for verdadeiro ele executa a instrução se não  ele sai do looping. A primeira volta de nosso looping a instrução é verdadeira  então dentro do looping escrevemos a mensagem e somamos mais 1 a variável <code>$i</code>  com o operador de <a href="/artigo/operadores-no-php">pós incremento</a>.  Após terminar isto o looping volta e avalia <code>$i</code> aqui com o valor de 2 e se for  verdadeira a expressão do while inicia tudo novamente.</p>
<p>Você sabe o porquê do <code>$i</code> no nosso looping? A  utilidade dele ali é fazer em um momento a expressão se tornar falsa senão  teremos um looping infinito. Como o nosso while avalia se <code>$i</code> é menor que 100 se  sempre ele for menor que 100 o looping nunca parará, por isso que temos que incrementá-lo  para poder uma hora ele chegar ao valor em que a instrução se tornará falsa.  Observe o código em que não incrementamos o <code>$i</code> antes de sairmos do looping.  Execute e rapidamente pause a execução do browser, pois como isto nunca terá  fim seu browser vai ir ficando bem lento e podendo até travar. Se não quiser  testar o resultado será “1 - Estou aprendendo loopings no Aprender PHP”  infinitamente um por linha.</p>
<pre class="brush: php;">
&lt;?php

$mensagem = "Estou aprendendo loopings no Aprender PHP";

$i = 1;
while( $i &lt;= 100 ){
  echo $i . ' - ' .$mensagem . '&lt;br /&gt;' . PHP_EOL ;
}

?&gt;
</pre>
<p>Observe agora o  mesmo exemplo de Bart Simpson escrevendo de 1 a 100, no entanto agora ele  escrevendo os números em ordem decrescente.</p>
<pre class="brush: php;">
&lt;?php

$mensagem = "Estou aprendendo loopings no Aprender PHP";

$i = 100;
while( $i &gt;= 1 ){
  echo $i . ' - ' .$mensagem . '&lt;br /&gt;' . PHP_EOL ;
  $i--;
}

?&gt;
</pre>
<p>Veja que alteramos  apenas a lógica agora iniciamos o <code>$i</code> com 100 e executamos o looping enquanto <code>$i</code>  for maior ou igual a 1 e a cada volta do looping diminuímos um para que em um  momento termos <code>$i</code> com o valor de 1 e encerrarmos o looping.</p>
<div class="dica">
    <p>Em relação à estrutura de controle while:</p>
    <ul>
        <li>A expressão a ser avaliada é declarada no inicio  do while</li>
        <li>Expressões são realizadas por <a href="/artigo/operadores-de-comparacao-operadores-logicos-e-a-precedencia-dos-operadores-no-php">operadores  lógicos e operadores de comparação</a></li>
        <li>O looping é executado enquanto a condição da  expressão for verdadeira (<code>True</code>)</li>
        <li>Quando  a condição da expressão for avaliada como falsa (<code>False</code>) o processamento da  rotina é desviado para fora do looping</li>
        <li>O bloco de código referente ao looping deve ser  delimitado por chaves {}</li>
        <li>Endente o código referente ao bloco em 4 espaços  por questões de legibilidade, a como configurar o seu editor de texto para  transformar Tabs em espaços</li>
        <li>Utilizamos um contador para o looping não ficar  um looping infinito</li>
        <li>Declara-se o contador <strong>fora</strong> do looping</li>
        <li>Não se esqueça de alterar o valor do contador  para não cairmos em um looping infinito.</li>
    </ul>
</div>
<h2>O do-while no PHP</h2>
<p>Bastante parecido com o while o do-while  caracteriza-se por uma estrutura que executa um teste lógico no fim do looping.  Tem seu funcionamento baseado em decisões assim como o while, no entanto <strong>pelo menos uma vez</strong> será executado o  conjunto de instruções, pois a condição da validade, verdadeiro ou falso, é  avaliado no final.</p>
<h2>Problema</h2>
<p>Continuaremos o mesmo problema de Bart Simpson, no entanto  agora utilizando o do-while.</p>
<h3>Diagrama de blocos</h3>
<p>Veja como seria a  representação do mesmo problema de Bart, no entanto agora utilizando o  do-while.</p>
<p class="center">
  <img alt="Diagrama de blocos do do-while no php" src="/img/artigos/lacos-de-repeticao-while-e-do-while-no-php/diagrama-de-blocos-do-do-while-no-php.jpg" />
</p>
<p>Basicamente o mesmo  diagrama de blocos do feito anteriormente para o while, no entanto observe que  a expressão é avaliada no final, se for verdadeira a expressão escrevemos a  mensagem e incrementamos em 1 o contador se for falsa saímos do looping.</p>
<h3>No PHP</h3>
<p>Observe como  ficaria a representação em PHP da solução do problema de Bart Simpson agora com  o uso do do-while.</p>
<pre class="brush: php;">
&lt;?php

$mensagem = "Estou aprendendo loopings no Aprender PHP";

$i = 1;

do {
  echo $i . ' - ' .$mensagem . '&lt;br /&gt;' . PHP_EOL ;
  $i++;
} while( $i &lt;= 100 );

?&gt;
</pre>
<p>Você observou que  temos todos os elementos que tínhamos no while né? O contador, incrementar o  contador, uma expressão. No entanto agora temos o “do” que quer dizer que pelo  menos uma vez será executado mesmo que a condição na expressão seja avaliada  como falsa, lembrando que assim como o while o do-while é executado enquanto a  expressão for verdadeira, observe abaixo onde Bart muito esperto alterou seu  contador para dizer ao diretor que já havia escrito 150 vezes.</p>
<pre class="brush: php;">
&lt;?php

$mensagem = "Estou aprendendo loopings no Aprender PHP";

$i = 150;

do {
  echo $i . ' - ' .$mensagem . '&lt;br /&gt;' . PHP_EOL ;
  $i++;
} while( $i &lt;= 100 );

?>
</pre>
<p>Veja que mesmo a  expressão sendo falsa, 150 não é menor nem igual a 100, o looping foi executado  pelo menos uma vez, pois a avaliação da expressão é feita no final. Agora veja  com o while o que ocorreria.</p>
<pre class="brush: php;">
&lt;?php

$mensagem = "Estou aprendendo loopings no Aprender PHP";

$i = 150;

while ( $i &lt;= 100 ) {
  echo $i . ' - ' .$mensagem . '&lt;br /&gt;' . PHP_EOL ;
  $i++;
}

?&gt;
</pre>
<p>Como no while a expressão é avaliada no começo, o looping  não foi executado nenhuma vez.  Já no  do-while como a expressão só é avaliada no final pelo menos uma vez o looping  será executado.</p>
<div class="dica">
    <p>Em relação à estrutura de controle do- while:</p>
    <ul>
        <li>A expressão a ser avaliada é declarada no final  do do-while</li>
        <li>É garantido que pelo menos uma vez o looping  será executado devido à dica anterior</li>
        <li>Expressões são realizadas por <a href="/artigo/operadores-de-comparacao-operadores-logicos-e-a-precedencia-dos-operadores-no-php">operadores  lógicos e operadores de comparação</a></li>
        <li>O looping é executado enquanto a condição da  expressão for verdadeira (True)</li>
        <li>Quando  a condição da expressão for avaliada como falsa (False) o processamento da  rotina é desviado para fora do looping</li>
        <li>O bloco de código referente ao looping deve ser  delimitado por chaves {}</li>
        <li>Endente o código referente ao bloco em 4 espaços  por questões de legibilidade, a como configurar o seu editor de texto para  transformar Tabs em espaços</li>
        <li>Utilizamos um contador para o looping não ficar  um looping infinito</li>
        <li>Declara-se o contador <strong>fora</strong> do looping</li>
        <li>Não se esqueça de alterar o valor do contador  para não cairmos em um looping infinito.</li>
    </ul>
</div>