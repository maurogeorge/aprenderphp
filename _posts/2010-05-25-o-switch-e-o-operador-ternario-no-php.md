---
layout: post
title: O switch e o operador ternário no PHP
meta_description: Descubra a funcionalidade do switch uma poderosa estrutura de controle no PHP, aprenda sobre o operador ternário e entenda o que ele tem a ver com as já conhecidas estruturas de controle if e else.
meta_keywords: switch, operador ternário, ? :, if, else, elseif, diagrama, diagrama de blocos, algoritmo, estruturas de controle
summary: Descubra a funcionalidade do switch uma poderosa estrutura de controle no PHP, aprenda sobre o operador ternário e entenda o que ele tem a ver com as já conhecidas estruturas de controle if e else.
tags: [Operadores, Algoritmo, Estruturas de controle]
---
<h2>O switch no PHP</h2>
<p>O switch funciona como uma série de <code>if</code> juntos, mais sobre as <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">estruturas de controle if, else e elseif</a> podem ser encontradas no artigo anterior, testando valores para uma  variável ou expressão. No entanto o switch trabalha basicamente com o <a href="/artigo/operadores-de-comparacao-operadores-logicos-e-a-precedencia-dos-operadores-no-php">operador de igualdade</a>. Então em casos que devemos testar se nossa variável, ou expressão, <strong>é igual</strong> a uma série de valores, o  <code>switch</code> é uma boa saída. Vamos agora ver um problema para entendermos melhor o <code>switch</code>.</p>
<h3>Problema</h3>
<p>Em um programa de televisão o expectador deve escolher números de 1 a 5 para um sorteio de prêmios, em que cada número representa um prêmio. Então faremos:</p>
<ol>
    <li>Ler a entrada, o número que o expectador  escolheu</li>
    <li>De acordo com o número que o expectador escolheu  retornar um prêmio</li>
    <li>Se escolher um numero que não seja de 1 a 5  retornar uma mensagem de erro.</li>
</ol>
<h3>O diagrama de blocos</h3>
<p>Observe como seria a representação do nosso problema no diagrama de blocos.</p>
<img src="/img/artigos/o-switch-e-o-operador-ternario-no-php/diagrama-de-blocos-do-switch.jpg" alt="Diagrama de blocos do switch" />
<p>O símbolo de início e entrada de dados não são  novidades afinal foram abordados no artigo sobre o <a href="/artigo/o-algoritmo-o-diagrama-de-blocos-e-o-php">algoritmo e diagrama de blocos no  PHP</a>, no entanto o  símbolo seguinte nos diz que iremos comparar o valor contido nele com os  símbolos de decisões seguintes. E como já foi falado no <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">artigo anterior</a> utilizamos as setas para indicar a direção do  processamento. Como você pode observar no diagrama será testado cada um dos  valores se não for verdadeiro o próximo será testado até o último, chegando no  ultimo se nem o último for verdadeiro executamos o default, equivalente a um <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">else</a>.</p>
<h3>No PHP</h3>
<p>O nosso problema poderia ser resolvido apenas  utilizando as <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">estruturas de controle if, else e elseif</a> que aprendemos no artigo anterior. Antes de  ver o código abaixo tente resolver o nosso problema apenas com as estruturas de  controle que aprendemos até este ponto. Conseguiu? Veja um exemplo de como  poderia ser resolvido utilizando apenas <code>if</code>, <code>else</code> e <code>elseif</code>:</p>
<pre class="brush: php;">
&lt;?php

/**
 * Entrada do número do expectador
 */
$numero = 3;

if ( $numero == 1 ){
  $mensagem = 'uma bicicleta';
} elseif ( $numero == 2 ) {
  $mensagem = '20 mil reais em barras de ouro';
} elseif ( $numero == 3 ) {
  $mensagem = 'uma casa';
} elseif ( $numero == 4 ) {
  $mensagem = 'um conjunto de panelas';
} elseif ( $numero == 5 ) {
  $mensagem = 'um carro zero';
} else {
  $mensagem = 'nada, infelizmente';
}

/**
 * Retornando a mensagem
 */
echo "Parabéns o seu prêmio foi: {$mensagem}" ;

?&gt;
</pre>
<p>Não foi muito difícil  de resolver né? No entanto observe o código comparamos sempre a variável <code>$numero</code> a um valor de 1 a 5 e retornávamos uma <code>$mensagem</code>, e se não fosse de 1 a  5 retornaríamos que ele não ganhou nada. Se estamos sempre comparando uma  variável, ou expressão se são iguais a uma série de valores talvez seja à hora  de trocarmos de estrutura de controle.</p>
<p>Ao utilizarmos o <code>switch</code> informamos a variável ou expressão que será testada em cada uma das  cláusulas (<code>case</code>) até que seja encontrada uma cláusula em que seja verdadeira.  Quando isto ocorre às instruções dentro do bloco de código da estrutura case é  executado até encontrar a instrução <code>break</code>, falaremos mais sobre <code>break</code> quando  chegarmos aos loops no PHP, se nenhuma cláusula for verdadeira a instrução <code>default</code> será executada.</p>
<pre class="brush: php;">
&lt;?php

/**
 * Entrada do número do expectador
 */
$numero = 3;

switch ( $numero ){
  case 1:
    $mensagem = 'uma bicicleta';
    break;
  case 2:
    $mensagem = '20 mil reais em barras de ouro';
    break;
  case 3:
    $mensagem = 'uma casa';
    break;
  case 4:
    $mensagem = 'um conjunto de panelas';
    break;
  case 5:
    $mensagem = 'um carro zero';
    break;
  default:
    $mensagem = 'nada, infelizmente';
}

/**
 * Retornando a mensagem
 */
echo "Parabéns o seu prêmio foi: {$mensagem}";

?&gt;
</pre>
<div class="observacao">
    <p>Voltaremos a falar  sobre a instrução <code>break</code> posteriormente, no entanto até este momento você só  deve ter em mente que se ela não for inserida seria como se não fechássemos a  instrução <code>case</code>. Observe o exemplo abaixo mesmo passando um valor e ele for  verdadeiro todas as expressões abaixo do valor escolhido são executadas e como  atribuímos um valor a variável o que prevalece é da ultima, o <code>default</code>, por este  motivo devemos sempre utilizar a instrução <code>break</code>.</p>
</div>
<pre class="brush: php;">
&lt;?php

/**
 * Entrada do número do expectador
 */
$numero = 3;

switch ( $numero ){
  case 1:
    $mensagem = 'uma bicicleta';
  case 2:
    $mensagem = '20 mil reais em barras de ouro';
  case 3:
    $mensagem = 'uma casa';
  case 4:
    $mensagem = 'um conjunto de panelas';
  case 5:
    $mensagem = 'um carro zero';
  default:
    $mensagem = 'nada, infelizmente';
}

/**
 * Retornando a mensagem
 */
echo "Parabéns o seu prêmio foi: {$mensagem}" ;

?&gt;
</pre>
<p>Agora que sabemos o porquê do <code>break</code>, podemos o aproveitar de uma maneira, por exemplo, se em nosso  problema caso a pessoa escolhesse 2 ou 3 o prêmio seria o mesmo. Poderíamos  apenas mudar o valor da variável mensagem para eles ficarem iguais, no entanto  estaríamos nos repetindo o que não é legal, pois sempre que tivéssemos que  alterar em um teríamos que lembrar de alterar no outro por isso. O melhor mesmo  é fazer da seguinte forma:</p>
<pre class="brush: php;">
&lt;?php

/**
 * Entrada do número do expectador
 */
$numero = 2;

switch ( $numero ){
  case 1:
    $mensagem = 'uma bicicleta';
    break;
  case 2:
  case 3:
    $mensagem = 'uma casa';
    break;
  case 4:
    $mensagem = 'um conjunto de panelas';
    break;
  case 5:
    $mensagem = 'um carro zero';
    break;
  default:
    $mensagem = 'nada, infelizmente';
}

/**
 * Retornando a mensagem
 */
echo "Parabéns o seu prêmio foi: {$mensagem}" ;

?&gt;
</pre>
<p>Como o valor que seria  mantido era o da cláusula 3 apenas retiramos as instruções da 2 e não colocamos <code>break</code> na cláusula 2 sendo assim ela seria a mesma que a 3 esta sim tendo a  instrução <code>break</code> como as demais.</p>
<div class="dica">
    <p>Em relação a estrutura  de controle switch:</p>
    <ul>
        <li>A variavel  ou expressão a ser avaliada é declarada no inicio do <code>switch</code></li>
        <li>Expressões  são realizadas por <a href="/artigo/operadores-de-comparacao-operadores-logicos-e-a-precedencia-dos-operadores-no-php">operadores lógicos e operadores de  comparação</a> </li>
        <li>O bloco de  código referente a estrutura de controle deve ser delimitado por chaves <code>{}</code></li>
        <li>Endente o código referente ao bloco em 4 espaços por questões de legibilidade, a como configurar o seu editor de texto para transformar Tabs em espaços</li>
        <li>Cada  cláusula (<code>case</code>) possui um valor a ser comparado e logo após o valor são  adicionado 2 pontos (<code>:</code>) dando inicio a clausula</li>
        <li>Após os 2  pontos o bloco de código que devera ser executado para aquela cláusula</li>
        <li>Finalizamos  a cláusula com o <code>break</code></li>
        <li>Caso  tenhamos 2 ou mais valores que executarão o mesmo bloco de código não definimos  o <code>break</code> apenas no ultimo em que for inserido o bloco de código, ver o exemplo  anterior</li>
        <li>Após todas  as cláusulas podemos adicionar uma cláusula <code>default</code> que será executada caso  todas as outras não tenham sido verdadeiras</li>
        <li>A cláusula  <code>default</code> não necessita de <code>break</code>, afinal ela é inserida após todas as outras</li>
    </ul>
</div>
<h2>Operador ternário</h2>
<p>O operador ternário basicamente é uma forma de  escrever uma instrução <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">if e else</a> em uma única linha.  Para utilizamos o operador ternário utilizamos o <code>?</code> e o <code>:</code>. Observe um exemplo utilizando <code>if</code> e <code>else</code>:</p>
<pre class="brush: php;">
&lt;?php

$resultado = 7.5;

if ( $resultado &gt; 7 ){
  echo 'Aprovado';
} else {
  echo 'Reprovado';
}

?&gt;
</pre>
<p>Um exemplo bem simples apenas para ilustrar, afinal <a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">if e else</a> já aprendemos.  Agora o mesmo código poderia ser transcrito com o operador ternário. Observe:</p>
<pre class="brush: php;">
&lt;?php

$resultado = 7.5;

echo $resultado &gt; 7 ? 'Aprovado' : 'Reprovado';

?&gt;
</pre>
<p>Resolvemos o mesmo  problema em apenas uma linha. O que vem seguido do <code>?</code> representa o <code>if</code> enquanto o <code>:</code> representa o <code>else</code>. Também podemos fazer atribuições utilizando o operador ternário. Observe:</p>
<pre class="brush: php;">
&lt;?php

$resultado = 7.5;

$mensagem = $resultado &gt; 7 ? 'Aprovado' : 'Reprovado';

echo $mensagem;

?&gt;
</pre>
<p>Agora a nossa variável <code>$mensagem</code> recebe o valor de acordo com o resultado utilizando do operador ternário.</p>
<div class="observacao">
    <p>Não utilize o operador  ternário para substituir sempre as estruturas<a href="/artigo/if-else-e-elseif-as-estruturas-de-controle-no-php">if e else</a>. O operador ternário deve ser utilizado quando  o retorno e a lógica implementada for algo pequeno.  Por isso cabe ao desenvolvedor analisar se  vale a pena substituir uma instrução <code>if</code> e <code>else</code> por um operador ternário ou vice e versa. Pense na legibilidade, pois seu código pode ser lido futuramente por  outra pessoa na situação o que seria mais fácil de ler?</p>
</div>
<div class="dica">
    <p>Em relação ao operador  ternário:</p>
    <ul>
        <li>Equivale a  um <code>if</code> e <code>else</code>. No entanto seu uso deve ser ponderado como pode ser lido  anteriormente.</li>
        <li>A  expressão a ser avaliada é declarada no inicio do operador</li>
        <li>O <code>?</code> inicia  o bloco que pode ser lido como o <code>if</code></li>
        <li>O <code>:</code> inicia  o bloco que pode ser lido como <code>else</code>.</li>
        <li>O valor  retornado pode ser atribuído a uma variável.</li>
    </ul>
</div>