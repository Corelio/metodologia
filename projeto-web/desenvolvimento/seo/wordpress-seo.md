# Wordpress SEO by Yoast

## O plugin
O [Wordpress SEO](https://wordpress.org/plugins/wordpress-seo/) é um dos plugins mais conhecidos para ajudar no processo de otimização de um website montado em Wordpress. É gratuito e suas configurações são bem completas.



## Referências
[Guia completo do plugin Wordpress SEO da Yoast](https://imasters.com.br/cms/wordpress/guia-completo-do-plugin-wordpress-seo-da-yoast/)



## Configurações básicas
Por conter muitas opções de configuração, acabamos não utilizando 100% dos recursos, mas os citados abaixo são as configurações mais básicas e essenciais (algumas já são padrão do plugin, mas estão listadas também):

### Títulos e metadados
**Geral**
* ✔ Usar a tag meta keywords;
* ✔ Adicionar globalmente a tag meta robots noodp no website;
* ✔ Adicionar globalmente a tag meta robots noydir no website.

**Início**
* Modelo de título: %%sitename%% - %%sitedesc%%;
* Modelo de meta descrição: tagline do website;
* Modelo de meta palavras-chave: palavras-chave relativas ao website ([Veja as melhores práticas para o preenchimento deste campo](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/desenvolvimento.md#meta-keywords)).

#### Metadados de autor

* Autor em destaque: por padrão, selecionamos “don’t show”.

**Tipos de posts**
#### Posts

* Modelo de título: %%title%% - %%sitename%%;
* Modelo de meta-descrição: %%excerpt%%;
* Modelo de meta-palavras: %%tag%%, %%category%%.

##### Páginas

* Modelo de título: %%title%% - %%sitename%%
* Modelo de meta-descrição: %%excerpt%%;
* Modelo de meta-palavras: %%tag%%, %%category%%.

#### Media

* Modelo de título: %%title%% %%page%% %%sep%% %%sitename%%;
* Meta robots: ✔ noindex, follow.

**Taxonomias**

#### Categorias

* Modelo de título: %%term_title%% %%page%% - %%sitename%%;
* Modelo de meta-descrição: %%term_description%%.

#### Tags
* Modelo de título: %%title%% - %%sitename%%;
* Modelo de meta-descrição: %%tag_description%%.

#### Formato
* Modelo de título: %%term_title%% Archives %%page%% %%sep%% %%sitename%%;
* Meta robots: ✔ noindex, follow.

**Outros**

#### Arquivos de autor
* Modelo de título: %%name%%, Author at %%sitename%% %%page%%;
* Meta robots: ✔ noindex, follow.

#### Arquivo de datas
* Modelo de título: %%date%% %%page%% %%sep%% %%sitename%%;
* Meta robots: ✔ noindex, follow.

#### Páginas de busca
* Modelo de título: Você pesquisou por %%searchphrase%% %%page%% - %%sitename%%.

#### Páginas 404
* Modelo de título: Página não encontrada - %%sitename%%



### Social
* ✔ Adicionar metadados OpenGraph;
* Logue com o usuário genérico para administrar as aplicações ([Mais informações](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/desenvolvimento.md#cria%C3%A7%C3%A3o-de-aplicativo)).

#### Configurações da página inicial
* URL da imagem: Aponte o caminho externo de uma imagem 200x200px que represente de forma genérica o website;
* Descrição: Título completo do website.

#### Configurações padrão
* URL da imagem: Insira a URL da mesma imagem apontada acima, ela será utilizada no compartilhamento de publicações que não possuem imagem de destaque.


### Sitemap XML

* ✔ Habilite essa opção para ativar a funcionalidade de sitemap XML.

#### Configurações gerais

* ✔ Pingar o Yahoo.

#### Excluir tipos de posts

* ✔ Media (attachment).

#### Excluir taxonomias

* ✔ Tags (post_tag);
* ✔ Formato (post_format).

### Links permanentes

* ✔ Remover a base da categoria (normalmente /category/) das URLs de categorias.

### RSS

* Conteúdo a colocar no final de cada post do feed: O post %%POSTLINK%% apareceu primeiro em %%BLOGLINK%%

=


