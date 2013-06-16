---
layout: post
title: Instalando o Apache, o PHP e o MySQL
meta_description: Aprenda fazer a instalação do WAMP (Windows, Apache, MySQL e PHP), caso não queira instalar manualmente daremos a dica também. Além de aprendermos configurar o WAMP para nosso ambiente de desenvolvimento.
meta_keywords: instalação, instalacao, windows, apache, mysql, php, wamp, desenvolvimento
summary: Aprenda fazer a instalação do WAMP (Windows, Apache, MySQL e PHP), caso não queira instalar manualmente daremos a dica também. Além de aprendermos configurar o WAMP para nosso ambiente de desenvolvimento.
tags: [Instalação, Apache, MySQL]
---
<p>Agora que você já conhece um pouco do PHP, iremos aprender a  fazer a instalação para podermos prosseguir com nossos estudos. Como sabemos o  PHP necessita de um servidor para rodar nossas aplicações este servidor no  nosso caso será o apache, também teremos de instalar o próprio PHP e para  nossas aplicações futuras envolvendo banco de dados utilizaremos o MySQL.</p>
<div class="observacao">
  <p>Focaremos nossa instalação do apache, php e mysql no Windows,  esta combinação também é conhecida como WAMP (Windows, Apache, MySQL e PHP).</p>
  <p>Caso utilize o linux a excelentes artigos pela  internet de como instalar o LAMP (Linux, Apache, MySQL e PHP)</p>
</div>
<h2>Sobre o Apache</h2>
<p>O Apache é um servidor open source, muito estável e seguro,  pois vem sendo desenvolvido há bastante tempo.<br />
  A idéia de instalarmos um servidor em  nossa maquina local é apenas para o desenvolvimento de nossas aplicações, pois  assim acessaremos o site como se estivéssemos acessando pela Internet. <br />
No entanto quando o projeto estiver finalizado transferimos nosso projeto para  nossa hospedagem normalmente.</p>
<h2>Instalando o Apache</h2>
<p>Baixe a versão mais nova do apache em <a href="http://www.apache.org/dist/httpd/binaries/win32/">http://www.apache.org/dist/httpd/binaries/win32/</a></p>
<p>Baixaremos a versão com installer do Windows algo como apache_2.2.xx-win32-x86-no_ssl.msi  onde xx é o número da versão aqui estamos instalando a 2.2.</p>
<p>Depois de realizado o download inicie a instalação  normalmente ao se deparar com a seguinte tela:</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/instalando-o-apache.jpg" alt="Instalando o Apache" />
</p>
<p>Preencha os dados de acordo com a figura anterior. Ou seja:</p>
<ul>
  <li>Network  Domain = localdomain</li>
  <li>Server  Name = localhost</li>
  <li>Administrator's  Email Address = seuemail@email.com</li>
  <li>Mantendo  a opção &quot;for All Users, on port 80, as a Service -- Recommended&quot;  marcado</li>
</ul>
<p>Finalizada a instalação você vera o ícone do apache, Apache Service  Monitor, próximo ao seu relógio. Utilizaremos o Apache Service Monitor quando  quisermos reiniciar o nosso servidor.</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/apache-service-monitor.jpg" alt="Apache Service Monitor" />
</p>
<p>Neste ponto temos instalado o nosso servidor, Apache, pare  ver se o apache está instalado e funcionando abra o seu navegador e digite  “localhost” devera ser exibida uma mensagem como a seguir:</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/apache-it-works.jpg" alt="Apache It works!" />
</p>
<p>A mensagem “It works!” significa qua o servidor está  funcionando algo como “ele trabalha!”. Agora para executarmos nossos programas  devemos colocar os arquivos dentro da pasta “htdocs” de nossa instalação do  apache, se você não alterou o caminho da instalação será algo como “C:\Program  Files\Apache Software Foundation\Apache2.2\htdocs” lembrando que é possível  criar diretórios assim os diretórios serão acessados por  HTTP://localhost/meu-diretorio.</p>
<h2>Instalando o PHP</h2>
<p>O PHP também pode ser encontrado com o instalador em <a href="http://www.php.net/downloads.php">http://www.php.net/downloads.php</a>.</p>
<p>Baixe a versão com instalador mais nova, o nome deve ser  algo como php-5.2.x-win32-installer, em que x é alguma revisão da versão 5.2,  se houver versões mais novas que a 5.2 prefira as mais novas.</p>
<p>Inicie a instalação normalmente quando ele pedir o tipo de servidor  usado escolha o Apache 2.2.x Module, que foi o que acabamos de instalar.</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/instalando-o-php.jpg" alt="Instalando o PHP selecionando o Apache 2.2.x Module" />
</p>
<p>Posteriormente será solicitada a pasta onde estão os  arquivos de configuração do apache , selecione a pasta conf dentro da pasta  onde foi instalado o apache</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/instalando-o-php-1.jpg" alt="Instalando o PHP selecionando a pasta onde estão os  arquivos de configuração do Apache" />
</p>
<p>Finalizada a instalação devemos reiniciar o apache, abra o  Apache Service Monitor e clique em “STOP” em seguida clique em “START”.</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/apache-service-monitor-1.jpg" alt="Apache Service Monitor STOP" />
</p>
<p>Para termos certeza se o PHP está funcionando crie um  arquivo com o nome de info.php e salve o dentro de seu htdocs, com o seguinte  conteúdo:</p>
<pre class="brush: php;">
&lt;?php

phpinfo();

?&gt;
</pre>
<p>Acesso o seu arquivo através de HTTP://localhost/info.php você verá uma  imagem como a seguir</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/php-info.jpg" alt="phpinfo()" />
</p>
<h2>Instalando o MySQL</h2>
<p>O Mysql pode ser encontrado para download em <a href="http://www.mysql.com/downloads/mysql/">http://www.mysql.com/downloads/mysql/</a>.</p>
<p>Baixe a versão mais recente com o instalador do  Windos(.msi).</p>
<p>Novamente inicie a instalação normalmente.</p>
<p>Em um ponto ele solicita o número da porta, mantenha o  padrão se for o caso, e marque a opção “Add Firewall exception for this port”  para garantir que o firewall não impedira o MySQL de funcionar.</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/instalando-o-mysql.jpg" alt="Instalando o MySQL" />
</p>
<p>Em um ponto a frente na instalação marque a opção &quot;Include  Bin Directory in Windows PATH&quot; para poder ser possível executar o mySQL  apartir do prompt.</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/instalando-o-mysql-1.jpg" alt="Instalando o MySQL" />
</p>
<p>Será solicitada uma senha para acesso ao banco de dados,  aqui para o usuário “root”, caso não queira definir senha alguma desmarque o  campo &quot;Modify Security Settings&quot;.</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/instalando-o-mysql-2.jpg" alt="Instalando o MySQL" />
</p>
<p>Estas são as configurações do MySQL o resto da instalação  não a duvidas.</p>
<h2>Configurações Finais</h2>
<h3>Configurando o PHP para o ambiente de desenvolvimento</h3>
<p>Agora temos que configurar o nosso PHP, para poder acessar o  Banco de dados, no nosso caso o MySQL através das extensões. Vá em meu  computador &gt; Painel de controle &gt; adicionar ou remover programas encontre  o PHP e clique em alterar em seguida clique em change não altere o que você já  configurou previamente. Chegando na etapa de extensões selecione “<strong>MySQL</strong>” e a opção “Will be installed on  local hard drive” realize a mesma coisa com as seguintes extensões “<strong>GD2</strong>” e “<strong>PDO</strong>” ambas extensões bastante utilizadas no PHP.</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/adicionando-extensoes-ao-php.jpg" alt="Adicionando extensões ao PHP" />
</p>
<p class="center">
    <img src="/img/artigos/instalando-o-apache-o-php-e-o-mysql/adicionando-extensoes-ao-php-1.jpg" alt="Adicionando extensões ao PHP" />
</p>
<p>Em seguida encontre o arquivo php.ini onde foi instalado o  seu php e procure pelos seguintes itens e altere seus valores, mantendo os  assim:</p>
<ul>
  <li>short_open_tag = On</li>
  <li>display_errors = On</li>
  <li>error_reporting  = E_ALL | E_STRICT</li>
</ul>
<p>Lembrando de alterar os valores reais pois o que está  precedido de ; são comentários e não são processados.</p>
<p>Os comandos que alteremos são respectivamente para aceitar o  uso de tags curtas do PHP você saberá do que se trata mais a frente, esta opção  é apenas por uma questão de compatibilidade de códigos de terceiros. Em seguida  para mostrar os erros, afinal estamos em modo de desenvolvimento, em modo de  produção <strong>nunca </strong>exiba os erros  diretamente para o usuário. E por último para reportamos todos os tipos de  erros.</p>
<h3>Configurando o Apache para o ambiente de desenvolvimento</h3>
<p>No diretório onde foi instalado o apache  encontre a pasta “conf” e o arquivo “httpd.conf “ busque por “DirectoryIndex”  defina os itens que deverão ser buscado ao ser acessado uma pasta ficando  assim:</p>
<pre class="brush: plain;">
&lt;IfModule dir_module&gt;
    DirectoryIndex index.html default.html index.htm default.htm index.php default.php
&lt;/IfModule&gt;
</pre>
<h4>Ativando o mod_rewrite</h4>
<p>O mod_rewrite resumidamente é um módulo do apache que nos  permite a reescrita de urls, apenas o ativaremos neste ponto, para quando for necessária  a reescrita de url não seja necessário nenhuma configuração posterior do  apache.</p>
<p>Procure pela linha “LoadModule rewrite_module  modules/mod_rewrite.so” se estiver comentada, com um # antes, descomente a ,  retirando o #. Busque também por AllowOverride e defina como All.</p>
<h3>Configurando o MySQL para o ambiente de desenvolvimento</h3>
<p>O MySQL não tem o que ser configurado tudo já foi  previamente definido na instalação. O que podemos fazer apenas é baixar as  ferramentas no próprio site do MySQL <a href="http://dev.mysql.com/downloads/gui-tools/5.0.html">http://dev.mysql.com/downloads/gui-tools/5.0.html</a>.</p>
<h2>Finalizando</h2>
<p>Após termos configurado tudo, reiniciamos novamente o  Apache. E para testarmos nossa conexão do PHP com o banco de dados criamos um  arquivo em nosso htdocs com o nome de banco.php com o seguinte conteúdo:</p>
<pre class="brush: php;">
&lt;?php

$link = mysql_connect('localhost', 'root', '');

if (!$link) {
    die('Não foi possível conectar: ' . mysql_error());
}
echo 'Conexão bem sucedida';

mysql_close($link);

?&gt;
</pre>
<p>Caso tenha alterado a senha de seu banco de dados a defina  aqui em <code>$link = mysql_connect('localhost', 'root', '<strong>sua senha aqui</strong>');</code></p>
<p>Acesse este programa através de <a href="http://localhost/banco.php">http://localhost/banco.php</a> e você  recebera uma mensagem dizendo se foi possível ou não realizar a conexão com o  banco de dados.</p>
<h2>E se eu não conseguir instalar? Ou simplesmente não quiser instalar isso  tudo.</h2>
<p>Não tem problema. Existem soluções que englobam toda a  instalação que acabamos de realizar em apenas uma instalação mais simples como  é o caso do <a href="http://www.apachefriends.org/pt_br/xampp.html">xampp</a>.</p>
<p>No entanto prefira a instalação manual pois você estará  aprendendo um pouco mais quando tiver que alterar um arquivo de configuração  seja ele do PHP ou do próprio Apache, mesmo que em ambiente de produção, onde  você hospedar seu site, dificilmente terá controle total sobre tais  configurações.</p>