# Formulário de contato

## Mailgun
Em alguns ambientes de produção, o envio de e-mails via formulário de contato não funcionam corretamente. Para solucionar o problema, estamos utilizando a ferramenta **MailGun**, não havendo mais a necessidade de configurações extras de SMTP ou algo do gênero no Wordpress.

### Configuração

[http://www.mailgun.com/](http://www.mailgun.com/)

````
Login: config@a2comunicacao.com.br 
Senha: 2FNOk3Yw
```

* Logue no Mailgun e adicione um domínio novo em _Add Domain_;
* Baixe o Plugin do Mailgun no Wordpress;
* Insira a URL do site nos campos _Mailgun Domain Name_ e _Tag_;
* Insira a _API Key_ (ela é padrão e está localizada na página inicial do Mailgun, na lateral esquerda)

> Não foi necessário até o momento verificar os domínios (neste caso ele permite o envio de até 300 e-mails por dia)

