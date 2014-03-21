#Facebook
## Como usar as open graph meta tags do Facebook em um website

## Criação de aplicativo no Facebook
Para a criação do aplicativo é necessário uma conta de desenvolvedor (autenticada por código enviado via SMS ou número de cartão de crédito). [Temos uma conta genérica para esse fim - dados na wiki interna](http://wiki.a2/index.php/Senhas_da_A2_em_sites_e_aplicativos).

1. Acesse o [Facebook Developers](http://developers.facebook.com/) e clique em _App_ no menu superior;
2. No topo a direita, clique em _+Criar novo aplicativo_;
3. Entre com os dados especificados abaixo e clique em _Continuar_;
* Nome do aplicativo: o título do website ou projeto;
* Espaço de nome do aplicativo: o título, sem espaço e caracteres especiais.
4. Nessa tela são exibidas as informações básicas do aplicativo criado. *Atenção para os dados _App ID_ e _App secret_: eles poderão ser solicitados para futuras integrações entre aplicativos*;
5. Aqui ainda precisamos apontar o modo como o aplicativo vai se integrar com o Facebook, clique em _Site com login do Facebook_ e entre com a _URL_ do website. Salve as alterações;
6. Agora precisamos configurar algumas Ações e Objetos: as ações que as pessoas poderão executar no aplicativo e com quais objetos elas poderão interagir (isso é necessário para a publicação correta na Linha do tempo e no Feed de notícias);
* Clique em _Open graph_ > _Tipos_;
* Clique em _Adicionar um novo tipo de ação_ e selecione uma ação (read / News, por exemplo) e clique em _Enviar_;
* Por último, ações poderão ser definidas (recomendadas: like, listen, read, watch - os objetos serão automaticamente incluídos).

## Integração do aplicativo do Facebook com o Wordpress

