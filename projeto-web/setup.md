# Setup
O que é preciso para iniciar um projeto? Configurações de máquina, criação do projeto no Basecamp, frameworks etc.

## A2boilerplate

## A2siteBox
O a2siteBox é um gerenciador de conteúdo (CMS) criado e mantido pela A2 Comunicação, que tem como objetivo auxiliar na criação, edição e gestão de conteúdos para websites e aplicativos web de forma personalizada.

O desenvolvimento do projeto pode ser acompanhado no [GitHub da A2 Comunicação](https://github.com/a2comunicacao/A2SiteBox).

Todos os passos para instalação e contribuição com o projeto estão concentrados no repositório.

## Basecamp

### Boas práticas
1. Sempre comece o título de uma tarefa com um verbo no infinitivo: Fazer, Organizar, Analisar, Criar etc.:
![Sempre comece o título de uma tarefa com um verbo no infinitivo](http://lab.a2comunicacao.com.br/metodologia/basecamp_01.png)
2. Sempre que possível, associe uma lista de tarefas à uma meta:
![Sempre que possível, associe uma lista de tarefas a uma meta](http://lab.a2comunicacao.com.br/metodologia/basecamp_02.png)
3. Coloque o link da página que você estiver comentando, mesmo que seja um endereço bem conhecido. Para URLs com acesso restrito, sempre coloque usuário e senha para facilitar;
4. Evite duplicar o conteúdo de uma mensagem em mais de uma tarefa. Coloque o link de uma tarefa na outra. ([Veja um exemplo correto](https://a2comunicacao.basecamphq.com/projects/8083835-2011-09-educacao2/todo_items/165610841/comments#comment_241229133));
5. Para tarefas longas, é recomendado fazer um breve resumo diário do andamento nos comentários;
6. Não deixe de cadastrar as horas trabalhadas no dia seguinte, crie o hábito de fazer isso no final do dia;
7. Se duas ou mais pessoas são responsáveis pela mesma tarefa, é preciso dividí-la:
![Se duas ou mais pessoas são responsáveis pela mesma tarefa é preciso dividí-la](http://lab.a2comunicacao.com.br/metodologia/basecamp_03.png);
8. Não tenha receio de copiar muitas pessoas em um comentário. Além de copiar os envolvidos diretamente na tarefa, inclua a equipe de atendimento, os gerentes das áreas e outras pessoas que possam se beneficiar com a informação. Na dúvida, copie todos! Se a pessoa não deseja receber comentários, ela pode desativar essa opção ou mesmo se desligar daquele projeto;
9. Ao criar um novo projeto, de preferência por utilizar um modelo já existente ou crie um novo modelo caso seja necessário. ([Veja um exemplo](https://a2comunicacao.basecamphq.com/project_templates)).
10. Primeiro cadastre no Basecamp e depois execute a tarefa, não o contrário.

### Perguntas frequentes (FAQ)

#### Como nomear um novo projeto no Basecamp? 
* **Projetos novos**: Por padrão, os projetos são criados com base no ano e mês de desenvolvimento mais o nome do projeto, separados por pontos (Ex.: 0000.00.a2comunicacao);
* **Projetos em manutenção**: É preciso acrescentar o campo “manutencao” ao final do nome do projeto (Ex.” 0000.00.a2comunicacao.manutencao) ;
* **Projetos com equipes externas**: É incluir o termo “equipe” ao final do nome do projeto (Ex.: 0000.00.a2comunicacao.equipe).

#### É possível mover uma tarefa de um projeto para outro?
Sim. Veja como na [página de ajuda do Basecamp (em inglês)](http://help.37signals.com/basecamp/questions/340-can-i-move-items-from-one-basecamp-project-to-another).
#### O que fazer quando surgir uma tarefa de manutenção de um projeto que já foi entregue e arquivado?
Evite reabrir o projeto quando surgir uma tarefa após ele ser arquivado. Caso não existe nenhum contrato/projeto de manutenção relacionado, cadastre a tarefa em uma lista dentro do projeto interno da empresa (A2 Internas).

#### Quem pode criar um novo projeto e quando ele deve ser criado?
Apenas os administradores podem criar novos projetos e devem ser criados após a aprovação do mesmo.

## GIT
É um sistema de controle de versão para projetos. Consiste em arquivar seu projeto em um local único mas que possa ser replicado em seu ambiente local para que diversas pessoas possam trabalhar nele e, que essas alterações feitas em conjunto possam ser mescladas sem que se percam dados sem aviso prévio.

Atualmente os projetos da A2 Comunicação são criados e arquivados no ambiente **192.168.0.241**.

### Clonagem de repositórios

#### XAMPP (MAC OS X)

**Configurando no MAC OS X**

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

### Softwares recomendados

* [Source Tree - MAC OS X](http://www.sourcetreeapp.com/)

## GitHub Pages
Ao criarmos um repositório no GitHub, temos a possiblidade de desenvolvermos uma “GitHub Page”. Geralmente, é utilizada para reunir as informações e documentação sobre o repositório.

### Por que?

Além de estar integrada ao repositório, um outro ponto positivo é que ela é hospedada pelo próprio GitHub, sem a necessidade de utilizarmos nenhum upload via FTP.

### Como?
1. No seu repositório, crie um _branch_ novo chamado _gh-pages_. Pode ser diretamente pelo site do GitHub ou via terminal: `git branch gh-pages`;
2. Caso você tenha criado o repositório direto pelo site do GitHub, atualize o seu repositório local com o novo _branch_ e altere o ambiente de desenvolvimento para o recém-criado  _gh-pages_; se você utilizou o terminal, altere seu ambiente de desenvolvimento para o novo _branch_: `git checkout gh-pages`;
3. Após isso, é só iniciar o desenvolvimento da página. Vale lembrar que o servidor do GitHub para as _gh-pages_ não aceita nenhuma linguagem de servidor (PHP, Ajax etc.). Portanto, nossos arquivos devem ser com a extensão _.html_ e, caso usemos _javascript_, não poderemos utilizar nenhuma requisição Ajax;
4. Finalizada a página, é só seguir o processo padrão de atualização de um repositório;
5. Feito isso, a _gh-page_ é automaticamente publicada no endereço: _usuario.github.io/repositorio_.

### Workflow

São 2 os workflows utilizados em projetos na A2 Comunicação:

* Em **projetos antigos** (até o início do segundo semestre de 2013) o workflow utilizado era o _Centralized Workflow_, onde somente o _branch master_ é utilizado e concentra todas as atualizações do projeto;
* Nos **projetos iniciados após esse período** são utilizados o [Gitflow Workflow](https://www.atlassian.com/git/workflows#!workflow-gitflow) para projetos complexos e que necessitam de maior controle, como o A2siteBox, por exemplo, e o [Feature Branch Workflow](https://www.atlassian.com/git/workflows#!workflow-feature-branch) para projetos com menos complexidade.

=

## Grunt
Basicamente o Grunt é um automatizador de tarefas. Utilizamos ele para agilizar algumas tarefas comuns no desenvolvimento de um projeto e adotamos o uso dele no [A2boilerplate](https://github.com/a2comunicacao/metodologia/blob/master/a2lab/a2lab.md#a2boilerplate). Pra instalá-lo em sua máquina, você precisa do [NodeJS](http://www.voltsdigital.com.br/labs/gruntjs-por-onde-comecar/) e NPM. Na prática, você instala _plugins_ e configura tarefas que rodarão através de comandos. As tarefas que costumamos utilizar são:

* **_imagemin_**: Reduz tamanho de imagens;
* **_svg2png_**: Converte SVGs em PNGs para utilização em browsers que não tem suporte para SVG;
* **_copy_**: Copia arquivos de uma pasta para outra;
* **_concat_**: Concatena arquivos (utilizamos principalmente para arquivos JS);
* **_uglify_**: Minifica arquivos JS;
* **_jshint_**: Valida arquivos JS;
* **_sass_**: Realiza tarefa do pré-processador SASS;
* ***browser_sync***: Levanta um servidor e sincroniza todos os dispositivos que acessarem determinado IP (ótimo para testes _cross-devide_);
* **_watch_**: Atualiza a página automaticamente conforme arquivos são salvos (funciona em complemento com o plugin [LiveReload](http://livereload.com/)). 



## Mac OS X

### Como configurar máquinas virtuais com Windows

1. Baixe e instale a [Virtual Box](https://www.virtualbox.org/wiki/Downloads);
2. Após instalar, crie uma nova máquina, clicando em _new_;
3. Nomeie a máquina virutal e selecione a versão do Windows que irá instalar (estamos utilizando a versão 7 de 64bit);
4. Defina 512mb de memória;
5. Crie um novo disco rígido selecionando _create hard drive_;
6. Selecione a opção _VDI (virtual box)_;
7. Selecione _dinamically allocated_;
8. Selecione um espaço mínimo de 20gb para o drive, caso contrário não será possível instalar os softwares básicos na máquina;
9. Inicie a máquina e aponte o arquivo de instação do Windows (ele está arquivado em _webhost > design > biblioteca > softwares > vm windows_;
10. Escolha a versão do Windows novamente (windows 7 professional) e faça a instalação personalizada, apontando para o drive criado anteriormente;
11. Após a instalação, basta inserir os dados básicos de usuário e rede;
12. Para ativar o Windows, rode na máquina virtual um executável que está dentro do arquivo .dmg de instalação, utilizando uma [pasta compartilhada](#mac1)

=

### <a name="mac1"></a>Como criar uma pasta compartilhada com a Virtual Box

1. Abra a Virtual Box e selecione no menu superior: _devices > insert guest additions_, selecione o .exe indicado e instale com suas configurações básicas;
2. Crie uma pasta no Mac com os arquivos que deseja transferir para a máquina virtual;
3. Volte na Virtual Box, e no menu superior selecione: _devices > share folder settings_;
4. Clique no botão “+”, selecione “Other” e aponte a pasta criada no Mac e seus arquivos ficarão acessíveis também na máquina virtual.

