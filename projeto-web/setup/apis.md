# APIs
Na criação de websites e aplicações em geral, é comum haver integrações com serviços externos, sejam eles com intuito social. Abaixo listamos os APIs de serviço que comumente utilizamos e como criar chaves para utilizá-los.


**Índice**

* [Google APIs](#apis1)
	* [Criando API Keys](#apis2)
	* [Google Maps](#apis3)
	* [Youtube](#apis4)
	* [Google Custom Search](#apis5)
* [Twitter](#apis6)
	* [Criando API Keys](#apis7)
* [Referências](#apis8)

=

## <a name="apis1"></a>Google APIs

O Google possui uma infinidade de serviços disponíveis para desenvolvedores. No entanto todos eles podem ser ativados com uma única chave.

### <a name="apis2"></a>Criando API keys
Chaves de API do Google são necessårias para serviços pagos e grátis com limite de cota. A criação de uma chave é simples, sendo realizada a partir dos seguintes passos:

1. Acesse o Could Console;
2. Crie um novo projeto clicando no botão _Create Project_;
3. Clique na seção _APIs & Auth_ localizada na barra lateral;
4. Ative as APIs necessárias;
5. Clique na seção _Credentials_ localizada na barra lateral;
6. Crie uma nova chave clicando no botão _Create new key_;
7. Selecione o tipo de chave
	* **_Server key_**: para utilização no back-end;
	* **_Browser key_**: para utilização no front-end;
	* **_Android key_**: para aplicações Android;
	* **_iOS key_**: para aplicações iOS.
8. Indique os hosts ou IPs que podem utilizar a chave;
9. Utilize a _API key_ para realizar a autenticação das APIs.


### <a name="apis3"></a>Google Maps
Utilizamos a API do Google Maps tanto para realizar busca de coordenadas para endereços, quanto para exibir mapas interativos e personalizados nos websites de clientes. A API permite a personalização e manipulação de mapas, tendo todas as funcionalidades de navegação presente no Google Maps.


### <a name="apis4"></a>Youtube
A API do Youtube permite que criemos listagens de vídeos dos canais de nossos clientes ou de playlists que eles criarem.


### <a name="apis5"></a>Google Custom Search
A API do Google Custom Search permite que nossos meios de busca obtenham resultados tão relevantes quanto a busca do Google, dispensando na maioria dos casos o processamento bruto de dados para retornar os resultados.

A busca pode ser utilizada apenas em um _client-side_ ou _server-side_ utilizando sua API. Pada cadastrar os dados da busca, é necessário registrar um novo método de busca no Google CSE, obtendo assim o _embed_ para utilização _client-side_ e o _CX_ para utilização _server-side_.

Em utilização _server-side_ com o Symfony Framework é possível facilmente a busca com o [Google CSE Bundle](https://github.com/williancarminato/GoogleCseBundle), criado pelo [Willian Carminato](https://twitter.com/willcampideli).




## <a name="apis6"></a>Twitter
O twitter é uma das maiores e mais utilizadas redes sociais do mundo. Sua poderosa API é utilizada por milhares de aplicações. Utilizamos a API do Twitter para criar boxes de timeline personalizadas. No entando, com a API do Twitter se tem acesso à tweets de usuários, timeline de menções, timeline pessoal, manipulação de tweets (criação, visualização, detalhes e exclusão), busca relevante, manipulação de mensagens diretas, informações sobre seguidores e amizades, entre diversas outras funcionalidades.

### <a name="apis7"></a>Criando API keys

As chaves de usuário são necessárias tanto para aplicações back-end quanto aplicações front-end, e podem ser obtidas ao cadastrar um aplicativo na [central de aplicativos](https://apps.twitter.com/).

1. Faça login na central de aplicativos;
2. Clique no link _Create new app_;
3. Preencha os dados da aplicação e clique no botão _Create your Twitter application_;
4. Modifique as permissões do app se necessário, clicando no link _modify app permisions_;
5. Utilize a _API key_ para realizar a autenticação nos aplicativos.

## <a name="apis8"></a>Referências

* [Padrão para criar uma API JSON](http://jsonapi.org/)

