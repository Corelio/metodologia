# Device Lab

O Device Lab foi implantado na A2 com o objetivo de testar os projetos em diversos dispositivos, possibilitando experiência de usabilidade do projeto em um dispositivo real e não em um simulador.

Atualmente no nosso Device Lab, temos os seguintes dispositivos:

* Tablets
** Motorola Xoom com Android 4.1.2
* 2 iPads 3ª geração
* Celulares
* iPhone 5
* Samsung Galaxy com Android 4.1.2
* BlackBerry Z10 - versão 10.2.1.2102

Para testarmos o projeto nos dispositivos, podemos usar o [Grunt Browser Sync](../setup/grunt.md) (recomendado) ou o [Adobe Edge Inspect](#adobe-edge-inspect)


## Adobe Edge Inspect
1. Primeiro precisamos fazer o [download](https://creative.adobe.com/inspect) do aplicativo do Edge Inspect. É necessário ter/criar uma conta na Creative Cloud;
2. Depois é necessário fazer o [download](https://chrome.google.com/webstore/detail/adobe-edge-inspect-cc/ijoeapleklopieoejahbpdnhkjjgddem) da extensão para Google Chrome;
3. Agora, precisamos escolher os dispositivos que vamos sincronizar com o computador e, fazer o download da app para a plataforma [Android](https://play.google.com/store/apps/details?id=com.adobe.shadow.android&hl=pt_BR) ou [iOS](https://itunes.apple.com/br/app/adobe-edge-inspect/id498621426?mt=8);
4. Feito isso, executarmos o aplicativo da Adobe Edge Inspect no computador. Provavelmente será necessário logarmos com a nossa conta da Creative Cloud;
5. Agora precisamos abrir a extensão do Chrome e ativá-la, clicando em um botão no canto superior direito;
6. O próximo passo é abrir o aplicativo no dispositivo que queremos sincronizar. Ao abrir, precisamos _Adicionar uma conexão_, clicando no ícone “+” no canto superior direito e, inserir o _IP_ do computador;
7. Após inserirmos o _IP_, um código será gerado na app. Devemos inserí-lo na extensão do Google Chrome que provavelmente irá abrir automaticamente;
8. Pronto! Tente acessar uma outra URL e automaticamente o dispositivo que sincronizamos com o computador irá atualizar automaticamente.
**Importante**: A versão gratuita permite apenas a conexão de um dispositivo.

## Referências
* [Adactio: Laboratory conditions](http://adactio.com/journal/5661/)
* [Brad Frost](http://bradfrostweb.com/blog/mobile/test-on-real-mobile-devices-without-breaking-the-bank/)
* [Building a device stand](http://viljamis.com/blog/2012/building-a-device-stand/)
* [Esbablishing an open device lab](http://mobile.smashingmagazine.com/2012/09/24/establishing-an-open-device-lab/)
* [Etsy](http://codeascraft.com/2013/08/09/mobile-device-lab/)
* [Happy Cog](http://cognition.happycog.com/article/building-the-happy-cog-test-lab)
* [How to built the open device lab at beyond tellerrand](http://klick-ass.com/events/open-device-lab-at-conference-beyond-tellerrand/#exhibition)
* [Lab Up!](http://lab-up.org/)
* [Open device labs](http://www.smashingmagazine.com/2013/05/28/open-device-labs-why-should-we-care/)
* [Testlab](http://clearleft.com/testlab/)
