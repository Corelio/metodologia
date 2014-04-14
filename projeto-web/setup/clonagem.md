# Clonagem de repositórios
Consiste em arquivar seu projeto em um local único mas que possa ser replicado em seu ambiente local para que diversas pessoas possam trabalhar nele e, que essas alterações feitas em conjunto possam ser mescladas sem que se percam dados sem aviso prévio.

Atualmente os projetos da A2 Comunicação são criados e arquivados no ambiente **192.168.0.241**.

## Softwares recomendados

### [Source Tree - MAC OS X](http://www.sourcetreeapp.com/)

### [XAMPP - MAC OS X](https://www.apachefriends.org/pt_br/index.html)

1. No Source Tree, aponte o caminho onde o projeto está arquivado seguindo a seguinte estrutura: `www-data@192.168.0.241:/Dados/A2Projetos/nomedoprojeto/www`;
2. Aponte no seu ambiente local onde o website será arquivado conforme sua preferência. Normalmente no MAC utilizando a pasta "Sites";
3. Defina uma URL local para seu website clonado. Abra o Terminal e digite o comando: `sudo /Applications/TextEdit.app/Contents/MacOS/TextEdit /etc/hosts` e insira a URL entre as linhas "127.0.0.1 localhost" e "255.255.255.255 broadcasthost". Sugerimos para sua URL a extensão **local.nomedoprojeto.a2**;
4. Agora precisamos dizer ao XAMPP que arquivos pegar para construir o website. Acesse _Aplicativos > XAMPP > etc > extra > httpvhosts.conf_ e edite o arquivo inserindo o código que aponta onde o website foi instalado:

` <VirtualHost *:80>
ServerName local.nomedoprojeto.a2
DocumentRoot /Users/vivianoliveira/Sites/nomedoprojeto
  <Directory "/Users/vivianoliveira/Sites/nomedoprojeto">
        	Options Indexes FollowSymLinks
        	AllowOverride All
        	Order allow,deny
        	Allow from all
    	</Directory>
</VirtualHost>`

![Arquivo httpvhosts.conf](http://lab.a2comunicacao.com.br/metodologia/git_01.png)

Obs.: Após essas configurações, inicie ou reinicie seu XAMPP. Caso encontre problemas, (o site não carrega ou carrega um outro site, por exemplo) abra novamente o terminal e limpe o cache de sua máquina com o comando: 'dscacheutil -flushcache` e reincie o XAMPP.

