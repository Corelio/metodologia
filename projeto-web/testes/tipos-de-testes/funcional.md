# Funcional
Testes funcionais estão relacionados a entrada e saída de dados. Clicar em links, preencher um cadastro e realizar uma busca são entrada de dados feitas pelos usuários na expectativa de obter uma resposta satisfatória do software.

## Checklist
* [Verificar links quebrados](https://github.com/a2comunicacao/metodologia/blob/master/manutencao-evolutiva/manutencao-evolutiva.md#verifica%C3%A7%C3%A3o-de-links) na barra de navegação e no corpo do texto usando a extensão [Link Checker](https://addons.mozilla.org/pt-br/firefox/addon/linkchecker/) (Firefox) ou [Check my links](https://chrome.google.com/webstore/detail/check-my-links/ojkcdipcgfaekbeaelaapakgnjflfglf/) (Chrome);
* Verificar preenchimento dos formulários (validação, envio e recebimento):
	* Existe alguma validação nos campos de preenchimento?;
	* Os campos marcados como obrigatórios estão sendo validados?;
	* Em caso de erro ou conexão lenta, existe alguma mensagem de feedback para o usuário?;
	* Os e-mails designados para serem destinatários estão recebendo o formulário?;
	* Em caso do usuário solicitar ou receber uma confirmação por e-mail, ela está sendo enviada e exibida corretamente?;
	* Em caso de upload, é possível enviar os arquivos? Existe algum limite de tamanho ou formato e isso está claro para o usuário?.
* Verificar sistemas com acesso restrito (login e senha):
	* É possível fazer login e logout no sistema?;
	* Existe alguma forma automática do usuário recuperar uma senha perdida.
* Verificar funcionalidades de comércio eletrônico:
	* É possível adicionar, remover ou atualizar itens do carrinho de compras?:
	* O processo de checkout está funcionando corretamente?.
* Verificar funcionalidades dos feeds de RSS;
* Verificar sistema de busca interna:
	* A busca está retornando resultados satisfatórios e relevantes ao usuário?;
	* É possível compartilhar o link de resultado de uma busca específica?;
	* O que acontece se realizarmos uma busca com o campo vazio?;
	* O resultado da busca está incluindo resultados de áreas de acesso restrito que não devem ser exibidos?
* Verificar funcionamento de elementos de áudio e vídeo, incluindo controles de volume e execução (parar, avançar e voltar);
* Verificar funcionamento do aplicativo de mapa:
	* É possível compartilhar o link de resultado de uma busca ou ponto específico?;
	* Em caso de erro ou conexão lenta, existe alguma mensagem de feedback para o usuário?.
* Verificar funcionamento de outros sistemas complexos e específicos que não estejam listados acima;
* Verificar a existência de favicons, [touch icons](http://mathiasbynens.be/notes/touch-icons) e [screen site tiles](http://www.buildmypinnedsite.com/);
* Verificar a existência da página de erro 404;
* Verificar existência da página de manutenção;
* Verificar se existe algum link para a URL de desenvolvimento que pode quebrar quando o website entrar no ar.
