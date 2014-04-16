
# Segurança
Testes de segurança são essenciais para verificar se dados confidenciais estão armazenados devidamente, se não há possibilidade de invasão do sistema e se existe uma rotina de backup.

## Checklist
* Verificar se páginas sensíveis ou protegidas estão declaradas no robots.txt [[1]](#seguranca1);
* Verificar espaço/capacidade em disco para armazenamento dos arquivos no servidor;
* Verificar rotina de backup dos arquivos e do banco de dados (e testar a recuperação dos dados);
* Verificar agenda de atualização do CMS e dos plugins;
* Verificar se mensagens de erro do servidor estão desativadas para o usuário;
* Verificar configuração de serviço de monitoramento de erros do servidor com avisos por e-mail ou SMS (Ex.: [Uptime Robot](http://www.uptimerobot.com/));
* Verificar se os endereços de e-mail estão mascarados contra spammers usando o [Email Encoder](http://www.wbwip.com/wbw/emailencoder.html);
* Verificar requisitos mínimos de segurança utilizando o [Websecurity Foundation](https://suite.websecurify.com/foundation).

## Referências
* [<a name="seguranca1"></a>1] - [Google Webmasters - Bloquear ou remover páginas usando um arquivo robots.txt](https://support.google.com/webmasters/answer/156449?hl=pt-BR)
