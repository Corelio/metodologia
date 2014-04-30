# Google Analytics

## Universal Analytics

É a plataforma mais recente do Google Analytics. Apresenta um novo código de acompanhamento mais flexível e otimizado.

* [Universal Analytics: A evolução do Google Analytics](http://www.dp6.com.br/universal-analytics-a-evolucao-do-google-analytics/)
* [Sobre o Universal Analytics](https://support.google.com/analytics/answer/2790010?hl=pt-BR&ref_topic=6010376)
* [Verificar se você usa o Universal Analytics](https://support.google.com/analytics/answer/4457764?hl=pt-BR&ref_topic=6010376)

#### Migrando do clássico para o Universal Analytics

* [Upgrade para o Universal Analytics](https://support.google.com/analytics/answer/3450662?hl=pt-BR&ref_topic=6010376)

#### Configurando do início

* [Configurar o Universal Analytics: uma visão geral](https://support.google.com/analytics/answer/2817075?hl=pt-BR&ref_topic=6010376)

## Monitoramento de eventos (Event Track)
Permite medir interações dos usuários com o conteúdo do website.  <br/>
Funciona em conjunto com os [HTML Events](http://www.w3schools.com/tags/ref_eventattributes.asp).

Código base para monitormaneto de eventos (no exemplo, com o evento _click_ e usando jquery):

```javascript
//Universal Analytics
$('#elemento').click(function(){
  ga('send', 'event', 'category', 'action', 'label');
}
```
```javascript
//Classic Analytics
$('#elemento').click(function(){
  _gaq.push(['_trackEvent', 'category', 'action', 'label']);
}
```

* [Event Tracking (Universal Analytics)](https://developers.google.com/analytics/devguides/collection/analyticsjs/events?hl=pt-BR)
* [Event Tracking  (Classic Analytics)](https://developers.google.com/analytics/devguides/collection/gajs/eventTrackerGuide?hl=pt-BR)

#### Onde encontrar os dados no Google Analytics?
O relatório que exibi as informações coletadas pelos _Event Tracks_ fica em **Comportamento > Eventos > Visão geral** (exemplo: veja o [relatório para o site da A2 Comunicação](https://www.google.com/analytics/web/?hl=pt-BR&pli=1#report/content-event-overview/a9911169w21785238p83581831/)).

## Monitoramento de envio de formulários

O monitoramento do _click_ no botão de envio do fomulário não é a forma mais eficaz para esse tipo de interação. Pois o usuário pode clicar no botão, sem ter preenchido os campos; o formulário não será enviado, mas o click será contabilizado no formulário do Google Analytics. 

Uma melhor solução é o monitoramento da resposta de sucesso que o servidor retorna quando formulário é efetivamente enviado. Para isso é necessário uma configuração especial dessas respostas (como foi feito no site da A2 pelo [@williancarminato](https://github.com/williancarminato)). 

```php
// Exemplo: como foi implementado o Event Track no site da A2 Comunicação (com Twig)
{% if enviou == true %} //onde 'enviou' é a variável de resposta do servidor
  <script>
    $(window).load(function(){
      ga('send', 'event', 'Contato', 'Enviou', 'Enviar uma mensagem', {'nonInteraction': 1});
    });
</script>
{% endif %}
```


## Monitoramento de eventos de botões nas redes sociais

O ideal para esse tipo de monitoramento é o uso dos [Social Plug-ins](#social-plugins). Se por alguma razão eles não se aplicarem, é possível configurar o monitoramento do _click_ no botão de compartilhamento.

Nesse caso, é interessante definir o _label_ dinamicamente com a URL do conteúdo. Pois assim, no relatório do Analytics vai ser possível saber quais os conteúdos mais clicados por rede social. 
```javascript
// Exemplo: como foi implementado o Event Track no site da A2 Comunicação (com JQuery)
$('.facebook').click(function(){
     var url = $(this).parent().data('href'); 
     ga('send', 'event', 'Facebook: Compartilhou', 'Clicou', url);
 });
```

## <a name="social-plugins"></a>Social Plug-ins 
