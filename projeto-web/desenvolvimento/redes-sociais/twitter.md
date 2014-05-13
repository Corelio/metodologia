# Twitter

## Como configurar os Twitter Cards
#### 1) Inclua as meta tags no ```<head>``` do HTML

    <meta name="twitter:card" content="Tipo do card"> 
    <meta name="twitter:creator" content="@username-do-website">
    <meta name="twitter:site" content="@username-do-autor">
    <meta name="twitter:domain" content="domain.com.br">
    <meta name="twitter:title" content=“O título do artigo”>
    <meta name="twitter:description" content="A descrição do artigo”>
    <meta name="twitter:image:src" content=content=“URL da imagem do artigo”>

* Há diferentes [tipos](https://dev.twitter.com/docs/cards#cards) de Twitter Cards; o mais usado é o _summary_
* O tamanho mínimo para a imagem do [_Summary Card_](https://dev.twitter.com/docs/cards/types/summary-card) é 120x120px (imagens maiores serão recortadas e/ou redimensionadas em formato quadrado); a imagem não deve ter mais de 1MB; use caminho absoluto 

#### 2) Teste e solicite a validação do _Card_

O Twitter disponibiliza uma ferramenta para validação dos _cards_ chamada [Card Validator](https://dev.twitter.com/docs/cards/validation/validator). 

Para validar:

**a)** Selecione o tipo de _card_ <br>
**b)** Clique em _Validate and Apply_ <br>
**c)** Entre com a URL e clique em GO <br>
**d)** Se estiver tudo ok com as declarações das meta tags, aparecerá _Request approval_; basta clicar<br>
**e)** Entre com os dados do Administrador (@a2lab) e os dados sobre o site; envie e é só aguardar a aprovação (que acontece em alguns minutos)

###Dicas
* O tamanho recomendado da imagem/thumbnail varia de acordo com o tipo de _card_
* Após a aprovação, pode levar alguns minutos até que a visualização do _card_ esteja disponível nos compartilhamentos
* Um e-mail é enviado ao Administrador (@a2lab) avisando sobre a aprovação do _card_; 
* Caso queira testar a aprovação, repita os procedimentos do Passo 2; ao invés do link de solicitação de validação, deve aparecer _approved_
* É necessário fazer a validação para cada tipo de _card_ que será utilizado

###Referências

* [About Twitter Cards](https://dev.twitter.com/docs/cards)
* [Cards Markup Tag Reference](https://dev.twitter.com/docs/cards/markup-reference)
* [Cards Validator Tool](https://dev.twitter.com/docs/cards/validation/validator)
