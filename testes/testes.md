# Testes

## Como realizar um teste?
1. Defina o tipo de teste que será realizado;
2. Acesse o Basecamp e insira no projeto que será testado, o template da lista de teste selecionado;
3. Defina as páginas que serão testadas, dando preferência à homepage, páginas de abertura de seção, páginas internas de conteúdo, páginas mais acessadas e páginas com formulários;
4. Acesse o website que será testado e realize as tarefas da lista;
5. Crie uma lista de tarefas no Basecamp chamada Planilha de erros. ([Veja um exemplo](https://a2comunicacao.basecamphq.com/projects/10920256-2013-04-a2comunicacao/todo_lists/23727083));
6. Inclua uma tarefa para cada erro encontrado, utilizando o formato: `PN / Tipo de teste / Ação para corrigir o erro encontrado`;
7. Inclua mais detalhes no comentário da tarefa (URL, navegador, sistema operacional etc.);
8. Marque as tarefas que foram verificadas;
9. Inclua link para o bug reportado, no comentário das tarefas onde foram encontrados os erros;
10. Apague as que não podem ser realizadas (ex. verificar um mapa em um website que não usa esse recurso).

## Por que realizar um teste?

## Tipos de testes

Os tipos de testes manuais (não automatizados) realizados em um website ou aplicativo web são:

1. [Acessibilidade](#acessibilidade)
1. [CMS](#cms)
1. [Compatibilidade](#compatibilidade)
1. [Conteúdo](#conteudo)
1. [Funcional](#funcional)
1. [Newsletter](#newsletter)
1. [Performance](#performance)
1. [Segurança](#seguranca)
1. [SEO e Marketing](#seo)
1. [Usabilidade](#usabilidade)
1. [Verificação de links](#verificacaodelinks)

### <a id="acessibilidade"></a>Acessibilidade

*Garantia de acesso para pessoas com deficiência (20% da população mundial).*

Estima-se que 20% da população mundial possue algum tipo de deficiência [[12](#nota12)]. Além de ser comercialmente imprudente excluir esses clientes em potencial, para a maioria dos governos é uma questão de seguir a legislação. Testes de acessibilidade incluem o cumprimento das normas como [ADA](http://www.ada.gov/index.html), [Seção 508](https://www.section508.gov/) ou [WCAG (W3C)](http://www.w3.org/TR/WCAG/);

#### Checklist

* Verificar declaração de idioma na tag HTML (Ex.:`<html lang="pt-br">`);
* Verificar se é possível navegar pelo teclado (utilizando a tecla TAB), se existe atalho para o conteúdo principal e se ele é visível para leitores de tela [[4](#nota04)];
* Verificar existência de landmarks (Ex.:`role="banner"`) [[8](#nota08)];
* Verificar se links estão marcados de forma correta (Evitar o fatídico "clique aqui")[[6](#nota06)][[39](#nota39)];
* Verificar contraste de cores das páginas utilizando o [Colour Contrast Check](http://snook.ca/technical/colour_contrast/colour.html);
* Verificar se todos os elementos do formulário possuem etiqueta `<label>` e se essa etiqueta está associada ao elemento correto do formulário (`<id>`) [[7](#nota07)];
* Verificar se elementos obrigatórios do formulário estão devidamente identificados (`aria-required=true`) [[9](#nota09)];
* Verificar se feedback do formulário direciona o usuário para o campo a ser corrigido, através de link [[10](#nota10)];

![Verificar se feedback do formulário direciona o usuário para o campo a ser corrigido, através de link](img/testes_form-validation.gif)
* Verificar se vídeos possuem legendas e se áudios possuem transcrição [[10](#nota10)];
* Validar (de forma automática) acessibilidade das páginas usando o [Wave](http://wave.webaim.org/) [[1](#nota01)];
* Validar (de forma automática) HTML das páginas usando o [W3C Validator](http://validator.w3.org/);
* Verificar funcionamento das páginas sem o uso de JavaScript, Flash ou outro(s) plugin(s);

#### Referências

* <a id="nota12"></a>[WebAIM - People with Disabilities on the Web](http://webaim.org/intro/#people)
* <a id="nota01"></a>[Issue #3: Acessibilidade - Qual norma e validador devemos utilizar?](https://github.com/a2comunicacao/metodologia/issues/3)
* [Acessibilidade na Web: Principais problemas e Soluções - FISL14](http://www.slideshare.net/julianafrost/acessibilidade-na-web-principais-problemas-e-solues)
* <a id="nota04"></a>[WebAIM - "Skip Navigation" Links](http://webaim.org/techniques/skipnav/)
* <a id="nota06"></a>[WebAIM - Screen reader users often navigate from link to link, skipping the text in between](http://webaim.org/techniques/hypertext/#link_to_link)
* <a id="nota39"></a>[Why Your Links Should Never Say “Click Here”](http://uxdesign.smashingmagazine.com/2012/06/20/links-should-never-say-click-here/)
* <a id="nota07"></a>[WebAIM - Creating Accessible Forms](http://webaim.org/techniques/forms/controls)
* <a id="nota08"></a>[WebAIM - Presenting Document Structure](http://webaim.org/techniques/aria/#structure)
* <a id="nota09"></a>[W3C - ARIA2: Identifying required fields with the aria-required property](http://www.w3.org/TR/WCAG20-TECHS/ARIA2.html)
* <a id="nota10"></a>[WebAIM - Usable and Accessible Form Validation and Error Recovery](http://webaim.org/techniques/formvalidation/#error)
* <a id="nota11"></a>[WebAIM - Web Captioning Overview](http://webaim.org/techniques/captions/)

--

### <a id="cms"></a>CMS

* Incluir uma página
* Editar uma página existente
* Apagar uma página
* ...

#### Wordpress

* Incluir testes específicos para WP

#### A2siteBox

* Incluir testes específicos para A2siteBox

--

### <a id="compatibilidade"></a>Compatibilidade (Cross-browser)

*Funcionamento em diferentes browsers, sistemas operacionais e servidores.*

Uma causa comum de falhas em websites é a falta de compatibilidade entre browsers, aplicativos, sistemas operacionais ou ambientes de produção que diferem muito do original. Atualmente um teste cross-browser eficiente deve ser feito nos principais browsers (Chrome, Internet Explorer, Firefox e Safari), entre sistemas operacionais (PC e Mac) e entre dispositvos (Smartphone, Tablet e Desktop).

#### O que deve ser observado em um teste cross-browser [[14](#nota14)]?

1. Diagramação das páginas e posição dos elementos está compatível com o layout original?
1. Links, menus e dropdowns são fáceis de clicar em interfaces de toque (tablets e smartphones)?	
1. Elementos clicáveis mudam visualmente ao passar o cursor do mouse (*mouse hover*)?
1. Efeitos de animação, transições da interface e janelas modais (popups) estão funcionando corretamente?
1. Fontes tipográficas estão bem renderizadas e num tamanho coerente?
1. A resolução das imagens é suficiente? Elas estão adaptadas para telas LCD ([Retina Display](http://pt.wikipedia.org/wiki/Tela_retina))?
1. Existe alguma barra de navegação horizontal que não foi planejada?
1. Palavras com acento são exibidas corretamente?
1. Validação e envio de formulários está funcionando?

#### Checklist

* Verificar páginas no Desktop (PC ou Mac) nas seguintes resoluções: 1024x768, 1280x800, 1280x1024, 1366x768, 1440x900 e 1920x1080 (Dica: utilizar o _resize_ da extensão [Web Developer](http://chrispederick.com/work/web-developer/) [[13](#nota13)];
* Verificar páginas no Firefox para Mac (versão atual);
* Verificar páginas no Firefox para Windows (versão atual);
* Verificar páginas no Internet Explorer 7;
* Verificar páginas no Internet Explorer 8;
* Verificar páginas no Internet Explorer (versão atual);
* Verificar páginas no Chrome para Mac (versão atual);
* Verificar páginas no Chrome para Windows (versão atual);
* Verificar páginas no Safari para Mac (versão atual);
* Verificar páginas no Safari para iPad (versão atual);
* Verificar páginas no Safari para iPhone (versão atual);
* Verificar se os campos de formulário estão marcados com o parâmetro TYPE correto [[38](#nota38)];
* Verificar impressão das páginas;

#### Referências

* <a id="nota13"></a>[W3Counter - Global Web Stats](http://www.w3counter.com/globalstats.php)
* <a id="nota14"></a>[Issue #6: Compatibilidade - O que deve ser observado em um teste cross-browser?](https://github.com/a2comunicacao/metodologia/issues/6)
* [Codrops - UI Design guidelines for Responsive Design](http://tympanus.net/codrops/2013/01/21/ui-design-guidelines-for-responsive-design/)
* [Smashing Magazine - Review Of Cross-Browser Testing Tools](http://www.smashingmagazine.com/2011/08/07/a-dozen-cross-browser-testing-tools/)
* [Techniques for mobile and responsive cross-browser testing: An Envato case study](http://webuild.envato.com/blog/techniques-for-mobile-and-responsive-cross-browser-testing/)
* <a id="nota38"></a>[Dive Into HTML5 - Uma forma de loucura](http://diveintohtml5.com.br/forms.html)


--

### <a id="conteudo"></a>Conteúdo

*Revisão dos textos, links externos, imagens, vídeos e áudios.*

O conteúdo é a parte mais importante de um website. Além de revisão ortográfica, deve-se avaliar o contexto e os pequenos trechos de texto ([*microcopy* [[15](#nota15)]) presentes na interface.

#### Checklist

* Revisar ortografia e sintaxe dos títulos e do corpo do texto;
* Revisar ortografia de "textos ocultos" como mensagens de validação de formulários, tooltips e alertas de janelas modais (popups);
* Verificar existência de conteúdo de teste ([Lorem ipsum](http://pt.wikipedia.org/wiki/Lorem_ipsum), [Placeholders](http://placehold.it/), etc.);
* Revisar relevância das imagens, legendas e créditos;
* Verificar existência de textos em outros idiomas;
* Verificar se a acentuação nos títulos está funcionando corretamente;
* Verificar se é possível selecionar, copiar e colar os principais textos da página;
* Verificar existência de palavras viúvas em títulos e parágrafos importantes;
* Verificar variação na grafia de palavras iguais (Ex.: websites, web sites, sites e sítios);
* Verificar tratamento unificado das listas ordenadas (Ex.: Deve-se usar ponto e vírgula no final de cada sentença?);
* Verificar se as redes sociais relacionadas ao website estão linkadas corretamente;
* Verificar se elementos de texto possuem formatação visual (links, listas, negrito, itálico, bloco, código, etc.); 
* Em caso de migração ou redesign, verificar se todo conteúdo está sendo considerado (notícias, imagens, vídeos, áudios, posts, comentários, etc.);

#### Referências

* <a id="nota15">15.</a> [Smashing Magazine - Five Ways To Prevent Bad Microcopy](http://uxdesign.smashingmagazine.com/2013/06/17/five-ways-prevent-bad-microcopy/)

--

### <a id="funcional"></a>Funcional

*Entrada e saída de dados.*

Testes funcionais estão relacionadas a entrada e saída de dados. Clicar em links, preencher um cadastro e realizar uma busca são entrada de dados feitas pelo usuário na expectiva de obter uma resposta satisfatória do software. 

#### Checklist


* Verificar links quebrados na barra de navegação e no corpo do texto usando a extensão [LinkChecker](https://addons.mozilla.org/pt-br/firefox/addon/linkchecker/) (Firefox) ou [Check My Links](https://chrome.google.com/webstore/detail/check-my-links/ojkcdipcgfaekbeaelaapakgnjflfglf/) (Chrome);
* Verificar preenchimento dos formulários (validação, envio e recebimento);
	* Existe alguma validação nos campos de preenchimento?
	* Os campos marcados como obrigatórios estão sendo validados?
	* Em caso de erro ou conexão lenta, existe alguma mensagem de feedback para o usuário?
	* Os emails designados para serem destinatários estão recebendo o formulário?
	* Em caso do usuário solicitar ou receber uma confirmação por email, ela está sendo enviada e exibida corretamente?
	* Em caso de upload, é possível enviar os arquivos? Existe algum limite de tamanho ou formato e isso está claro para o usuário?
* Verificar sistemas com acesso restrito (login e senha):
	* É possível fazer login e logout no sistema?
	* Existe alguma forma automática do usuário recuperar uma senha perdida?
* Verificar funcionalidades de comércio eletrônico;
	* É possível adicionar, remover ou atualizar itens do carrinho de compras?
	* O processo de checkout está funcionando corretamente?
* Verificar funcionamento dos feeds de RSS;
* Verificar sistema de busca interna;
	* A busca está retornando resultados satisfatórios e relevantes ao usuário?
	* É possível compartilhar o link de resultado de uma busca específica?
	* O que acontece se realizarmos uma busca com o campo vazio?
	* O resultado da busca está incluindo resultados de áreas de acesso restrito que não devem ser exibidos?
* Verificar funcionamento de elementos de áudio e vídeo, incluido controles de volume e execução (parar, avançar e voltar);
* Verificar funcionamento do aplicativo de mapa;
	* É possível compartilhar o link de resultado de uma busca ou ponto específico?
	* Em caso de erro ou conexão lenta, existe alguma mensagem de feedback para o usuário?
* Verficar funcionamento de outros sistemas complexos e específicos que não estejam listados acima;
* Verificar existência de favicons, [touch icons](http://mathiasbynens.be/notes/touch-icons) e [screen site tiles](http://www.buildmypinnedsite.com/);
* Verificar existência da página de erro 404;
* Verificar existência da página de manutenção;
* Verificar se existe algum link para a URL de desenvolvimento que pode quebrar quando o website entrar no ar;

--

### <a id="newsletter"></a>Newsletter

* Verificar formatação da newsletter no MS Outlook;
* Verificar formatação da newsletter no Hotmail;
* Verificar formatação da newsletter no Yahoo! Mail;
* Verificar formatação da newsletter no Gmail;
* Verificar se todas as imagens `<img>` possuem os atributos _display:block_ e _alt_;
* Verificar se todos os links `<a>` possuem o atributo _outline:none_;
* Utilizar sempre o atributo _valign=top_ nas `<td>`;
* As imagens devem possuir URL absoluta;
* Verificar o preenchimento da tag `<title>`;

#### Referências

* <a id="nota03"></a>[Campaign Monitor - Email Client Popularity](http://www.campaignmonitor.com/resources/will-it-work/email-clients/)
* [Newsletter](Newsletter)

--

### <a id="performance"></a>Performance

*Capacidade de resposta e estabilidade do website.*

Testes de performace são realizados para determinar como um sistema roda em termos de capacidade de resposta e estabilidade sob uma carga de trabalho particular. Também pode servir para investigar, mensurar, validar ou verificar escalabilidade, confiabilidade e uso de recursos.

* Verificar existência de código CSS e JS inline ou incorporado no HTML [[22](#nota22)];
* Verificar posicionamento dos estilos (topo) e scripts (rodapé) no HTML [[23](#nota23)];
* Verificar se arquivos [JavaScript](https://github.com/zenorocha/browser-diet/wiki/Tools#minify-your-script) e [CSS](https://github.com/zenorocha/browser-diet/wiki/Tools#minify-your-stylesheets) estão comprimidos/minificados;
* Verificar se folhas de estilo estão combinadas em um único arquivo CSS [[24](#nota24)];
* Verificar se arquivo CSS está sendo chamado com `<link>` e não com `@import` [[25](#nota25)];
* Verificar se código Javascript de terceiros estão sendo carregados de forma assíncrona [[26](#nota26)];
* Verificar o uso desnecessário `document.write` no código Javascript [[27](#nota27)];
* Verificar se scripts estão combinados em um único arquivo JS [[28](#nota28)];
* Verificar se bibliotecas JS, como jQuery, estão atualizadas;
* Verificar uso de CSS Sprites [[29](#nota29)];
* Verificar se imagens não estão sendo redimensionadas por CSS ou HTML [[30](#nota30)];
* Verificar otimização das imagens [[31](#nota31)];
* Verificar uso de cache dos arquivos no servidor [[32](#nota32)];
* Verificar compressão de arquivos pelo servidor (GZIP) [33](#nota33)];
* Verificar e anotar o tempo de carregamento e peso da página utilizando o [YSlow](http://developer.yahoo.com/yslow/), [Page Speed Insights](https://developers.google.com/speed/pagespeed/insights) ou [Page Speed Insights Browser Extension](https://developers.google.com/speed/pagespeed/insights_extensions);
* Verificar uso de CDNs para carregamento de bibliotecas e frameworks públicos [[34](#nota34)];
* Validar arquivos CSS utilizando o [CSSLint](http://csslint.net/) [[2](#nota02)];
* Validar arquivos Javascript utilizando o [JSLint](http://www.jslint.com/)[[5](#nota05)];

#### Referências

* <a id="nota22">[Browser Diet - Evite código inline/incorporado no HTML](http://browserdiet.com/pt/#avoid-inline)
* <a id="nota23">[Browser Diet - Estilos no topo, scripts no rodapé](http://browserdiet.com/pt/#css-on-top-js-on-bottom)
* <a id="nota24">[Browser Diet - Combine vários arquivos CSS em um só](http://browserdiet.com/pt/#combine-css)
* <a id="nota25">[Browser Diet - Prefira <link> a @import](http://browserdiet.com/pt/#prefer-link-over-import)
* <a id="nota26">[Browser Diet - Carregue código de terceiros de forma assíncrona](http://browserdiet.com/pt/#3rd-party-async)
* <a id="nota27">[Browser Diet - Evite document.write](http://browserdiet.com/pt/#documentwrite)
* <a id="nota28">[Browser Diet - Combine vários arquivos js em um só](http://browserdiet.com/pt/#combine-js)
* <a id="nota29">[Browser Diet - Use CSS Sprites](http://browserdiet.com/pt/#sprites)
* <a id="nota30">[Browser Diet - Não escale imagens direto no código](http://browserdiet.com/pt/#scale)
* <a id="nota31">[Browser Diet - Otimize suas imagens](http://browserdiet.com/pt/#optimize)
* <a id="nota32">[Browser Diet - Habilite o cache dos arquivos](http://browserdiet.com/pt/#cache)
* <a id="nota33">[Browser Diet - GZIP](http://browserdiet.com/pt/#gzip)
* <a id="nota34">[YSlow - Use a Content Delivery Network](http://developer.yahoo.com/performance/rules.html#cdn)
* [Smashing Magazine - Writing Fast, Memory-Efficient JavaScript](http://coding.smashingmagazine.com/2012/11/05/writing-fast-memory-efficient-javascript/)
* [Superhero.js - Uma coleção de artigos, vídeos e apresentações sobre criação, teste e manutenção de código Javascript.]( http://superherojs.com/)
* <a id="nota02"></a>[Issue #2: CSS - Por que validar e qual validador devemos utilizar?](https://github.com/a2comunicacao/metodologia/issues/2)
* <a id="nota05"></a>[Issue #4: Javascript - Por que validar e qual validador devemos utilizar?](https://github.com/a2comunicacao/metodologia/issues/4)

--

### <a id="seguranca"></a>Segurança

*Armazenamento de dados confidenciais, possibilidade de invasão do sistema e rotina de backup.*

Testes de segurança são essenciais para verificar se dados confidenciais estão armazenados devidamente, se não há possibilidade de invasão do sistema e se existe uma rotina de backup.

* Verificar se páginas sensíveis ou protegidas estão declaradas no robots.txt [[35](#nota35)];
* Verificar espaço/capacidade em disco para armazenamento dos arquivos no servidor;
* Verificar rotina de backup dos arquivos e do banco de dados (e testar a recuperação dos dados);
* Verificar agenda de atualização do CMS e dos plugins;
* Verificar se mensagens de erro do servidor estão desativadas para o usuário;
* Verficar configuração de serviço monitoramento de erros do servidor com avisos por email ou SMS (Ex.: [Uptime Robot](http://www.uptimerobot.com));
* Verificar se os endereços de email estão mascarados contra spammers usando o [Email Encoder](http://www.wbwip.com/wbw/emailencoder.html);
* Verificar requisitos mínimos de segurança utilizando o [Websecurify Foundation](https://suite.websecurify.com/foundation);

#### Referências

* <a id="nota35"></a>[Google Webmasters - Bloquear ou remover páginas usando um arquivo robots.txt](https://support.google.com/webmasters/answer/156449?hl=pt-BR)

--

### <a id="seo"></a>SEO e Marketing

*Boas práticas de código e conteúdo para garantir visibilidade nos mecanismos de busca.*

É importante avaliar se boas práticas de código e conteúdo estão sendo seguidas para garantir uma boa visibilidade do website ou software nos mecanismos de busca.

* Verificar existência e relevância de keywords nos títulos das páginas;
* Verificar existência, relevância e tamanho (entre 150 a 160 caracteres [[19](#nota19)]) das metas descriptions utilizando a extensão [Meta SEO Inspector (Chrome)](https://chrome.google.com/webstore/detail/meta-seo-inspector/ibkclpciafdglkjkcibmohobjkcfkaef/);
* Verificar configuração de URL canônica no servidor [[16](#nota16)];
* Verificar formatação e estruturação das URL amigáveis [[17](#nota17)];
* Verificar marcação e semântica do código HTML [[36](#nota36)];
* Verificar funcionamento dos links de compartilhamento e como estão sendo exibidos nas redes sociais [[37](#nota36)];
* Verificar existência de arquivo XML Sitemap com permissão de escrita;
* Verificar configuração do [Google Webmaster Tools](https://www.google.com/webmasters/) e [Bing Webmaster Tools](http://www.bing.com/toolbox/webmaster);
* Verificar funcionamento da ferramenta de monitoramento de acessos ([Ex.: Configuração de metas no Google Analytics](http://www.google.com/analytics/)) [[18](#nota18)];
* Em caso de migração ou redesign, verificar se as URLs alteradas estão sendo redirecionadas através do código de status HTTP 301;
* Verificar aparência do website nas páginas de resultados de busca (SERPs) [[21](#nota21)];  	

#### Referências

* <a id="nota19"></a>[Moz - Meta Description](http://moz.com/learn/seo/meta-description)
* <a id="nota16"></a>[Matt Cutts - SEO advice: url canonicalization](http://www.mattcutts.com/blog/seo-advice-url-canonicalization/)
* <a id="nota17"></a>[Webdesigntuts+ - How to Create an SEO-Friendly URL Structure](http://webdesign.tutsplus.com/articles/seo-articles/seo-friendly-url-structure/)
http://www.google.com/analytics/learn/setupchecklist.html
* <a id="nota18"></a>[Google Analytics - Aproveite ao máximo seus relatórios](http://www.google.com/analytics/learn/setupchecklist.html)
*  <a id="nota20">[Issue #7: SEO - Uso do arquivo human.txt?](https://github.com/a2comunicacao/metodologia/issues/7)
* <a id="nota21">[Google Webmasters - Buscar como o Google](https://support.google.com/webmasters/answer/158587?hl=pt-BR)
* <a id="nota36">[Issue #10](https://github.com/a2comunicacao/metodologia/issues/10)
* <a id="nota37">[Define an Open Graph object](https://developers.facebook.com/docs/web/tutorials/scrumptious/open-graph-object/)

--

### <a id="usabilidade"></a>Usabilidade

*Facilidade do website de ser compreendido e manipulado pelo usuário.*

** Essa versão ainda é um rascunho! **

Testes de usabilidade tem por objetivo verificar a facilidade que o software ou website possui de ser claramente compreendido e manipulado pelo usuário.

* Realizar testes de usabilidade com usuários reais;
* Realizar análise heurítica de usabilidade;
* Verificar o estado das telas em branco;
* Feedback para o usuário;
* http://www.webdesignerdepot.com/2013/06/how-to-approach-usability-testing/

--

### <a id="verificacaodelinks"></a> Verificação de links

* Frequência de verificações: Todas as segundas
* Abrangência: Somente na homepage
* Software utilizado: Extensão para Firefox chamado [LinkChecker](https://addons.mozilla.org/pt-br/firefox/addon/linkchecker/)

#### Instalação e como usar
Após adicionar a extensão ao Firefox, um ícone de "certo" aparecerá no Browser. 
Para fazer a verificação dos links, abra o site que deseja verificar, clique no ícone e aguarde enquanto a extensão roda. Não é possível rodar em mais de um site por vez. 
Os links ficarão marcados com cores:
* Verde: Link funcionando corretamente;
* Amarelo: Link demorando para carregar ou quebrado;
* Vermelho: Link quebrado.

Quando os ícones estiverem amarelos/vermelhos, abra-o em uma nova aba e veja se ele carrega. Se carregar, OK. Caso esteja quebrado, faça uma busca no site por outro link que corresponda ao mesmo serviço e informe ao atendimento via Basecamp sobre o problema, o cliente então informará se o link encontrado está correto ou qual link deverá ser usado (ou até removido). Lembrando que o link não funcionando pode ser apenas uma instabilidade no site. 

--

## Referências

* [HTML5 Boilerplate documentation](https://github.com/h5bp/html5-boilerplate/blob/v4.2.0/doc/TOC.md)
* [Wikipedia - Software testing](http://en.wikipedia.org/wiki/Software_testing)
* [Re-launching The Ultimate Website Launch Checklist](http://www.boxuk.com/blog/relaunching-the-ultimate-website-launch-checklist/)
