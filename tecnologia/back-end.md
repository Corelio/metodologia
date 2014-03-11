# Back-end

## A2siteBox

O A2siteBox é um gerenciador de conteúdo (CMS) criado e mantido pela A2 Comunicação que tem como objetivo auxiliar na criação, edição e gestão de conteúdos para websites e aplicativos web de forma personalizada.

O desenvolvimento do projeto pode ser acompanhado no Github da A2Comunicação: <code>https://github.com/a2comunicacao/A2SiteBox</code>

Todos os passos para instalação e contribuição com o projeto estão concentrados no repositório.

## WordPress

## Git

### Clonagem de repositórios no servidor interno Doors usando XAMPP no MAC

1. Para clonar, no Source Tree aponte o caminho: www-data@192.168.0.241:/Dados/A2Projetos/nomedoprojeto/www . Aponte para a pasta onde serão instalados os websites, no MAC configurei o XAMPP para apontar para a pasta "Sites" e sempre os nomeio com o mesmo nome da Doors;

2. Para criar o ambiente local, abra a pasta Xampp dentro de Aplicativos: Xampp > etc > extra > httpvhosts.conf e edite o arquivo inserindo o código apontando a pasta onde o site foi instalado (para facilitar, nomeio sempre como local.nomedoprojeto.a2 - pois para ver se tudo está ok na Doors, só retiro o termo local da url): 

	``<VirtualHost 127.0.0.1> 
	ServerName local.pastadoprojetoclonado
	DocumentRoot "/Users/Vivian/Sites/pastadoprojetoclonado" 
	<Directory "/Users/Vivian/Sites/pastadoprojetoclonado"> 
	    Options Indexes FollowSymLinks Includes ExecCGI 
	    AddType text/shtml .shtml 
	    AddOutputFilter INCLUDES .shtml 
	    AllowOverride All 
	    Order allow,deny 
	    Allow from all 
	</Directory> 
	</VirtualHost>``

3. Para terminar de configurar o domínio local, abra o Terminal e digite o comando: 
sudo/applications/textedit.app/contents/macOS/textedit/etc/hosts
Digite sua senha, e insita a url que você vai utilizar entre as linhas "127.0.0.1    localhost" e "255.255.255.255    broadcasthost".

4. Inicie ou reinicie o XAMPP para que funcione. 

5. Se por um acaso mesmo assim aparecer algum outro site no lugar: desligue o XAMPP, abra novamente o Terminal, e limpe o cache da máquina: dscacheutil -flushcache.

6. Reinicie o XAMPP.


## GitHub pages

Ao criarmos um repositório no GitHub, temos a possibilidade de desenvolvermos uma 'GitHub page'. Geralmente, é utilizada para reunir as informações e documentação sobre o repositório.

### Por que?

Além de estar integrada ao repositório, um outro ponto positivo, é que ela é hospedada pelo próprio GitHub, sem a necessidade de utilizarmos nenhum upload via _FTP_.

### Como?

1. No seu repositório, crie um **branch** novo chamado _gh-pages_. Pode ser diretamente pelo site do GitHub, ou via terminal:
`git branch gh-pages`
2. Caso você tenha criado o repositório direto pelo site do GitHub, atualize o seu **repositório local** com o novo _branch_ e altere ambiente de desenvolvimento para o recém-criado **gh-pages**; se você utilizou o terminal, altere seu ambiente de desenvolvimento para o novo _branch_:
`git checkout gh-pages`
3. Após isso, é só iniciar o desenvolvimento da página. Vale lembrar que o servidor do GitHub para as _gh-pages_ não aceita nenhuma linguagem de servidor (_PHP_, _Ajax_ ..). Portanto, nossos arquivos devem ser com a extensão `.html` e caso usemos `javascript` não poderemos utilizar nenhuma requisição Ajax.
4. Finalizada a(s) páginas(s), é só seguirmos os processos padrões de atualização de um repositório.
5. Feito isso, a _gh-page_ é automaticamente pubilicada no endereço:
_usuario.github.io/repositorio_

