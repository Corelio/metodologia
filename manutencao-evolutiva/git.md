# GIT

## Padronização de _commits_

Por padrão, os _commits_ deverão ser na língua inglesa.

Na fase de manutenção, os _commits_ deverão seguir o padrão abaixo com o objetivo de gerir relatórios e estatísticas.

* [**perfomance**] _tarefas relacionadas à perfomance do projeto (aplicação ou site)_
   * pages
   * posts
   * media
* [**security**] _tarefas relacionadas à segurança_
   * webserver _(.htaccess, Apache, Mod security)_
   * application _(relacionada à aplicação, como um módulo de usuários)_
* [**usability**] _tarefas relacionadas à questões de usabilidade/design/desenvolvimento do projeto_
   * content _(ajustes de conteúdo, como troca de textos e imagens)_
   * pages _(ajustes gerais de CSS/HTML/JS nas páginas do projeto)_
   * posts _(semelhante ao anterior, porém apenas aplicado em post/notícias)_

Um exemplo de utilização:

Bugfix - [**performance**][**media**] - Removing unused thumbnail creation call

Obs: Lembre-se sempre de colocar o "Bugfix" no início.
