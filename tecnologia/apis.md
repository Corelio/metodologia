# APIs

Na criação de sites e aplicações em geral é comum haver integrações com serviços externos, sejam eles com intuíto social, de armazenamento ou multimídia.
Abaixo irei listar APIs de serviço que comumente utilizamos e como criar chaves para utilizá-las.

## Google APIs
O Google possui uma infinidade de serviços disponíveis para desenvolvedores. No entanto todos eles podem ser ativados com uma única chave.

APIs utilizadas:

* Google Maps
* Youtube
* Google Custom Search

### Google Custom Search

A API do Google Custom Search permite que nossos meios de busca obtenham resultados tão relevantes quando a busca do Google, dispensando na maioria dos casos processamento bruto de dados para retornar os resultados.

### Youtube

A API do Youtube permite que criemos listagens de vídeos dos canais de nossos clientes ou de playlists que eles criarem.

### Google Maps

Utilizamos a API do Google Maps tanto para realizar busca de coordenadas para endereços, quanto para exibir mapas interativos e personalizados nos sites de clientes. A API permite a personalização e manipulação de mapas, tendo todas as funcionalidades de navegação presente no Google Maps.

### Criando API keys

Chaves de API do Google são necessárias para serviços pagos e serviços grátis com limites de cota.
A criação de uma chave é simples, sendo realizada a partir dos passos abaixo:

1. Acesse o [Cloud Console](https://console.developers.google.com)
2. Crie um novo projeto clicando no botão `Create Project`
3. Clique na seção `APIs & Auth` localizada na barra lateral
4. Ative as APIs necessárias
5. Clique na seção `Credentials`  localizada na barra lateral
6. Crie uma nova chave clicando no botão `Create new key`
7. Selecione o tipo de chave
 * `Server key` para utilização no backend
 * `Browser key` para utilização no frontend
 * `Android key` para aplicações Android
 * `iOS key` para aplicações iOS
8. Indique os hosts ou IPs que podem utilizar a chave

## Twitter

O Twitter é uma das maiores e mais utilizadas redes sociais do mundo. Sua poderosa API é utilizada por milhares de aplicações. Utilizamos a API do Twitter para criar boxes de timeline personalizados.
No entanto com a API do Twitter se tem acesso a tweets de usuários, timeline de menções, timeline pessoal, manipulação de tweets (criação, visualização, detalhes e exclusão), busca relevante, manipulação de mensagens diretas, informações sobre seguidores e amizades, entre diversas outras funcionalidades.

### Criando API keys no Twitter

As chaves de usuário são necessárias tanto para aplicações backend quando aplicações frontend, e podem ser obtidas ao cadastrar um aplicativo na [central de aplicativos](https://apps.twitter.com/).
