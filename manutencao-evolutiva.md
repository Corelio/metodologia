# Manutenção evolutiva

Tudo que acontece depois que o projeto já foi entregue para o cliente, e ainda precisamos que atualizar.

## A2Projetos
### 2013.04.a2comunicacao

* URL: http://a2comunicacao.com.br/
* CMS: A2siteBox - http://a2comunicacao.com.br/a2sitebox/login/
* Hospedagem: Hostgator - https://financeiro.hostgator.com.br/
* Repositório GIT: 192.168.0.241:/Dados/A2Projetos/2013.04.a2comunicacao/www
* FTP
 * a2comunicacao.com.br
 * login: a2com691
 * Senha: p60vbK62gV
* Dependências:
 * Composer (deve ser instalado na pasta do projeto)
 * Grunt (deve ser instalado na pasta do tema)

#### Configurando o projeto:

1) Atualize/Baixe o projeto para sua máquina:
www-data@192.168.0.241:/Dados/A2Projetos/2013.04.a2comunicacao/www

2) Baixe a pasta /web/uploads do servidor, via FTP (ela não vem com o projeto)

3) Instale o composer na pasta raiz do projeto
via terminal: php composer.phar install

4) Instale o Grunt na pasta do tema (/web/themes/site)
via terminal: npm install

#### Atualizações no código CSS/JS

1) Rode o Grunt na pasta do tema (/web/themes/site)
via terminal, na pasta do tema: grunt w

2) Faça as modificações necessárias (o arquivo mimificado deve ser gerado automaticamente via grunt)

3) Suba os arquivos via FTP:

 * Se alterações de CSS: além dos arquivos modificados, suba o style.css (em /web/themes/site/css)

 * Se alterações de JS: além dos arquivos modificados, suba a pasta build (/web/themes/site/js/build) OBS. Essa pasta não vem com o projeto, é gerada automaticamente via grunt

 * Se alterações em templates: simplesmente suba os arquivos modificados
	
OBS. O site da A2 Comunicação tem cache ativado; após subir é preciso limpá-lo (ver instruções abaixo)

#### Limpando o cache no servidor

1) Acesse o FTP do site
via terminal: ssh [user-ftp]@a2comunicacao.com.br -p2222 (onde 2222 é o número da porta)

2) Responda (só no 1º acesso) Are you sure you want to continue connecting (yes/no)? Yes 

3) Entre com a password (do FTP)

4) Acesse: cd public_html 

5) Entre com a instrução de limpeza: rm -rf app/cache/* 


#### Atualizações da Equipe (seção Quem somos)

1) Salve a imagem original com o nome padronizado (nome_sobrenome.jpg) na pasta do projeto no servidor Design: 2013.04.a2comunicacao/design/imagens/Fotos novas da A2/Fotos da Equipe

2) Trate a imagem: 

 * a) abra o arquivo com as imagens tratadas todos.psd (na mesma pasta onde a imagem foi salva) e inclua a nova imagem

 * b) faça as modificações necessárias, de modo que a nova imagem fique com o aspecto semelhante às demais: com o fundo branco e leve “luz” alaranjanda

 * c) Salve a imagem final no tamanho 120x120 pixels, dentro da pasta 120x120_tratadas com o nome padronizado (nome_sobrenome.jpg)

3) Copie a imagem para a pasta do projeto /themes/site/img/equipe/

4) Edite o template /2013.04.a2comunicacao/app/Resources/SiteBundle/views/Templates/quem-somos.html.twig

 * a) Duplique o bloco ```<div class="thumb">```; 
Importante: repare que há um limite máximo de 6 membros por linha. Caso precise de uma nova linha, basta acrescentar ```<div class="linha-thumb"></div>``` após a última linha e então incluir o bloco na nova linha

 * b) Altere o nome, texto do curriculum, o caminho da imagem e salve o arquivo

5) Suba a imagem e o template para o servidor, via FTP

6) Execute a limpeza do cache e verifique a atualização no browser
