# Newsletter

## Estrutura

* `<table>` - Tabela
* `<tr>` - Linha da tabela
* `<td>`- Colunas dentro da linha

## Boas práticas

* Utilizar sempre o DOCTYPE Transitional ;
* Não utilizar CSS externo e utilize apenas CSS inline (utilize apenas o extremamente necessário na tag `<head>`);
* Não abusar de propriedades como float, position etc.;
* Determine a altura e largura das imagens;
* Não utilize png transparente;
* Evite gifs;
* Não ultrapassar 600px de largura;
* HTML com até 30kb;
* Usar sempre background-color (ou bgcolor quando for num elemento da tabela) quando usar imagens - assim não ficará branco quando o leitor não entender a imagem;
* Quando precisar de padding interno, utilize uma outra tabela dentro com a propriedade `cellspacing` preenchida (outlook não entende `padding` no elemento);
* Quando usar imagem com elemento de texto ao lado, aumente o espaço onde deseja o `padding`, pelo mesmo motivo acima;
* [Aqui](http://www.campaignmonitor.com/css/) é possível ver todas as propriedades de CSS que são aceitas ou não nos browsers.

### Referências:
* [Boas práticas para e-mail marketing](http://tableless.com.br/boas-praticas-para-e-mail-marketing/#.UgEIxlOAFFR)
* [Which doctype should I use in HTML email?](http://www.campaignmonitor.com/blog/post/3317/correct-doctype-to-use-in-html-email/)
* [What You Should Know About HTML Email](http://hub.tutsplus.com/tutorials/what-you-should-know-about-html-email--webdesign-12908)

## Mailchimp

Lembrar sempre de usar os atributos:
* `*|ARCHIVE|*` - Para mostrar a newsletter no browser caso a pessoa não consiga visualiza-la corretamente;
* `*|UNSUB|*` - Opção do usuário descadastrar seu e-mail;
* `*|REWARDS|*` - Para exibir o badge do Mailchimp

_Obs.:_ Caso esqueça a tag `unsub` ou `rewards` o Mailchimp automaticamente insere todas as informações relevantes no rodapé (endereço, telefone, cep)

## Testes
É importante testar a newsletter antes de enviá-la, leitores como Gmail, Hotmail e Outlook interpretam o HTML de forma totalmente diferente uma das outras. Não foi possível até o momento deixar as três ferramentas lendo a formatação de forma unificada (isso também porque, nossas newsletters são bem personalizadas). 

### Checklist

* Utilize sempre o atributo `valign=top` nas `<td>` ;
* Todas as imagens devem ter `display:block`;
* As imagens devem possuir URL absoluta;
* Utilize o atributo `alt`;
* Não esquecer de preencher a tag `<title>`;
* Insira o atributo `outline: none` em todos os elementos `<a>`, evita que fique com a borda pontilhada ao clicar.

## Como incluir elementos inline, com background e espaçamento interno

Exemplo:
![Elementos inline com background](img/newsletter_itens-inline.png)

Dentro da tabela principal do conteúdo, insira uma `<tr>`com a quantidade de `<td>` desejadas. Dentro de cada `<td>` inclua uma nova tabela, com uma nova `<tr>` e `<td>` dentro. Insira a cor na tabela com o atributo `bgcolor` e o espaçamento interno com o atributo `cellpadding`. Para alinhar o conteúdo, coloque o atributo de alinhamento na `<td>`.
