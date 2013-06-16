---
layout: post
title: If, else e elseif as estruturas de  controle no PHP
meta_description: Aprenda sobre a tomada de decisões no PHP com as estruturas de controle if, else e elseif.
meta_keywords: php, estruturas de controle, if, else, elseif, diagrama de blocos, condicionais, operadores
summary: Aprenda sobre a tomada de decisões no PHP com as estruturas de controle if, else e elseif.
tags: [Tipos de dados, Operadores, Algoritmo, Estruturas de controle]
---
<h2>Introdução</h2>
<p>Você aprendeu trabalhar com a <a href="/artigo/o-algoritmo-o-diagrama-de-blocos-e-o-php">entrada, o processamento e a saída  de dados</a> com a <a href="/artigo/comecando-a-programar-em-php">utilização de variáveis e constantes</a> além dos <a href="/artigo/operadores-no-php">operadores aritméticos</a> e o que fará mais sentido aqui os <a href="/artigo/operadores-de-comparacao-operadores-logicos-e-a-precedencia-dos-operadores-no-php">operadores de comparação e os operadores  lógicos</a>.</p>
<p>Até o momento sem as estruturas de controle não  podemos <strong>tomar decisões</strong>. Imagine o seguinte  problema.</p>
<h3>Problema</h3>
<ol>
    <li>Ler a  entrada de 4 notas de um aluno</li>
    <li>Obter  sua média</li>
    <li>Se a média  for maior ou igual a 7 retornar aprovado menor que 7 retornar reprovado</li>
    <li>Exibir a  média do aluno e se foi aprovado ou reprovado</li>
</ol>
<p>Como você pode observar as partes 1 e 2 do  problema poderíamos resolver facilmente com os operadores aritméticos. Veja o  exemplo a seguir:</p>
<pre class="brush: php;">
&lt;?php

/**
 * Entrada das 4 notas do aluno
 */
$nota1 = 10;
$nota2 = 9;
$nota3 = 7;
$nota4 = 5;

/**
 * Obtendo a média do aluno
 */
$resultado = ($nota1 + $nota2 + $nota3 + $nota4) / 4;

/**
 * Retornando a média
 */
echo $resultado;

?&gt;
</pre>
<div class="destaque">
  <p>Caso não tenha entendido o uso dos operadores ou o porquê do parêntesis. Recomendo  antes de continuar ler o artigo sobre <a href="/artigo/operadores-no-php">operadores no PHP</a> e  o artigo que fala sobre a <a href="/artigo/operadores-de-comparacao-operadores-logicos-e-a-precedencia-dos-operadores-no-php">precedência dos operadores no PHP</a></p>
</div>
<p>No entanto a parte 3, não poderíamos  desenvolver até aqui, pois necessitamos das estruturas de controle, que você  irá ver agora.</p>
<h2>If o desvio condicional simples no  PHP</h2>
<p>O construtor <code>If</code> tem como  objetivo executar todo o código que esteja entre o construtor caso o resultado da avaliação seja verdadeiro caso contrario nada será executado.</p>
<p>Continuando o problema anterior mais neste  ponto apenas um fragmento para ilustrar.</p>
<h3>Problema</h3>
<ol>
    <li>Ler a  entrada de 4 notas de um aluno</li>
    <li>Obter sua  média</li>
    <li>Se a média  for maior ou igual a 7 retornar aprovado</li>
    <li>Exibir a média  do aluno e se foi aprovado</li>
</ol>
<h3>O diagrama de blocos</h3>
<p>Observe como seria a  representação do nosso problema no diagrama de blocos.</p>
<p class="center">
    <img alt="Diagrama de blocos do problema apresentado" src="/img/artigos/if-else-e-elseif-as-estruturas-de-controle-no-php/diagrama-de-blocos-do-problema-de-estruturas-de-controle-no-php.jpg" />
</p>
<p>O símbolo de inicio  não é nenhuma novidade afinal já foi explicado no artigo sobre <a href="/artigo/o-algoritmo-o-diagrama-de-blocos-e-o-php">algoritmo e diagrama de blocos no  PHP</a>, o símbolo seguinte  também já é um conhecido nosso o de entrada de dados, no entanto como teremos a  entrada de 4 valores foi preferível exemplificar desta forma apenas um símbolo  de entrada e os valores separados por virgula. Em seguida o processamento  novamente nada demais, se esta com duvida sobre o porquê da variável <code>$mensagem</code> vazia não se preocupe se você não conseguir descobrir um pouco mais a frente  será explicado. Agora o nosso símbolo novo é o <strong>losango</strong> que é o nosso símbolo de <strong>decisão</strong>. Observe também a presença das letras <strong>S</strong> e <strong>N</strong> representando  respectivamente <strong>sim</strong> e <strong>não</strong>. Caso a condição dentro do bloco de  decisão seja <strong>verdadeira</strong> o que esta  dentro do bloco do <strong>sim</strong>, S, será  executado, caso seja <strong>falsa</strong> o que  estiver dentro do bloco do <strong>não</strong>, N,  será executado. Observe o uso das setas para indicar a direção do  processamento. Ao final novamente um símbolo conhecido o display e para  finalizar o terminal final.</p>
<h3>No PHP</h3>
<p>Seguimos a mesma  lógica do código anterior, no entanto observe que criamos a variável $mensagem,  em seguida criamos a nossa estrutura de controle <code>If</code> com o <a href="/artigo/operadores-de-comparacao-operadores-logicos-e-a-precedencia-dos-operadores-no-php">operador de comparação</a> <code>&gt;=</code> se esta expressão for <strong>verdadeira</strong> a variável <code>$mensagem</code> terá  uma valor dizendo que o aluno foi aprovado. Se a nota for menor que 7 apenas exibe  a nota. Observe o código a seguir:</p>
<pre class="brush: php;">
&lt;?php

/**
 * Entrada das 4 notas do aluno
 */
$nota1 = 10;
$nota2 = 9;
$nota3 = 7;
$nota4 = 5;

/**
 * Obtendo a média do aluno
 */
$resultado = ($nota1 + $nota2 + $nota3 + $nota4) / 4;

/**
 * Crio a mensagem
 */
$mensagem = '';
if( $resultado &gt;= 7 ){

  $mensagem = ' o aluno foi aprovado';

}

/**
 * Retornando a média
 */
echo $resultado . $mensagem;

?&gt;
</pre>
<div class="observacao">
  <p>Você sabe o porquê de  termos criado a variável <code>$mensagem</code> com um valor vazio antes do <code>If</code>? O objetivo  disto é o seguinte, pois independente da nota exibimos a variável <code>$mensagem</code> no  nosso retorno, e se a nota for menor que 7 não teríamos a variável <code>$mensagem</code>,  pois ela só seria criada se a média fosse maior ou igual a 7, o que geraria um  erro de notice afinal o PHP estaria tentando exibir uma variável inexistente.  No <a href="/artigo/instalando-o-apache-o-php-e-o-mysql">artigo de instalação do PHP</a> exibimos como manter para seu PHP exibir todos  os erros.</p>
</div>
<div class="dica">
    <p>Em relação a estrutura  de controle <code>If</code>:</p>
    <ul>
        <li>As  expressões são exibidas entre parêntesis logo após a declaração da estrutura</li>
        <li>Expressões  são realizadas por <a href="/artigo/operadores-de-comparacao-operadores-logicos-e-a-precedencia-dos-operadores-no-php">operadores lógicos e operadores de  comparação</a> </li>
        <li>O bloco de  código referente a estrutura de controle deve ser delimitado por chaves <code>{}</code></li>
        <li>Endente o  código referente ao bloco em 4 espaços por questões de legibilidade, a como  configurar o seu editor de texto para transformar Tabs em espaços</li>
    </ul>
</div>
<p>Até aqui está legal  nosso programa, se a nota for maior que 7 ele exibe que foi aprovado, no  entanto ainda falta ele exibir também quando o aluno for reprovado, pois até o  momento quando ele é reprovado apenas a nota é exibida, então é neste ponto que  conheceremos outra estrutura de controle o <code>else</code>.</p>
<h2>Else o desvio condicional composto no  PHP</h2>
<p>O else é a estrutura  de controle que é executada quando o <code>If</code>, ou <code>elseif</code>, você aprenderá a seguir,  for retornado falso.</p>
<p>Continuando  o nosso primeiro problema apresentado agora poderemos exibir a média e se foi  aprovado ou reprovado. Lembrando que com apenas o <code>If</code> conseguíamos exibir apenas  o aprovado.</p>
<h3>O diagrama de blocos</h3>
<p>Observe como seria a  representação do nosso problema no diagrama de blocos.</p>
<p class="center">
    <img alt="Diagrama de blocos do problema apresentado" src="/img/artigos/if-else-e-elseif-as-estruturas-de-controle-no-php/diagrama-de-blocos-do-problema-de-estruturas-de-controle-no-php-1.jpg" />
</p>
<p>Seguimos a mesma  lógica do diagrama anterior. E como foi dito que o else é executado quando o <code>if</code>  for retornado falso, apenas tivemos que criar um bloco de processamento  seguindo para o bloco da letra <strong>N</strong> afinal  é o <code>else</code> e só será executado se a condição for falsa.</p>
<h3>No PHP</h3>
<p>Seguimos a mesma  lógica do código anterior, no entanto observe que logo após o fechamento do <code>if</code> inserimos a nossa nova clausula <code>else</code>. O que poderia ser lido assim “se  resultado for maior ou igual a 7 o aluno foi aprovado senão o aluno foi reprovado”.  Lembrando que será executado o bloco <code>if</code> se a expressão, em nosso caso <code>$resultado  &gt;= 7</code>, for verdadeira <strong>senão</strong> será  executado o else. Observe o código a seguir:</p>
<pre class="brush: php;">
&lt;?php

/**
 * Entrada das 4 notas do aluno
 */
$nota1 = 10;
$nota2 = 2;
$nota3 = 7;
$nota4 = 5;

/**
 * Obtendo a média do aluno
 */
$resultado = ($nota1 + $nota2 + $nota3 + $nota4) / 4;

/**
 * Crio a mensagem
 */
$mensagem = '';
if( $resultado &gt;= 7 ){

  $mensagem = ' o aluno foi aprovado';

} else {

  $mensagem = ' o aluno foi reprovado';

}

/**
 * Retornando a média
 */
echo $resultado . $mensagem;

?&gt;
</pre>
<div class="observacao">
  <p>Mantemos a variável  mensagem criada antes por questões de visibilidade e padronização do nosso  código, pois aqui de um jeito ou de outro ela seria criada se fosse maior ou  igual a 7 ou se não fosse menor que 7 devido ao nosso else.</p>
</div>
<div class="dica">
    <p>Em relação a estrutura  de controle else:</p>
    <ul>
        <li><strong>Não</strong> possui expressões a ser avaliada é executado após um <code>if</code>, ou <code>elseif</code>,  você aprenderá a seguir, ter retornado <code>false</code>(falso)</li>
        <li>O bloco de  código referente à estrutura de controle deve ser delimitado por chaves <code>{}</code></li>
        <li>Endente o  código referente ao bloco em 4 espaços por questões de legibilidade, a como configurar  o seu editor de texto para transformar Tabs em espaços</li>
    </ul>
</div>
<p>Tudo bem até aqui  finalizamos o nosso problema, apresentado no inicio. No entanto podemos o  incrementar ainda mais para ficar mais legal. E se o aluno tirar 10? Ele foi  aprovado, mais podemos exibir uma mensagem especial igual as que as professoras  de primário exibem. Sendo assim se o aluno tirar 10 exibiremos uma mensagem  especial e para exibir esta mensagem especial utilizaremos da estrutura de controle <code>elseif</code>.</p>
<h2>Elseif outro desvio condicional  composto no PHP</h2>
<p>O <code>elseif</code> é a estrutura  de controle que será avaliada após o <code>if</code> retornar falso, o <code>elseif</code> é inserido  antes do <code>else</code>, e mais de um <code>elseif</code> pode ser inserido, lembrando que o <code>elseif</code> avalia expressões assim como o <code>if</code>. Ficando assim se um <code>if</code> retornar falso caíra  no <code>elseif</code>, se o <code>elseif</code> retornar falso cairá no próximo <code>elseif</code> se houver, após  todos os <code>elseif</code> finaliza á lógica no <code>else</code>.</p>
<p>Continuando nossa  lógica da média do aluno, iremos exibir uma mensagem de sucesso quando ele  tirar 10, e uma mensagem para ele estudar mais se tirar 0, pois como foi dito  podemos ter mais de um <code>elseif</code>, além do que já esta sendo exibido  o aprovado e reprovado.</p>
<h3>O diagrama de blocos</h3>
<p>Observe como seria a  representação no diagrama de blocos com a inserção da nossa nova lógica.</p>
<p class="center">
    <img alt="Diagrama de blocos do problema apresentado" src="/img/artigos/if-else-e-elseif-as-estruturas-de-controle-no-php/diagrama-de-blocos-do-problema-de-estruturas-de-controle-no-php-2.jpg" />
</p>
<p>Observe que  adicionamos mais uma condição no <code>if</code> agora nosso resultado além de ser maior ou  igual a 7 não pode ser 10, pois o 10 tem uma mensagem especial. Se esta  condição for verdadeira exibe a mensagem de aprovado, até aqui tudo igual. Se a  condição for falsa verificamos se a variável <code>$resultado</code> é igual a 0 se a  condição for verdadeira retornamos uma mensagem, se for falsa, verificamos  novamente o valor de <code>$resultado</code> se é igual a 10 se for verdadeira a expressão  retornamos uma mensagem caso contrario caímos no nosso else que diz que o aluno  foi reprovado. Observe que utilizamos o mesmo símbolo de condição, o losango,  para representar o <code>elseif</code>. E um novo símbolo que é um pequeno circulo, o  conector, foi utilizado para conectar as condições e todas levarem para um  mesmo final.</p>
<h3>No PHP</h3>
<p>Mantendo a mesma  lógica do código anterior adicionamos 2 estruturas <code>elseif</code> antes do <code>else</code>. Uma  para quando a média do aluno for igual a 0 e outra para quando a média do aluno  for igual a 10, assim retornando mensagens personalizadas para estas médias.  Observe que adicionamos uma nova condição ao <code>if</code> com o operador lógico  <code>&amp;&amp;</code> e com o operador de comparação <code>!=</code> pois aqui dissemos para retornar o  resultado do <code>if</code> se a nota for maior ou igual a 7 e não igual a 10, afinal 10  tem um tratamento especial. Agora porque não colocamos o operador de negação no  0? Porque o <code>if</code> só é executado se o <code>$resultado</code> for maior ou igual a 7 e como o 0  é menor ele não se encaixa no <code>if</code> e seguiria para o próximo <code>elseif</code>. Observe o  código a seguir:</p>
<pre class="brush: php;">
&lt;?php

/**
 * Entrada das 4 notas do aluno
 */
$nota1 = 10;
$nota2 = 10;
$nota3 = 10;
$nota4 = 10;

/**
 * Obtendo a média do aluno
 */
$resultado = ($nota1 + $nota2 + $nota3 + $nota4) / 4;

/**
 * Crio a mensagem
 */
$mensagem = '';
if ( $resultado &gt;= 7 &amp;&amp; $resultado != 10 ) {

  $mensagem = ' o aluno foi aprovado.';

} elseif ( $resultado == 0 ) {

  $mensagem = ' estude mais, você não acertou nada.';

} elseif ( $resultado == 10 ) {

  $mensagem = ' parabéns! Aprovado com nota máxima.';

} else {

  $mensagem = ' o aluno foi reprovado.';

}

/**
 * Retornando a média
 */
echo $resultado . $mensagem;

?&gt;
</pre>
<div class="dica">
    <p>Em relação a estrutura  de controle <code>elseif</code>:</p>
    <ul>
        <li>O <code>elseif</code>  será avaliada após o <code>if</code> retornar falso</li>
        <li>É inserido  depois do <code>if</code> e antes do <code>else</code></li>
        <li>Podemos  ter vários <code>elseif</code> antes do <code>else</code></li>
        <li>Aceita  expressões</li>
        <li>As  expressões são exibidas entre parêntesis logo após a declaração da estrutura</li>
        <li>Expressões  são realizadas por <a href="/artigo/operadores-de-comparacao-operadores-logicos-e-a-precedencia-dos-operadores-no-php">operadores lógicos e operadores de  comparação</a> </li>
        <li>O bloco de  código referente à estrutura de controle deve ser delimitado por chaves <code>{}</code></li>
        <li>Endente o  código referente ao bloco em 4 espaços por questões de legibilidade, a como  configurar o seu editor de texto para transformar Tabs em espaços</li>
    </ul>
</div>
<div class="destaque">
<p>Ainda temos mais  estruturas de controle no PHP, sendo assim no próximo artigo voltaremos a elas. Enquanto isso experimente, com as estruturas de controle que aprendeu tente  resolver pequenos problemas.  Por exemplo  entre com 3 valores um operador, a e b e de acordo com o operador o programa  tem que executar uma operação matemática(soma, subtração, multiplicação e  divisão) utilizando as estruturas de controle aprendidas aqui e os <a href="/artigo/operadores-no-php">operadores do PHP</a>.</p>
</div>