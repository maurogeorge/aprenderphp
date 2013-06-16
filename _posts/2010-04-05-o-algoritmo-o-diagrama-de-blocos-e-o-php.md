---
layout: post
title: O Algoritmo, o diagrama de blocos e o PHP
meta_description: Aprenda um pouco sobre os algoritmos, o diagrama de blocos e descubra o que isto tem a ver com o PHP
meta_keywords: PHP, algoritmo, entrada, processamento, saída de dados, diagrama de blocos
summary: Aprenda um pouco sobre os algoritmos, o diagrama de blocos e descubra o que isto tem a ver com o PHP
tags: [Variável, Operadores, Operadores aritméticos, Operadores de Atribuição, Algoritmo]
---
<h2>Algoritmo</h2>
<p>O <a href="http://pt.wikipedia.org/wiki/Algoritmo">algoritmo</a> é um processo de resolução de problemas bem definido e sem ambigüidade. É a  lógica em que aplicamos para resolvermos nossos problemas.</p>
<h2>Entrada, processamento e saída de dados</h2>
<p>Para se fazer um programa é preciso ter em mente três  pontos: a <strong>entrada</strong>, o <strong>processamento</strong> e a <strong>saída de dados</strong>. Temos que saber também se um dado for inserido  errado resultará em erro.</p>
<h3>Entrada de dados</h3>
<p>Em nossos estudos trabalharemos em que a entrada de dados  será as variáveis iniciais que definirmos em nosso script. Pois podemos ter  entrada de dados de diferentes fontes como modem, leitor ótico, cd etc.</p>
<h3>Processamento de dados</h3>
<p>Será onde ocorrerá à lógica, o processamento, que retornará  a saída de dados.</p>
<h3>Saída de dados</h3>
<p>Nossa saída de dados será o nosso próprio monitor, pois a  saída de dados pode ser uma impressora, disco etc.</p>
<h2>Diagrama de blocos</h2>
<p>É a ferramenta que o profissional possui que tem  como objetivo descrever o processo, o mesmo citado anteriormente <strong>entrada, processamento e saída de dados.</strong> O  diagrama de blocos pode ser desenvolvido em qualquer nível de detalhamento. O  diagrama de blocos utiliza-se de várias formas geométricas para representarmos  as seqüências a serem efetuadas. Observe a imagem a seguir seria a  representação em diagrama de blocos dos processos básicos a entrada,  processamento e saída de dados.</p>
<p class="center">
    <img src="/img/artigos/o-algoritmo-o-diagrama-de-blocos-e-o-php/exemplo-basico-de-diagrama-de-blocos.jpg" alt="Exemplo básico de diagrama de blocos" />
</p>
<p>O primeiro e o ultimo símbolo é o <strong>terminal</strong> representando respectivamente o inicio e o fim da  aplicação. Este símbolo tem que estar sempre presente representando o início e  o fim do diagrama de blocos. A <strong>seta </strong>indica  a direção em que o processamento do programa deve seguir. O símbolo seguido do  inicio representa o <strong>teclado</strong>, a  entrada de dados, o seguinte representa o <strong>processamento  de dados</strong> e o ultimo antes do terminal final representa o <strong>display</strong>, a saída de dados.</p>
<div class="dica">
    <ul>
        <li>Para o desenvolvimento correto do diagrama de  blocos o mesmo sempre deve ser feito de <strong>cima</strong> para <strong>baixo</strong> e da <strong>esquerda</strong> para <strong>direita</strong>.</li>
        <li>Como um bom exercício primeiro desenvolva o  problema no diagrama de blocos para posteriormente transcrevê-lo para a  linguagem de programação, no nosso caso o PHP.</li>
    </ul>
</div>
<div class="observacao">
  <p>Não entraremos em muitos detalhes sobre os diagramas de blocos, pois nem todos os símbolos serão utilizados à medida que formos avançando introduziremos novos símbolos.</p>
</div>
<h2>Exemplo em PHP e com a representação no diagrama de blocos</h2>
<p>Como foi dito anteriormente primeiro devemos desenvolver o  problema no diagrama de blocos para posteriormente desenvolvermos no próprio PHP. Então vamos primeiro ao problema, ou seja, o que nosso algoritmo terá que  resolver.</p>
<h3>Problema</h3>
<ol>
    <li>Ler dois valores, no caso às variáveis <code>$a</code> e <code>$b</code></li>
    <li>Realizar a soma das variáveis <code>$a</code> e <code>$b</code> e atribuir  o resultado a variável <code>$resultado</code></li>
    <li>Exibir o valor da variável <code>$resultado</code></li>
</ol>
<h3>Diagrama de blocos</h3>
<p>Observe como ficaria a representação no diagrama  de blocos do problema apresentado anteriormente.</p>
<p class="center">
    <img src="/img/artigos/o-algoritmo-o-diagrama-de-blocos-e-o-php/diagrama-de-blocos-do-problema-apresentado.jpg" alt="Diagrama de blocos do problema apresentado" />
</p>
<p>Primeiro iniciamos o diagrama de blocos com o <strong>terminal</strong> para representarmos o inicio  do código. Em seguida inserimos dois símbolos que representam a <strong>entrada de dados</strong>, pelo fato de nosso  programa necessitar de dois valores <code>$a</code> e <code>$b</code>. No bloco de <strong>processamento</strong> definimos que a variável <code>$resultado</code> terá o valor da  soma de <code>$a</code> com <code>$b</code>. Em seguida temos o display que representa a <strong>saída de dados</strong> que exibirá para nos a  variável <code>$resultado</code>. E por ultimo inserimos o terminal de fim.</p>
<h3>PHP</h3>
<p>Observe como ficaria a representação em PHP do diagrama de  blocos do problema apresentado anteriormente.</p>
<pre class="brush: php;">
&lt;?php

// Entrada de dado $a
$a = 10;

// Entrada de dado $b
$b = 7;

/**
 *  Processamento, somamos $a com $b
 *  e atribuimos o valor a $resultado
 */
$resultado = $a + $b;

// Saida de dados, o display
echo $resultado;

?&gt;
</pre>
<p>No código anterior da transcrição do diagrama de blocos para  o PHP. Iniciamos primeiramente criando as duas variáveis que serão à <strong>entrada de dados</strong> <code>$a</code> e <code>$b</code>. Em seguida  criamos a variável <code>$resultado</code> que tem em seu valor o resultado da soma de <code>$a</code> com <code>$b</code>, que seria o <strong>processamento</strong>.E por ultimo exibimos o resultado em  tela que seria a variável <code>$resultado</code> este sendo a nossa <strong>saída de dados</strong>.</p>
<p>Como você pode observar fizemos um exemplo muito simples,  pois a idéia é apenas você se acostumar com os símbolos apresentados no  diagrama de blocos e como representar o mesmo no PHP.</p>
<div class="observacao">
  <p>Realizamos a entrada de dados direto no nosso arquivo PHP por questões didáticas, no entanto esta entrada poderia vir de um formulário presente em seu sistema e processado e exibido neste nosso arquivo. No entanto trabalharemos no momento com a entrada de dados direto no nosso arquivo, posteriormente será abordada a entrada de dados por formulários.</p>
</div>
<div class="dica">
  <ul>
        <li>Experimente! Sinta-se livre para experimentar  com números diferentes, alterar o processamento para outra operação como a  multiplicação.</li>
        <li> Faça um  exercício crie um programa como o anterior para cada uma das operações  matemáticas que você aprendeu em <a href="/artigo/operadores-no-php">Operadores  aritméticos no PHP</a>.</li>
    </ul>
</div>