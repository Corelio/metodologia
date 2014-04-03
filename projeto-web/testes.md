#Testes

## Device Lab

### Adobe Edge Inspect
1. Primeiro precisamos fazer o [download](https://creative.adobe.com/inspect) do aplicativo do Edge Inspect. É necessário ter/criar uma conta na Creative Cloud;
2. Depois é necessário fazer o [download](https://chrome.google.com/webstore/detail/adobe-edge-inspect-cc/ijoeapleklopieoejahbpdnhkjjgddem) da extensão para Google Chrome;
3. Agora, precisamos escolher os dispositivos que vamos sincronizar com o computador e, fazer o download da app para a plataforma [Android](https://play.google.com/store/apps/details?id=com.adobe.shadow.android&hl=pt_BR) ou [iOS](https://itunes.apple.com/br/app/adobe-edge-inspect/id498621426?mt=8);
4. Feito isso, executarmos o aplicativo da Adobe Edge Inspect no computador. Provavelmente será necessário logarmos com a nossa conta da Creative Cloud;
5. Agora precisamos abrir a extensão do Chrome e ativá-la, clicando em um botão no canto superior direito;
6. O próximo passo é abrir o aplicativo no dispositivo que queremos sincronizar. Ao abrir, precisamos _Adicionar uma conexão_, clicando no ícone “+” no canto superior direito e, inserir o _IP_ do computador;
7. Após inserirmos o _IP_, um código será gerado na app. Devemos inserí-lo na extensão do Google Chrome que provavelmente irá abrir automaticamente;
8. Pronto! Tente acessar uma outra URL e automaticamente o dispositivo que sincronizamos com o computador irá atualizar automaticamente.
**Importante**: A versão gratuita permite apenas a conexão de um dispositivo.

### Referências
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

=

## Como realizar um teste?
1. Defina o tipo de teste que será realizado;
2. Acesse o Basecamp e insira no projeto que será testado, o template da lista de teste selecionado;
3. Defina as páginas que serão testadas, dando preferência à homepage, páginas de abertura de seção, páginas internas de conteúdo, páginas mais acessadas e páginas com formulários;
4. Acesse o website que será testado e realize as tarefas da lista;
5. Crie uma lista de tarefas no Basecamp chamada “Planilha de erros” ([Veja um exemplo](https://a2comunicacao.basecamphq.com/projects/10920256-2013-04-a2comunicacao/todo_lists/23727083));
6. Inclua uma tarefa para cada erro encontrado, utilizando o formato: `PN / Tipo de teste / Ação para corrigir o erro encontrado`;
7. Inclua mais detalhes no comentário da tarefa (URL, navegador, sistema operacional etc.);
8. Marque as tarefas que foram verificadas;
9. Inclua link para o bug reportado no comentário das tarefas onde foram encontrados os erros;
10. Apague as que não podem ser realizadas (Ex.: Verificar um mapa em um website que não usa esse recurso).

=

## Por que realizar um teste?

= 

## Tipos de testes

Os tipos de testes manuais (não automatizados) realizados em um website ou aplicativo web são:

1. [Acessibilidade](#acessibilidade)
2. [CMS](#cms)
3. [Compatibilidade](#compatibilidade)
4. [Conteúdo](#conteudo)
5. [Funcional](#funcional)
6. [Newsletter](#newsletter)
7. [Performance](#performance)
8. [Segurança](#seguranca)
9. [SEO e Marketing](#seo)
10. [Usabilidade](#usabilidade)

### <a name="acessibilidade"></a>Acessibilidade

Estima-se que 20% da população mundial possue algum tipo de deficiência [[1]](#acessibilidade1). Além de ser comercialmente imprudente excluir esses clientes em potencial, para a maioria dos governos é uma questão de seguir a legislação. Testes de acessiblidade incluem o cumprimento das normas como [ADA](http://www.ada.gov/index.html), [Seção 508](https://www.section508.gov) ou [WCAG (W3C)](http://www.w3.org/TR/WCAG/).

#### Checklist
* Verificar declaração de idioma na tag HTML (Ex.: `<html lang=”pt-br”>`);
* Verificar se é possível navegar pelo teclado (utilizando a tecla TAB), se existe atalho para o conteúdo principal e se ele é visível para leitores de tela [[2]](#acessibilidade2);
* Verificar existência de landmarks (Ex.: `role=”banner”) [[3]](#acessibilidade3);
* Verificar se links estão marcados de forma correta (Evitar o fatídico “Clique aqui”) [[4]](#acessibilidade4)[[5]](#acessibilidade5);
* Verificar contraste de cores das páginas utilizando o [Colour contrast check](http://snook.ca/technical/colour_contrast/colour.html);
* Verificar se todos os elementos do formulário possuem etiqueta `<label>` e se essa etiqueta está associada ao elemento correto do formulário (`<id>`) [[6]](#acessibilidade6);
* Verificar se elementos obrigatórios do formulário estão devidamente identificados (`aria-required=true`) [[7]](#acessibilidade7);
* Verificar se o feedback do formulário direciona o usuário para o campo a ser corrigido, através de link [[8]](#acessibilidade8);
![Verificar se feedback do formulário direciona o usuário para o campo a ser corrigido, através de link](http://lab.a2comunicacao.com.br/metodologia/testes_form-validation.gif)
* Verificar se vídeos possuem legendas e se áudios possuem transcrição;
* Validar (de forma automática) acessibilidade das páginas usando o [Wave](http://wave.webaim.org/) [[9]](#acessibilidade9);
* Validar (de forma automática) HTML das páginas usando o [W3C Validator](http://validator.w3.org/);
* Verificar funcionamento das páginas sem o uso de JavaScript, Flash ou outro(s) plugin(s).

#### Referências

* [<a name="acessibilidade1"></a>1] - [WebAIM - People with disabilities on the web](http://webaim.org/intro/#people)
* [<a name="acessibilidade2"></a>2] - [WebAIM - “Skip navigation links](http://webaim.org/techniques/skipnav/)
* [<a name="acessibilidade3"></a>3] - [WebAIM - Presenting document structure](http://webaim.org/techniques/aria/#structure)
* [<a name="acessibilidade4"></a>4] - [WebAIM - Screen reader users often navigate from link to link, skipping the text in between](http://webaim.org/techniques/hypertext/#link_to_link)
* [<a name="acessibilidade5"></a>5] - [Why your links should never say “Click here”](uxdesign.smashingmagazine.com/2012/06/20/links-should-never-say-click-here/)
* [<a name="acessibilidade6"></a>6] - [WebAIM - Creating accessible forms](http://webaim.org/techniques/forms/controls)
* [<a name="acessibilidade7"></a>7] - [W3C - ARIA2: Identifying required fields with the aria-required property](http://www.w3.org/TR/WCAG20-TECHS/ARIA2.html)
* [<a name="acessibilidade8"></a>8] - [WebAIM - Usable and accesible form validation and error recovery](http://webaim.org/techniques/formvalidation/#error)
* [<a name="acessibilidade9"></a>9] - [Issue #3: Acessibilidade - Qual norma e validador devemos utilizar?](https://github.com/a2comunicacao/metodologia/issues/3)
* [Acessibilidade na Web: Principais problemas e soluções - FISL14](http://www.slideshare.net/julianafrost/acessibilidade-na-web-principais-problemas-e-solues)
* [WebAIM - Web captioning overview](http://webaim.org/techniques/captions/)

=

### <a name="cms"></a>CMS

=

### <a name="compatibilidade"></a>Compatibilidade (Cross-browser)
Funcionamento em diferentes browsers, sistemas operacionais e servidores. Atualmente o teste deve ser feito nos principais browsers (Chrome, Internet Explorer, Firefox, Safari e Opera), entre sistemas operacionais (PC e Mac) e entre dispositivos (Smartphone, Tablet e Desktop).

#### O que deve ser observado em um teste cross-browser? [[1]](#compatibilidade1)
1. A diagramação das páginas e posição dos elementos estão compatíveis com o layout original?;
2. Links, menus e dropdowns são fáceis de clicar em interfaces de toque (tablets e smartphones)?;
3. Elementos clicáveis mudam visualmente ao passar o cursor do mouse (mouse over)?;
4. Efeitos de animação, transições da interface e janelas modais (pop-ups) estão funcionando corretamente?;
5. Fontes tipográficas estão bem renderizadas e num tamanho coerente?;
6. A resolução das imagens é suficiente? Elas estão adaptadas para telas LCD ([Retina display](http://pt.wikipedia.org/wiki/Tela_retina))?;
7. Existe alguma barra de navegação horizontal que não foi planejada?;
8. Palavras com acento são exibidas corretamente?;
9. Validação e envio de formulários está funcionando?

#### Checklist
* Verificar páginas no Desktop (PC ou Mac) nas seguintes resoluções: 1024x768, 1280x800, 1280x1024, 1366x768, 1440x900 e 1920x1080 [[2]](#compatibilidade2) (Dica: Utilize a opção “resize” da extensão [Web Developer](http://chrispederick.com/work/web-developer/);
* Verificar páginas no Fireforx para Mac (versão atual);
* Verificar páginas no Firefox para Windows (versão atual);
* Verificar páginas no Internet Explorer 7;
* Verificar páginas no Internet Explorer 8;
* Verificar páginas no Internet Explorer (versão atual);
* Verificar páginas no Chrome para Mac (versão atual);
* Verificar páginas no Chrome para Windows (versão atual);
* Verificar páginas no Safari para Mac (versão atual);
* Verificar páginas no Safari para iPad (versão atual);
* Verificar páginas no Safari para iPhone (versão atual);
* Verificar se os campos de formulário estão marcados com o parâmetro _TYPE_ correto [[3]](#compatibilidade3).

#### Referências

* [<a name="compatibilidade1"></a>1] - [Issue #6 - Compatibilidade - O que deve ser observado em um teste cross-browser?](https://github.com/a2comunicacao/metodologia/issues/6)
* [<a name="compatibilidade2"></a>2] - [W2Counter - Global Web Stats](http://www.w3counter.com/globalstats.php)
* [<a name="compatibilidade3"></a>3] - [Dive into HTML5 - Uma forma de loucura](http://diveintohtml5.com.br/forms.html)
* [Codrops - UI Design guidelines for Responsive Design](http://tympanus.net/codrops/2013/01/21/ui-design-guidelines-for-responsive-design/)
* [Smashing Magazine - Review of cross-browser testing tools](http://www.smashingmagazine.com/2011/08/07/a-dozen-cross-browser-testing-tools/)
* [Techniques for mobile and responsive cross-browser testing: An Envato case study](http://webuild.envato.com/blog/techniques-for-mobile-and-responsive-cross-browser-testing/)

=

### <a name="conteudo">Conteúdo
O conteúdo é a parte mais importante de um website. Além de revisão ortográfica, deve-se avaliar o contexto e os _microtextos_ [[1]](#conteudo1) presentes na interface.

#### Checklist
* Revisar ortografia e sintaxe dos títulos e do corpo do texto;
* Revisar ortografia de “textos ocultos” como mensagens de validação de formulários, tooltips e alertas de janelas modais (pop-ups);
* Verificar a existência de conteúdo de teste ([Lorem ipsum](http://pt.wikipedia.org/wiki/Lorem_ipsum), [Placeholders](http://placehold.it/) etc.);
* Revisar relevância das imagens, legendas e créditos;
* Verificar existência de textos em outros idiomas;
* Verificar se a acentuação nos títulos está funcionando corretamente;
* Verificar se é possível selecionar, copiar e colar os principais textos da página;
* Verificar existência de palavras viúvas em títulos e parágrafos importantes;
* Verificar variação na grafia de palavras iguais (Ex.: websites, web sites, sites e sítios);
* Verificar se as redes sociais relacionadas ao website estão linkadas corretamente;
* Verificar se elementos de texto possuem formatação visual (links, listas, negrito, itálico, bloco, código, etc.);
* Em caso de migração ou redesign, verificar se todo o conteúdo está sendo considerado (notícias, imagens, vídeos, áudios, posts, comentários, etc.).

#### Referências
* [<a name="conteudo1"></a>1] [Smashing Magazine - Five ways to prevent bad microcopy](http://uxdesign.smashingmagazine.com/2013/06/17/five-ways-prevent-bad-microcopy/)
* [BlogdeAI - Usando os microtextos a favor da experiência do usuário](http://arquiteturadeinformacao.com/user-experience/usando-os-microtextos-a-favor-da-experiencia-do-usuario/)

=

### <a name="funcional"></a>Funcional
Testes funcionais estão relacionados a entrada e saída de dados. Clicar em links, preencher um cadastro e realizar uma busca são entrada de dados feitas pelos usuários na expectativa de obter uma resposta satisfatória do software.

#### Checklist
* Verificar links quebrados na barra de navegação e no corpo do texto usando a extensão [Link Checker](https://addons.mozilla.org/pt-br/firefox/addon/linkchecker/) (Firefox) ou [Check my links](https://chrome.google.com/webstore/detail/check-my-links/ojkcdipcgfaekbeaelaapakgnjflfglf/) (Chrome);
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

=

### <a name="newsletter"></a>Newsletter

#### Checklist
* Verificar formatação da newsletter no MS Outlook;
* Verificar formatação da newsletter no Hotmail;
* Verificar formatação da newsletter no Yahoo! Mail;
* Verificar formatação da newsletter no Gmail;
* Verificar se todas as imagens `<img>` possuem os atributos _display:block_ e _alt_;
* Verificar se todos os links `<a>` possuem o atributo _outline:none_;
* Utilizar sempre o atributo _valign=top_ nas `<td>`;
* As imagens devem possuir URL absoluta;
* Verificar o preenchimento da tag `<title>`.

#### Referências
* [Campaign Monitor - Email client popularity](http://www.campaignmonitor.com/resources/will-it-work/email-clients/)
* [Newsletter](https://github.com/a2comunicacao/metodologia/blob/master/testes/Newsletter)

=

### Performance
Testes de performance são realizados para determinar como um sistema roda em termos de capacidade de resposta e estabilidade sob uma carga de trabalho particular. Também pode ser para investigar, mensurar, validar ou verificar escalabilidade, confiabilidade e uso de recursos.

#### Checklist
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

#### Referências
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

=

### <a name="seguranca"></a>Segurança
Testes de segurança são essenciais para verificar se dados confidenciais estão armazenados devidamente, se não há possibilidade de invasão do sistema e se existe uma rotina de backup.

#### Checklist
* Verificar se páginas sensíveis ou protegidas estão declaradas no robots.txt [[1]](#seguranca1);
* Verificar espaço/capacidade em disco para armazenamento dos arquivos no servidor;
* Verificar rotina de backup dos arquivos e do banco de dados (e testar a recuperação dos dados);
* Verificar agenda de atualização do CMS e dos plugins;
* Verificar se mensagens de erro do servidor estão desativadas para o usuário;
* Verificar configuração de serviço de monitoramento de erros do servidor com avisos por e-mail ou SMS (Ex.: [Uptime Robot](http://www.uptimerobot.com/));
* Verificar se os endereços de e-mail estão mascarados contra spammers usando o [Email Encoder](http://www.wbwip.com/wbw/emailencoder.html);
* Verificar requisitos mínimos de segurança utilizando o [Websecurity Foundation](https://suite.websecurify.com/foundation).

#### Referências
* [<a name="seguranca1"></a>1] - [Google Webmasters - Bloquear ou remover páginas usando um arquivo robots.txt](https://support.google.com/webmasters/answer/156449?hl=pt-BR)

=

### <a name="seo"></a>SEO e Marketing
É importante avaliar se boas práticas de código e conteúdo estão sendo seguidas para garantir uma boa visibilidade do website ou software nos mecanismos de busca.

#### Checklist
* Verificar existência e relevância de keywords nos títulos das página;
* Verificar existência, relevância e tamanho (entre 150 a 160 caracteres [[1]](#seo1) das [metas descriptions](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/desenvolvimento.md#meta-description) utilizando a extensão [Meta SEO Inspector (Chrome)](https://chrome.google.com/webstore/detail/meta-seo-inspector/ibkclpciafdglkjkcibmohobjkcfkaef/);
* Verificar configuração de URL canônica no servidor [[2]](#seo2);
* Verificar formatação e estruturação das URL amigáveis [[3]](#seo3);
* Verificar a padronização e hierarquia dos cabeçalhos no conteúdo usando a extensão Web Developer [[4]](#seo4);
* Verificar funcionamento dos links de compartilhamento e como estão sendo exibidos nas redes sociais;
* Verificar existência de arquivo XML Sitemap com permissão de escrita;
* Verificar configuração do [Google Webmaster Tools](https://www.google.com/webmasters/) e [Bing Webmaster Tools](http://www.bing.com/toolbox/webmaster);
* Verificar funcionamento da ferramenta de monitoramento de acessos (Ex.: [Configuração de metas no Google Analytics](http://www.google.com/analytics/)) [[5]](#seo5);
* Em caso de migração ou redesign, verificar se as URLs alteradas estão sendo redirecionadas através do código de status HTTP 301;
* Verificar aparência do website nas páginas de resultado de busca (SERPs) [[6]](#seo6).

=

### <a name="usabilidade"></a>Usabilidade

Testes de usabilidade tem por objetivo verificar a facilidade que o software ou website possui de ser claramente compreendido e manipulado pelo usuário.

#### Checklist
* Realizar testes de usabilidade com usuários reais;
* Realizar análise heurística de usabilidade;
* Verificar o estado das telas em branco;
* Feedback para o usuário;

#### Referências
* [Webdesigner Depot - How to approach usability testing](http://www.webdesignerdepot.com/2013/06/how-to-approach-usability-testing/)

=

## Referências

* [HTML5 Boilerplate documentation](https://github.com/h5bp/html5-boilerplate/blob/v4.2.0/doc/TOC.md)
* [Wikipedia - Software testing](http://en.wikipedia.org/wiki/Software_testing)
* [Re-lauching the ultimate website launch checklist](http://www.boxuk.com/blog/relaunching-the-ultimate-website-launch-checklist/)
