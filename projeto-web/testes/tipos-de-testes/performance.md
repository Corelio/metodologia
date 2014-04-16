# Performance
Testes de performance são realizados para determinar como um sistema roda em termos de capacidade de resposta e estabilidade sob uma carga de trabalho particular. Também pode ser para investigar, mensurar, validar ou verificar escalabilidade, confiabilidade e uso de recursos.

## Checklist
* Verificar existência de código CSS e JS inline ou incorporado no HTML [[1]](#performance1);
* Verificar posicionamento dos estilos (topo) e scripts (rodapé) no HTML [[2]](#performance2);
* Verificar se arquivos [JavaScript](https://github.com/zenorocha/browser-diet/wiki/Tools#minify-your-script) e [CSS](https://github.com/zenorocha/browser-diet/wiki/Tools#minify-your-stylesheets) estão comprimido/minificados;
* Verificar se folhas de estilo estão combinadas em um único arquivo CSS [[3]](#performance3);
* Verificar se arquivo CSS está sendo chamado com `<link>` e não com `@import` [[4]](#performance4);
* Verificar se código JavaScript de terceiros estão sendo carregador de forma assíncrona [[5]](#performance5);
* Verificar o uso desnecessário de `document.write` no código JavaScript [[6]](#performance6);
* Verificar se scripts estão combinados em um único JS [[7]](#performance7);
* Verificar se bibliotecas JS, como jQuery, estão atualizadas;
* Verificar uso de CSS Sprites [[8]](#performance8);
* Verificar se imagens não estão sendo redimensionadas por CSS ou HTML [[9]](#performance9);
* Verificar otimização das imagens [[10]](#performance10);
* Verificar uso de cache dos arquivos no servidor [[11]](#performance11);
* Verificar compressão de arquivos pelo servidor (GZIP) [[12]](#performance12);
* Verificar e anotar o tempo de carregamento e peso da página utilizando o [YSlow](http://developer.yahoo.com/yslow/), [Page Speed Insights](https://developers.google.com/speed/pagespeed/insights) ou [Page Speed Insights Browser Extension](https://developers.google.com/speed/pagespeed/insights_extensions);
* Verificar o uso de  CDNs para carregamento de bibliotecas e frameworks públicos [[13]](#performance13);
* Validar arquivos CSS utilizando o CSSLint [[14]](#performance14);
* Validar arquivos JavaScript utilizando o JSLint [[15]](#performance15).

## Referências
* [<a name="performance1"></a>1] - [Browser diet - Evite código inline/incorporado no HTML](http://browserdiet.com/pt/#avoid-inline)
* [<a name="performance2"></a>2] - [Browser diet - Estilos no topo, scripts no rodapé](http://browserdiet.com/pt/#css-on-top-js-on-bottom)
* [<a name="performance3"></a>3] - [Browser diet - Combine vários arquivos CSS em um só](http://browserdiet.com/pt/#combine-css)
* [<a name="performance4"></a>4] - [Browser diet - Prefira a @import](http://browserdiet.com/pt/#prefer-link-over-import)
* [<a name="performance5"></a>5] - [Browser diet - Carregue código de terceiros de forma assíncrona](http://browserdiet.com/pt/#3rd-party-async)
* [<a name="performance6"></a>6] - [Browser diet - Evite document.write](http://browserdiet.com/pt/#documentwrite)
* [<a name="performance7"></a>7] - [Browser diet - Combine vários arquivos js em um só](http://browserdiet.com/pt/#combine-js)
* [<a name="performance8"></a>8] - [Browser diet - Use CSS sprites](http://browserdiet.com/pt/#sprites)
* [<a name="performance9"></a>9] - [Browser diet - Não escale imagens direto no código](http://browserdiet.com/pt/#scale)
* [<a name="performance10"></a>10] - [Browser diet - Otimize suas imagens](http://browserdiet.com/pt/#optimize)
* [<a name="performance11"></a>11] - [Browser diet - Habilite o cache dos arquivos](http://browserdiet.com/pt/#cache)
* [<a name="performance12"></a>12] - [Browser diet - GZIP](http://browserdiet.com/pt/#gzip)
* [<a name="performance13"></a>13] - [YSlow - Use a content delivery network](http://developer.yahoo.com/performance/rules.html#cdn)
* [<a name="performance14"></a>14] - [Issue #2 - CSS - Por que validar e qual validador devemos utilizar?](https://github.com/a2comunicacao/metodologia/issues/2)
* [<a name="performance15"></a>15] - [Issue #4 - JavaScript - Por que validar e qual validador devemos utilizar?](https://github.com/a2comunicacao/metodologia/issues/4)
* [Smashing Magazine - Writing fast, memory-efficient JavaScript](http://coding.smashingmagazine.com/2012/11/05/writing-fast-memory-efficient-javascript/)
* [Superhero.js - Uma coleção de artigos, vídeos e apresentações sobre criação, teste e manutenção de código JavaScript](http://superherojs.com/)
* [My performance audit workflow](http://aerotwist.com/blog/my-performance-audit-workflow/)
