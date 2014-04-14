# GitHub Pages

Ao criarmos um repositório no GitHub, temos a possiblidade de desenvolvermos uma “GitHub Page”. Geralmente, é utilizada para reunir as informações e documentação sobre o repositório. Além de estar integrada ao repositório, um outro ponto positivo é que ela é hospedada pelo próprio GitHub, sem a necessidade de utilizarmos nenhum upload via FTP.

## Como usar?
1. No seu repositório, crie um _branch_ novo chamado _gh-pages_. Pode ser diretamente pelo site do GitHub ou via terminal: `git branch gh-pages`;
2. Caso você tenha criado o repositório direto pelo site do GitHub, atualize o seu repositório local com o novo _branch_ e altere o ambiente de desenvolvimento para o recém-criado  _gh-pages_; se você utilizou o terminal, altere seu ambiente de desenvolvimento para o novo _branch_: `git checkout gh-pages`;
3. Após isso, é só iniciar o desenvolvimento da página. Vale lembrar que o servidor do GitHub para as _gh-pages_ não aceita nenhuma linguagem de servidor (PHP, Ajax etc.). Portanto, nossos arquivos devem ser com a extensão _.html_ e, caso usemos _javascript_, não poderemos utilizar nenhuma requisição Ajax;
4. Finalizada a página, é só seguir o processo padrão de atualização de um repositório;
5. Feito isso, a _gh-page_ é automaticamente publicada no endereço: _usuario.github.io/repositorio_.

## Workflow

São 2 os workflows utilizados em projetos na A2 Comunicação:

* Em **projetos antigos** (até o início do segundo semestre de 2013) o workflow utilizado era o _Centralized Workflow_, onde somente o _branch master_ é utilizado e concentra todas as atualizações do projeto;
* Nos **projetos iniciados após esse período** são utilizados o [Gitflow Workflow](https://www.atlassian.com/git/workflows#!workflow-gitflow) para projetos complexos e que necessitam de maior controle, como o A2siteBox, por exemplo, e o [Feature Branch Workflow](https://www.atlassian.com/git/workflows#!workflow-feature-branch) para projetos com menos complexidade.
