

## Redes sociais
### Facebook

#### Como usar OpenGraph metatags

#### Criação de aplicativo 
Para a criação do aplicativo, é necessário uma conta de desenvolvedor (autenticada por código enviado via SMS ou número de cartão de crédito). [Temos uma conta genérica para esse fim - Dados na Wiki](http://wiki.a2/index.php/Senhas_da_A2_em_sites_e_aplicativos)

1. Acesse o [Facebook Developers](https://developers.facebook.com/) e clique em _App_ no menu superior;
2. No topo a direita, clique em _+Criar novo aplicativo_;
3. Entre com os dados especificados abaixo e clique em _Continuar_;
4. **Nome do aplicativo**: o título, sem espaço e caracteres especiais;
5. **Espaço de nome do aplicativo**: o título, sem espaço e caracteres especiais;
6. Nessa tela são exibidas as informações básicas do aplicativo criado. **Atenção para os dados _App ID_ e _App Secret_: eles poderão ser solicitados para futuras integrações entre aplicativos;
7. Aqui ainda precisamos apontar o modo como o aplicativo vai se integrar com o Facebook, clique em _Site com login do Facebook_ e entre com a URL do website. Salve as alterações;
8. Agora precisamos configurar algumas _Ações_ e _Objetos_: as ações que as pessoas poderão executar no aplicativo e com quais objetos elas poderão interagir (isso é necessário para a publicação correta na Linha do Tempo e no Feed de Notícias);
9. Clique em _Open graph > Tipos_;
10. Clique em _Adicionar um novo tipo ação_ e selecione uma ação (read / News, por exemplo) e clique em _Enviar_;
11. Por último, ações poderão ser definidas (recomendadas: like, listen, read, watch - os objetos serão automaticamente incluídos).

#### Integração do aplicativo com Wordpress

=

### Twitter
### Youtube
### Google+

=

### Disqus

#### Instalação
1. [Criar uma conta](https://disqus.com/profile/signup/) para poder usar o serviço;
2. Logar e clicar em [_Dashboard_](http://disqus.com/dashboard/);
3. Em _your sites_, clique em “[Add](https://disqus.com/admin/signup/)” para adicionar o site que vai receber o plugin.

#### Wordpress

1. No painel esquerdo do seu administrador Wordpress, selecione _Plugins > Adicionar novo_;
2. Procure por _Disqus Comment System_;
3. Selecione _Instalar agora > Ativar plugin_;
4. Clique em _Configure_ e logue com usuário e senha que você criou;
5. Selecione o site que você configurou no Disqus.

Obs.: Se já existir comentários nos posts e você quiser exportá-los para o disqus, clique em _Plugin settings_ no canto superior direito da tela, role a tela até _Import and Export_ e clique em _Export Comments_.

#### Universal Code

1. Clique em _Dashboard_;
2. Em _Your Sites_, clique no link do website que você criou;
3. Clique em _Settings > Install > Universal Code_;
4. E siga os procedimentos informados.

=

## SEO 
### Metatags
As metatags oferecem informações sobre o website para os mecanismos de busca e devem ser inseridas no _head_ do código.
#### Utilizando as metatags
##### Meta description
* Seja claro e honesto com o conteúdo/serviço do website;
* Se o website possuir uma tagline, coloque na meta description;
* Não ultrapasse 160 caracteres.

##### Meta keywords
* Liste as keywords mais óbvias relacionadas ao website;
* Procure por sinônimos dessas palavras utilizando o [Google Adwords Keywords Tools](https://adwords.google.com/KeywordPlanner) valorizando aquelas que tem maior busca;
* Procure e utilize as keywords que os concorrentes usam, para diminuir a força deles;
* Não ultrapasse 30 keywords.

##### Title
O title não é necessariamente uma metatag, mas como é exibido nos resultados de pesquisa, é importante não esquecer de preenchê-lo.

#### Referências
[Metatags - Ferramentas do Gogle para webmasters](https://support.google.com/webmasters/answer/79812?hl=pt-BR)

=

### Ranking de SERP

#### Ferramenta para análise
[Whats my SERP](http://www.whatsmyserp.com/)
#### Análises feitas
[Rodoanel](https://a2comunicacao.basecamphq.com/projects/9257684-2012-02-saopaulosp-equipe/todo_items/159233699/comments)

=

### Wordpress SEO by Yoast

#### O plugin
O [Wordpress SEO](https://wordpress.org/plugins/wordpress-seo/) é um dos plugins mais conhecidos para ajudar no processo de otimização de um website montado em Wordpress. É gratuito e suas configurações são bem completas.

#### Referências
[Guia completo do plugin Wordpress SEO da Yoast](https://imasters.com.br/cms/wordpress/guia-completo-do-plugin-wordpress-seo-da-yoast/)

#### Configurações básicas
Por conter muitas opções de configuração, acabamos não utilizando 100% dos recursos, mas os citados abaixo são as configurações mais básicas e essenciais (algumas já são padrão do plugin, mas estão listadas também):

##### Títulos e metadados
**Geral**
* ✔ Usar a tag meta keywords;
* ✔ Adicionar globalmente a tag meta robots noodp no website;
* ✔ Adicionar globalmente a tag meta robots noydir no website.

**Início**
* Modelo de título: %%sitename%% - %%sitedesc%%;
* Modelo de meta descrição: tagline do website;
* Modelo de meta palavras-chave: palavras-chave relativas ao website ([Veja as melhores práticas para o preenchimento deste campo](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/desenvolvimento.md#meta-keywords)).

###### Metadados de autor

* Autor em destaque: por padrão, selecionamos “don’t show”.

**Tipos de posts**
###### Posts

* Modelo de título: %%title%% - %%sitename%%;
* Modelo de meta-descrição: %%excerpt%%;
* Modelo de meta-palavras: %%tag%%, %%category%%.

####### Páginas

* Modelo de título: %%title%% - %%sitename%%
* Modelo de meta-descrição: %%excerpt%%;
* Modelo de meta-palavras: %%tag%%, %%category%%.

###### Media

* Modelo de título: %%title%% %%page%% %%sep%% %%sitename%%;
* Meta robots: ✔ noindex, follow.

**Taxonomias**

###### Categorias

* Modelo de título: %%term_title%% %%page%% - %%sitename%%;
* Modelo de meta-descrição: %%term_description%%.

###### Tags
* Modelo de título: %%title%% - %%sitename%%;
* Modelo de meta-descrição: %%tag_description%%.

###### Formato
* Modelo de título: %%term_title%% Archives %%page%% %%sep%% %%sitename%%;
* Meta robots: ✔ noindex, follow.

**Outros**

###### Arquivos de autor
* Modelo de título: %%name%%, Author at %%sitename%% %%page%%;
* Meta robots: ✔ noindex, follow.

###### Arquivo de datas
* Modelo de título: %%date%% %%page%% %%sep%% %%sitename%%;
* Meta robots: ✔ noindex, follow.

###### Páginas de busca
* Modelo de título: Você pesquisou por %%searchphrase%% %%page%% - %%sitename%%.

###### Páginas 404
* Modelo de título: Página não encontrada - %%sitename%%

##### Social
* ✔ Adicionar metadados OpenGraph;
* Logue com o usuário genérico para administrar as aplicações ([Mais informações](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/desenvolvimento.md#cria%C3%A7%C3%A3o-de-aplicativo)).

###### Configurações da página inicial
* URL da imagem: Aponte o caminho externo de uma imagem 200x200px que represente de forma genérica o website;
* Descrição: Título completo do website.

###### Configurações padrão
* URL da imagem: Insira a URL da mesma imagem apontada acima, ela será utilizada no compartilhamento de publicações que não possuem imagem de destaque.

#### Sitemap XML

* ✔ Habilite essa opção para ativar a funcionalidade de sitemap XML.

###### Configurações gerais

* ✔ Pingar o Yahoo.

###### Excluir tipos de posts

* ✔ Media (attachment).

###### Excluir taxonomias

* ✔ Tags (post_tag);
* ✔ Formato (post_format).

##### Links permanentes

* ✔ Remover a base da categoria (normalmente /category/) das URLs de categorias.

##### RSS

* Conteúdo a colocar no final de cada post do feed: O post %%POSTLINK%% apareceu primeiro em %%BLOGLINK%%

=


