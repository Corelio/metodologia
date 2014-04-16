# Facebook

## Criação de aplicativo 
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

## Como usar as Open Graph meta tags
#### 1) Crie um aplicativo no Facebook
Opcional. Porém altamente recomendado, principalmente se você precisa ter um controle maior das configurações de compartilhamento. Veja [Criação de aplicativo](#cria%C3%A7%C3%A3o-de-aplicativo).

#### 2) Inclua as Open Graph meta tags no ```<head>``` do HTML

	<meta property=“fb:app_id” content=“ID do aplicativo no Facebook”>
	<meta property="og:site_name” content=“O nome do website”>
	<meta property="og:type” content=“Tipo do conteúdo”>
	<meta property="og:title" content=“O título do artigo”>
	<meta property="og:url” content=“URL do artigo”>
	<meta property="og:description" content="A descrição do artigo.”>
	<meta property="og:image" content=“URL da imagem do artigo”>

#### 3) Declare os namespaces necessários
Para o Facebook analisar a página HTML corretamente, é preciso adicionar os [namespaces](http://www.w3schools.com/xml/xml_namespaces.asp) do Open Graph:

	<head prefix="og: http://ogp.me/ns# fb: http://ogp.me/ns/fb#>

#### 4) Teste

* [Usuário Genérico](https://www.facebook.com/usuario.generico.9)
* email: a2teste@a2comunicacao.com.br
* senha: a2@345box

### Boas práticas
* Use as [OG meta tags apropriadas](https://developers.facebook.com/docs/opengraph/howtos/maximizing-distribution-media-content#tags)
* Declare o [ID do aplicativo do Facebook](https://help.yahoo.com/kb/yahoo-merchant-solutions/facebook-application-sln18861.html) 
* Inclua os [namespaces necessários](http://www.geoffhayward.eu/blog/you-can-validate-open-graph-metadata)
* Defina [imagens nos tamanhos recomendados](https://developers.facebook.com/docs/plugins/checklist/#images)
* Use o [Debug Tool](https://developers.facebook.com/tools/debug/)

### Truques e Dicas

* Por padrão, o aplicativo do Facebook é criado em modo sandbox. Ou seja, ele é acessível somente ao desenvolvedor e usuários com permissão. É necessário [desativar o modo sandbox](http://stackoverflow.com/questions/20706322/how-to-disable-sandbox-mode-for-app-in-new-facebook-developer) para que o aplicativo se torne visível e utilizável a todos.
* O Facebook guarda cache das definições das OG meta tags; usando o Debug Tool você também reinicia essas configurações
* A meta tag "author" interfere no Facebook, fazendo com que o conteúdo compartilhado seja atriuído ao autor declarado nela
* Para evitar cortes nas imagens de thumbnail dos compartilhamentos, procure mantê-las na proporção de 1.91:1
* Teste os compartilhamentos de 2 formas: usando o botão *like/share* e também copiando e colando o link direto no Facebook
* Use caminho absoluto na declaração de OG meta tags; caso contrário, não vão funcionar


### Referências

* [An introduction to using Facebook's Open Graph protocol](http://engageinteractive.co.uk/blog/an-introduction-to-using-facebooks-open-graph-protocol)
* [Utilizando as meta tags do Facebook](http://tableless.com.br/utilizando-meta-tags-facebook/)
* [The Open Graph Protocol](http://ogp.me/)  
* [Facebook Sharing Checklist](https://developers.facebook.com/docs/plugins/checklist/)  
* [OG Object Types](http://ogp.me/#types)
* [You Can Validate Open Graph Metadata](http://www.geoffhayward.eu/blog/you-can-validate-open-graph-metadata)
* [XML Namespaces](http://www.w3schools.com/xml/xml_namespaces.asp)  
