# Google Analytics

## Universal Analytics

É a plataforma mais recente do Google Analytics. Apresenta um novo código de acompanhamento mais flexível e otimizado.

* [Universal Analytics: A evolução do Google Analytics](http://www.dp6.com.br/universal-analytics-a-evolucao-do-google-analytics/)
* [Sobre o Universal Analytics](https://support.google.com/analytics/answer/2790010?hl=pt-BR&ref_topic=6010376)
* [Verificar se você usa o Universal Analytics](https://support.google.com/analytics/answer/4457764?hl=pt-BR&ref_topic=6010376)

####Migrando do clássico para o Universal Analytics

* [Upgrade para o Universal Analytics](https://support.google.com/analytics/answer/3450662?hl=pt-BR&ref_topic=6010376)

####Configurando do início

* [Configurar o Universal Analytics: uma visão geral](https://support.google.com/analytics/answer/2817075?hl=pt-BR&ref_topic=6010376)

## Monitoramento de eventos (Event Track)
Permite medir interações dos usuários com o conteúdo do website.  <br/>
Funciona em conjunto com os [HTML Events](http://www.w3schools.com/tags/ref_eventattributes.asp).

Código base para monitormaneto de eventos (no exemplo, com o evento 'click' e usando jquery):

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


## Monitoramento de envio de formulários

## Monitoramento de eventos de botões nas redes socias

## Social Plug-ins 
