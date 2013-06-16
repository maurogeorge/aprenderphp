---
layout: post
title: Começando a programar em PHP
meta_description: Inicio do aprendizado em PHP, entenda o que são delimitadores de código, o que é uma variável, saiba como enviar resultados para o browser através do PHP. O PHP agindo em conjunto com o HTML e pra finalizar aprenda inserir comentários no PHP e entenda o que é uma constante.
meta_keywords: aprender, delimitadores, código, variável, HTML, comentários, constante
summary: Inicio do aprendizado em PHP, entenda o que são delimitadores de código, o que é uma variável, saiba como enviar resultados para o browser através do PHP. O PHP agindo em conjunto com o HTML e pra finalizar aprenda inserir comentários no PHP e entenda o que é uma constante.
tags: [HTML, Delimitadores de código, Variável, Comentários, Constantes]
---
<h2>Inicio da programação em PHP</h2>
<p>Para começarmos a programar em PHP primeiro abra o seu <a href="http://pt.wikipedia.org/wiki/Editor_de_texto">editor de texto</a> ou <a href="http://pt.wikipedia.org/wiki/Ambiente_de_Desenvolvimento_Integrado">IDE</a> preferido, <a href="http://www.smashingmagazine.com/2009/02/11/the-big-php-ides-test-why-use-oneand-which-to-choose/">analise  entre as melhores IDE para PHP</a> e  <a href="http://spreadsheets.google.com/ccc?key=pV8XyUSUOM7ET07rn4n7NYA">tabela  comparativo entre as melhores IDE para PHP</a> ambos em inglês. Uma boa saida é o <a href="http://www.aptana.org/">Aptana</a> e o <a href="http://www.aptana.org/php">plugin para desenvolvimento em PHP</a> mais  você pode utilizar o seu preferido.</p>
<h2>Delimitadores de código PHP</h2>
<p>Assim como o HTML temos as tags no PHP temos os  delimitadores de código, que são <code>&lt;?php</code> e <code>?&gt;</code> respectivamente a tag de  abertura e a tag de fechamento, em que o código deve ser inserido. Veja o  exemplo a seguir:</p>
<pre class="brush: php;">
&lt;?php

// Código PHP aqui!!!

?&gt;
</pre>
<div class="observacao">
  <p>Além dos delimitadores de código <code>&lt;?php</code> e <code>?&gt;</code> todas as suas páginas devem possuir a extensão .php por exemplo: meu-primeiro-programa.php</p>
</div>
<p>Ou ainda como mencionado no artigo anterior sobre o que é o PHP podemos <strong>misturar o PHP com o HTML</strong> como pode ser observado no exemplo a seguir.</p>
<pre class="brush: php; html-script: true">
&lt;?php

// Sim também podemos ter código PHP antes do DocType.

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;Titulo da minha página&lt;/title&gt;
&lt;?php

// Código PHP aqui dentro do head.

?&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;?php

// Código PHP aqui dentro do body!!!

?&gt;
&lt;/body&gt;
&lt;/html&gt;
&lt;?php

// Código PHP aqui até depois de fecharmos a tag html!

?&gt;
</pre>
<p>Como você pode perceber podemos escrever código PHP misturado com o HTML em qualquer parte do código. Além do exemplo que eu mostrei imagine que você queira gerar o titulo da sua página pelo PHP dinamicamente o que você faria? Isso mesmo colocaria as tags do PHP dentro da tag title e realizaria uma rotina para gerar o titulo dinamicamente.</p>
<div class="observacao">
  <p>Caso você já tenha programado algo em PHP ou baixado algum  script em PHP talvez já tenha se deparado com as tags respectivamente de  abertura e fechamento assim:</p>
  <ol>
    <li><code>&lt;?   ?&gt;</code></li>
    <li><code>&lt;% %&gt;</code></li>
    <li><code>&lt;script language=”PHP”&gt; &lt;/script&gt;</code></li>
  </ol>
  <p>O mais utilizado é o primeiro caso, no entanto <strong>não o utilize</strong>. Pois com o avanço do PHP  este tipo de escrita pode ser desabilitado e ainda pode ocorrer a possibilidade  de seu servidor web não aceitar este tipo de tag.</p>
  <p>Por isso prefira sempre as tags <code>&lt;?php</code> e <code>?&gt;</code>.</p>
</div>

<h2>Conceito de variável</h2>
<p>Variáveis como você já deve estar imaginando apenas pelo  nome é tudo aquilo que é sujeito a <strong>variações</strong>,  que é <strong>incerto</strong>, <strong>instável</strong> ou <strong>inconstante</strong>,  ou seja, pode <strong>mudar durante sua  existência</strong>. Vamos a uma analogia para entendermos o conceito de  variáveis.  Imagine a seguinte situação:<br />
  Joãozinho mora na casa de seus pais desde que nasceu e passa a maior parte do  dia em seu quarto. Com o passar dos anos o quarto de Joãozinho foi mudando,  seus brinquedos foram trocados por um computador, seu berço foi trocado por uma  cama, seu guarda-roupa de criança foi trocado por um de adulto, as paredes  foram pintadas de cores diferentes e Joãozinho ganhou uma televisão em seu  quarto.<br />
  Como você já deve ter imaginado a nossa variável aqui foi o quarto de  Joãozinho, que com o passar do tempo foi variando seu conteúdo.</p>
  <p>Trazendo o conceito de variável ao PHP e a nossas páginas de  internet. Voltemos ao exemplo anterior em que misturamos PHP e HTML. O conteúdo  que ficaria dentro da tag body gerado pelo PHP seria uma variável, que dependo  da página que estaríamos acessando este valor, ou seja, ele seria variável. A  página inicial teria um valor naquela variável e página de contato já teria um  valor diferente em sua variável.</p>
  <h2>As variáveis no PHP</h2>
  <p>Agora que você já possui um conceito de variável iremos ver  como criar nossas variáveis no PHP. As variáveis servem para armazenar dados  que podem ser utilizado em qualquer parte do programa. Para criar uma variável  em PHP você deve seguir algumas regras, são todas bem fáceis de se acostumar,  veja a seguir:</p>
  <ol>
    <li>As variáveis são representadas por um cifrão ($)  seguido pelo nome da variável</li>
    <li>O PHP é <a href="http://pt.wikipedia.org/wiki/Case_sensitive">case sensitive</a>, ou seja,  ele diferencia minúsculas de maiúsculas. Sendo então <code>$nome</code> diferente de <code>$Nome</code> e  <code>$NoMe</code></li>
    <li>Nomes de variáveis devem ser iniciados apenas  com uma letra ou _ (sublinhado) e podem ser seguido de letras ou algarismos, ou  seja, números podem aparecer em outras posições exceto na primeira</li>
    <li>Nunca utilize caracteres especiais em nome de  uma variável como acentos (é í ó) cedilha (ç) </li>
  </ol>
<h3>Exemplo de variáveis validas no PHP</h3>
<p>Veja a seguir exemplos de nomes válidos para variáveis,  baseadas nas regras que estudamos anteriormente.</p>
<pre class="brush: php;">
&lt;?php

$nome = 'Mauro George';
$nascimento = '06/09/1989';
$sobre_nome = 'Oliveira Tavares';

?&gt;
</pre>
<h3>Exemplo de variáveis invalidas no PHP</h3>
<p>Agora alguns nomes de variáveis invalidas no PHP que <strong>não</strong> devem ser utilizadas.</p>
<pre class="brush: php;">
&lt;?php

$20_anos_e_nome = 'Mauro George';
$ nascimento = '06/09/1989';
$*este_é_meu_sobrenome = 'Oliveira Tavares';

?&gt;
</pre>
<p>Como você já deve ter imaginado o sinal de <code>=</code> (igual) é  utilizado para atribuir um valor a variável, aprenderemos mais sobre eles  quando chegarmos em operadores de atribuição.</p>
<h2>Separação de instruções</h2>
<p>Você também deve ter reparado no exemplo anterior que depois  definirmos um valor a variável terminamos utilizando o sinal de <code>;</code> (ponto e  virgula). Este é o separador de instruções do PHP, ou seja, sempre que  definirmos uma variável ou imprimirmos algo na tela devemos utilizar o <code>;</code>.</p>
<h2>Enviando resultados ao browser, o uso do comando echo</h2>
<p>Você deve estar imaginando acabei de criar varias variáveis  mais como que eu faço para exibir o conteúdo que guardei em cada uma delas? E  neste ponto que aprenderemos exibir o valor de nossas variáveis na tela. Mais  primeiro exibiremos o mais clichê de todas as linguagens de programação o  famoso “Hello World”.</p>
<p>Aconselho a partir deste ponto criar uma pasta com o nome de <strong>estudos</strong> em seu diretório HTDOCS e vá  testando os exemplos que serão mostrados a seguir.</p>
<p>Não se esquecendo de salvar os arquivos com a extensão .php</p>
<pre class="brush: php;">
&lt;?php

echo 'Hello World';

?&gt;
</pre>
<p>Repare que ainda não exibimos os dados de uma variável  apenas exibimos um texto comum.</p>
<h3>Exibindo dados das variáveis no PHP</h3>
<p>Agora iremos exibir os valores de nossas variáveis no  browser utilizando o PHP, para isso utilizaremos as variáveis que criamos  anteriormente.</p>
<pre class="brush: php;">
&lt;?php

$nome = 'Mauro George';
$nascimento = '06/09/1989';
$sobre_nome = 'Oliveira Tavares';


echo $nome;
echo $sobre_nome;
echo $nascimento;

?&gt;
</pre>
<p>Você deve ter percebido que como exibimos varias variáveis quando terminou o dado de uma ele “colou” com o dado da próxima variável mais isto será concertado quando chegarmos a concatenação de strings, mais neste ponto o interessante é vermos que conseguimos exibir o valor da variável.</p>
<h3>Posso exibir dados das variáveis no PHP misturado com o HTML?</h3>
<p>SIM! Como o PHP se mistura ao HTML podemos exibir os dados em conjuntos vejam um exemplo pratico.</p>
<pre class="brush: php; html-script: true">
&lt;?php

$titulo = 'Aqui vai o titulo da minha página';
$css = '&lt;link rel="stylesheet" type="text/css" href="css/estilos.css" /&gt;';
$conteudo = 'Aqui é o conteudo mais como não tenho nenhum... &lt;br /&gt; vai apenas um&lt;br /&gt;&lt;br /&gt; &lt;strong&gt;Hello World&lt;/strong&gt;';

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;&lt;?php echo $titulo; ?&gt;&lt;/title&gt;

&lt;?php
echo $css;
?&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;?php

echo $conteudo;

?&gt;

&lt;p&gt;Eu posso repetir o valor da variavel sempre que eu quiser sabia? Veja aqui o nosso titulo denovo "&lt;?php echo $titulo; ?&gt;"&lt;/p&gt;
&lt;p&gt;E não necessariamente deveria imprimir $titulo apenas porque eu a declarei primeiro poderia imprimir $css antes e depois $titulo ou qualquer uma variavel isso vai de acorodo com sua necessidade&lt;/p&gt;
&lt;p&gt;Agora irei exibir $conteudo novamente olhe ela ai&lt;/p&gt;
&lt;p&gt;&lt;?php echo $conteudo; ?&gt;&lt;/p&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>
<p>Repare que além do PHP esta misturado ao HTML também a tags  de HTML no valor da minha variável em PHP.</p>
<p>As variáveis podem ser exibidas sempre que necessário na  tela, veja que repeti algumas variáveis mais de uma vez.</p>
<p>E ainda independente da ordem de declaração das variáveis  elas podem ser chamadas a sua escolha. Mesmo eu tendo declarado <code>$titulo</code>, <code>$css</code> e  <code>$conteudo</code> eu poderia exibir na tela primeiro <code>$conteudo</code> e <code>$css</code> e por ultimo  exibir <code>$titulo</code> a ordem de exibição sou eu que faço.</p>
<p>No entanto o seguinte exemplo geraria um erro:</p>
<pre class="brush: php;">
&lt;?php

echo $nome;
echo $sobre_nome;
echo $nascimento;

$nome = 'Mauro George';
$nascimento = '06/09/1989';
$sobre_nome = 'Oliveira Tavares';

?&gt;
</pre>
<p>Você sabe me dizer o por quê? Se você respondeu que devido a  tentarmos exibir uma variável sem antes declará-la você acertou. Ou seja, antes  de exibirmos qualquer dado antes devemos o ter declarado previamente.</p>
<h2>Comentários no PHP</h2>
<p>O PHP nos fornece um suporte a comentários que vem a ser  muito útil quando estamos desenvolvendo sistemas. Temos os seguintes tipos de  comentários no PHP:</p>
<ol>
  <li><code>//</code> comentário de uma linha apenas</li>
  <li><code>#</code> também comentário de uma linha apenas</li>
  <li><code>/* */</code> comentário de múltiplas linhas</li>
</ol>
<p>Veja todos eles em funcionamento abaixo:</p>
<pre class="brush: php;">
&lt;?php

// Comentario de uma linha apenas
# Outro modo de escrever um comentario de uma linha

/* Comentario de varias linhas com
 este podemos quebra linha e escrever
 quantas linhas quisermos.
*/

// Apenas um nome
$nome = 'Mauro George';
# A data de nascimento de uma pessoa
$nascimento = '06/09/1989';
// O Sobre nome de uma pessoa
$sobre_nome = 'Oliveira Tavares';

/* Aqui exibimos o nome
o sobre nome e a data de nascimento de
uma pessoa
*/
echo $nome;
echo $sobre_nome;
echo $nascimento;

?&gt;
</pre>
<h2>Constantes no PHP</h2>
<p>Como você já deve ter imaginado as constantes no PHP guardam  valores que nunca serão alterados.  Diferente das variáveis que possuem valores  que podem ser alterados, sendo assim após definida uma constante ela não pode  ser alterada ou removida.</p>
<p>Para definirmos uma constante utilizamos o comando <code>define();</code> que tem sua sintaxe a seguir:</p>
<p><code>define( ‘NOME_DA_CONSTANTE’, ‘VALOR DA CONSTANTE’ );</code></p>
<p>O nome de uma constante tem a mesma regra de qualquer  identificador PHP, ou seja, as mesmas regras de nomes de variáveis exceto pelo  fato de constantes <strong>não</strong> iniciarem o  nome com cifrão ($).<br />
  Veja um exemplo a seguir em que utilizamos uma constante.</p>
<pre class="brush: php; html-script: true">
&lt;?php
// Defino o titulo da minha página
$titulo = 'Exemplo utilizando Constantes';
// Apenas um nome
$nome = 'Mauro George';
// A data de nascimento de uma pessoa
$nascimento = '06/09/1989';
// O Sobre nome de uma pessoa
$sobre_nome = 'Oliveira Tavares';
// Defino o ESTADO da pessoa que é uma constante
define( 'ESTADO', 'Rio de Janeiro' );

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;&lt;?php echo $titulo; ?&gt;&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;&lt;?php echo $nome; ?&gt; &lt;?php echo $sobre_nome; ?&gt;, nascido em &lt;?php echo $nascimento; ?&gt; nasceu no &lt;?php echo ESTADO; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<p>Agora que você entendeu o funcionamento de uma constante  deve estar se perguntando: qual a diferença real entre variáveis e constantes?<br />
  Acompanhe o exemplo a seguir e observe que variáveis podem ter seus valores  modificados durante a execução de uma página, já as constantes seus valores  nunca podem ter seus valores alterados.</p>
<pre class="brush: php; html-script: true">
&lt;?php
// Defino o titulo da minha página
$titulo = 'Exemplo utilizando Constantes';
// Apenas um nome
$nome = 'Mauro George';
// A data de nascimento de uma pessoa
$nascimento = '06/09/1989';
// O Sobre nome de uma pessoa
$sobre_nome = 'Oliveira Tavares';
// Defino o ESTADO da pessoa que é uma constante
define( 'ESTADO', 'Rio de Janeiro' );

?&gt;
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;&lt;?php echo $titulo; ?&gt;&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;p&gt;&lt;?php echo $nome; ?&gt; &lt;?php echo $sobre_nome; ?&gt;, nascido em &lt;?php echo $nascimento; ?&gt; nasceu no &lt;?php echo ESTADO; ?&gt;&lt;/p&gt;
&lt;?php
/**
 * Redefino os valores das seguintes variaveis
 *
 */
$nome = 'Jéssica';
$nascimento = '12/07/1990';
$sobre_nome = 'Monteiro da Silva';
define( 'ESTADO', 'São Paulo' );

?&gt;
&lt;p&gt;&lt;?php echo $nome; ?&gt; &lt;?php echo $sobre_nome; ?&gt;, nascido em &lt;?php echo $nascimento; ?&gt; nasceu no &lt;?php echo ESTADO; ?&gt;&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<div class="observacao">
  <p>Por padrão sempre escreva o nome de constantes em maiúsculo  e separado por _ (sublinhado). Exemplo:</p>
  <p>MINHA_CONSTANTE, UMA_CONSTANTE, CONSTANTE</p>
  <p>E não se esqueça que constantes não são iniciadas com o  cifrão ($).</p>
</div>