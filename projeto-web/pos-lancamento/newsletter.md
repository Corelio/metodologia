# Newsletter

## Boas práticas
* Utilize sempre o `DOCTYPE Transitional`;
* Não utilize CSS externo e use apenas CSS inline;
* Não abuse de propriedades como `float`, `position` etc.;
* Determine a altura e largura das imagens;
* Não utilize arquivos .png com fundo transparente;
* Evite gifs;
* Não ultrapasse 600px de largura;
* Deixe seu arquivo HTML com até 30kb;
* Use sempre `background-color` (ou `bgcolor` quando for em um elemento da tabela) quando usar imagens - assim não ficará em branco quando o leitor não carregar a imagem;
* Quando precisar de padding interno, utilize uma outra tabela dentro com a propriedade `cellspacing` preenchida (Outlook não entende padding no elemento);
* Quando usar imagem com elemento de texto ao lado, aumente o espaço onde deseja o padding, pelo mesmo motivo acima;
* Não utilize propriedades CSS que não aceitas nos browsers [[1]](#newsletter1).

=

## Estrutura

* Tabela: `<table>`;
* Linha da tabela: `<tr>`;
* Coulunas dentro da tabela: `<td>`.

=

## Mailchimp
Ao criar uma campanha no Mailchimp, não esqueça de usar as seguintes marcações:

* `*|ARCHIVE|*` - Para mostrar a newsletter no browser caso a pessoa não consiga visualizá-la corretamente;
* `*|UNSUB|*` - Opção do usuário descadastrar seu e-mail;
* `*|REWARDS|*` - Para exibir o _badge_ do Mailchimp.

Obs.: Caso esqueça a tag `unsub` ou `rewards`, o Mailchimp automaticamente insere todas as informações do cadastro no rodapé (endereço, telefone, cep etc.).

=

## Dicas

### Como incluir elementos inline, com background e espaçamento interno

Exemplo: 

![Elementos inline com background](/assets/newsletter_01.png)

* Dentro da tabela principal do conteúdo, insira uma `<tr>` com a quantidade de `<td>` desejadas;
* Dentro de cada `<td>` inclua uma nova tabela, com uma nova `<tr>` e `<td>` dentro;
* Insira a cor na tabela com o atributo `brcolor` e o espaçamento interno com o atributo `cellpadding`;
* Para alinhar o conteúdo, coloque o atributo de alinhamento na `<td>`.

=

## Testes
Os testes são feitos nos principais leitores: Gmail, Hotmail e Outlook. É importante observar que não existe um padrão de escrita e a newsletter provavelmente apresentará alguma diferença entre esses leitores devido às limitações de cada um.

### Checklist
* Utilize sempre o atributo `valign=top` nas `<td>`;
* Todas as imagens devem ter `display:block`;
* As imagens devem possuir URLs absolutas;
* Utilize o atributo `alt` nas imagens;
* Não esqueça de preencher a tag `<title>`;
* Insira o atributo `outline:none` em todos os elementos `<a>`, evita que fique com uma borda pontilhada ao clicar.

=

## Referências
* [<a name="newsletter1"></a>1] - [The ultimate Guide to CSS](http://www.campaignmonitor.com/css/)
* [Boas práticas para e-mail marketing](http://tableless.com.br/boas-praticas-para-e-mail-marketing/#.UgEIxlOAFFR)
* [Which doctype should I use in HTML e-mail?](http://www.campaignmonitor.com/blog/post/3317/correct-doctype-to-use-in-html-email/)
* [What you should know about HTML e-mail](http://hub.tutsplus.com/tutorials/what-you-should-know-about-html-email--webdesign-12908)



