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

