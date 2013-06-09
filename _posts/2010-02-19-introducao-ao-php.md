---
layout: post
title: Introdução ao PHP
meta_description: Uma introdução ao PHP, neste artigo descubra se o PHP é gratuito, sua integração com o HTML, entenda o que é Server-side e Client-side eo principal o que podemos fazer com o PHP.
meta_keywords: introdução, php, html, server-side, client-side, banco de dados, mysql
summary: Uma introdução ao PHP, neste artigo descubra se o PHP é gratuito, sua integração com o HTML, entenda o que é Server-side e Client-side e o principal o que podemos fazer com o PHP.
tags: [HTML, Server-side, Client-side, Banco de dados]
---
<h2>O que é o PHP</h2>
<p>PHP é o acrônimo para Hypertext Preprocessor, algo como  pré-processador de hiper texto, uma linguagem de programação muito utilizada  principalmente para o desenvolvimento web. Apesar de ter a versão <a href="http://pt.wikipedia.org/wiki/PHP-GTK">PHP-GTK</a> para ambiente desktop.  No decorrer de nosso aprendizado focaremos no <a href="http://pt.wikipedia.org/wiki/PHP">PHP</a> para desenvolvimento web.</p>
<h2>O PHP é gratuito?</h2>
<p>Sim! Para começar o PHP é <a href="http://pt.wikipedia.org/wiki/C%C3%B3digo_aberto">open source</a>, ou  seja, código fonte aberto. Assim para obter o PHP a única coisa que deve fazer  é entrar no <a href="http://www.php.net/">site do PHP</a> e fazer o <a href="http://www.php.net/downloads.php">download da versão mais nova</a>. Pois  com a versão mais recente terá novas funcionalidades além de possíveis bugs  terem sido corrigidos.</p>
<h2>PHP e o HTML</h2>
<p>Uma pagina em PHP normalmente possui a extensão <strong>.php</strong>(dependendo da configuração do  servidor Web). No entanto nestas páginas com a extensão .php pode ser inserido  normalmente o código HTML que você já esta acostumado a desenvolver. E  funcionara da seguinte maneira, sempre que o servidor receber páginas com a  extensão .php ele  saberá que a linguagem  de programação na página, interpretando HTML, e ao encontrar código PHP  interpretar os mesmos, ou vice versa e mais de uma vez pois não importa a  quantidade de vezes que você altera entre código HTML e PHP e se você inicia o  código com um ou com outro. Resumindo podemos escrever HTML e PHP em um arquivo  .php que tudo será interpretado corretamente.</p>
<h2>O PHP, o Server-side e o Client-side</h2>
<h3>Client-side</h3>
<p>É tudo processado no lado do cliente. O <a href="http://pt.wikipedia.org/wiki/Client_Side_Scripts">client-side</a> é  interpretado diretamente pelo browser (navegador) do usuário. Sendo assim ao  acessar uma página web o HTML, CSS e JavaScript são interpretados todos pelo  navegador sem intervenção nenhuma de um servidor. Por isso podemos exibir o  código fonte em nosso browser e visualizar o HTML, CSS e o JavaScript.</p>
<h3>Server-side</h3>
<p>O oposto do client-side. Aqui as informações são processadas  por um servidor web que interpretara e retornará o resultado que será exibido  no browser. Sendo assim não é possível visualizar o código de uma aplicação  rodando no <a href="http://pt.wikipedia.org/wiki/Server-side">Server-side</a>.</p>
<h3>E o PHP?</h3>
<p>O PHP é processado no servidor por isso é uma linguagem  Server-side. Sendo assim suas aplicações não poderão ser copiadas por outras  pessoas. Todos os processos, rotinas e funções serão feitas no servidor e o  usuário recebera apenas o resultado em seu browser.</p>
<h2>O que podemos fazer com o PHP</h2>
<h3>Interação com usuário</h3>
<p>Primeiramente transformação de sites estáticos, que não  possuem nenhum tipo de interação, em sites dinâmicos, com maior possibilidade  de interação e dinamismo. Por exemplo, com páginas estáticas não podemos ter  uma sessão de comentários em nosso site, em que ao terminar de ler um artigo a  pessoa preencha um campo no formulário e deixar sua opinião e no mesmo estante  a sua opinião estar no site, coisas que podemos realizar com o PHP e um banco  de dados.</p>
<h3>Facilidade na manutenção</h3>
<p>Imagine um site que tenha 10 itens no menu do site e cada  item abre mais 5 páginas internas, temos um total de 50 páginas. Agora imagine  a situação: Seu cliente liga para você e pede para inserir mais um item no menu,  lembrando que o menu esta presente em todas as páginas, o que você faria?  Provavelmente abriria as 50 páginas e iria copiando e colando o código do menu  entre elas, trabalho braçal bem chato né?, Além de possíveis erros. Mais  continuemos você inseriu o item no menu, deve ter pensado que o problema acabou,  mais não, no entanto no dia seguinte o item no menu que seu cliente havia  chamado de contato na realidade ele lhe enviou o nome errado pois o pessoal do  marketing descobriu que o nome fale conosco tem maior apelo com os clientes. E  lá vai você novamente para o mesmo trabalho braçal.</p>
<p>E se fosse noticias que devem ser inseridas 3 vezes ao dia?  Seu cliente mandaria a você, você as incluiria e sempre que houvesse erros você  teria que ir lá e corrigi-las. Além de ter uma chamada com todas as noticias  que você deveria atualizar também e uma chamada com foto na página inicial.  Processo chato para você e o cliente.</p>
<p>Com o PHP podemos separar no primeiro caso o menu em um  arquivo que ao ser atualizado seria atualizado em todo o site, pois este menu  seria inserido em todas as páginas pelo PHP.<br>
E no segundo caso das noticias  poderíamos criar uma área administrativa em que apenas usuários logados, os  administradores, teriam acesso e poderiam inserir e editar as noticias sem  precisar entrar em contato com você.</p>
<h3>PHP e o banco de dados</h3>
<p>O PHP possui acesso a diversos <a href="http://pt.wikipedia.org/wiki/Banco_de_dados">bancos de dados</a>. Sendo  assim você terá uma serie de funções para poder utilizar entre os <a href="http://www.php.net/manual/pt_BR/refs.database.php">diversos tipos de  bancos de dados suportados pelo PHP</a>. Em nosso aprendizado utilizaremos o <a href="http://www.mysql.com/">MySQL</a>.</p>
<h3>Exemplo de aplicações que podemos desenvolver com o PHP</h3>
<p>Com o PHP podemos desenvolver coisas como áreas restritas  que necessitem de autenticação, sistemas de comentários para artigos, noticias etc.  Envio de emails, sistemas de noticias, lojas virtuais, redes sociais e qualquer  outra coisa que você possa imaginar.<br>
  Uma aplicação web de grande porte que foi desenvolvida em PHP, foi a <a href="http://pt.wikipedia.org/wiki/P%C3%A1gina_principal">Wikipédia</a>. Nela  você encontra várias coisas como o sistema de autenticação, publicação e edição  de artigos, upload de fotos entre outros.</p>
