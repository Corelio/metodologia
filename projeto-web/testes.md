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

1. Acessibilidade
2. CMS
3. Compatibilidade
4. Conteúdo
5. Funcional
6. Newsletter
7. Performance
8. Segurança
9. SEO e Marketing
10. Usabilidade

### Acessibilidade

Estima-se que 20% da população mundial possue algum tipo de deficiência [1]. Além de ser comercialmente imprudente excluir esses clientes em potencial, para a maioria dos governos é uma questão de seguir a legislação. Testes de acessiblidade incluem o cumprimento das normas como [ADA](http://www.ada.gov/index.html), [Seção 508](https://www.section508.gov) ou [WCAG (W3C)](http://www.w3.org/TR/WCAG/).

#### Checklist
* Verificar declaração de idioma na tag HTML (Ex.: `<html lang=”pt-br”>`);
* Verificar se é possível navegar pelo teclado (utilizando a tecla TAB), se existe atalho para o conteúdo principal e se ele é visível para leitores de tela [2];
* Verificar existência de landmarks (Ex.: `role=”banner”) [3];
* Verificar se links estão marcados de forma correta (Evitar o fatídico “Clique aqui”) [4][5];
* Verificar contraste de cores das páginas utilizando o [Colour contrast check](http://snook.ca/technical/colour_contrast/colour.html);
* Verificar se todos os elementos do formulário possuem etiqueta `<label>` e se essa etiqueta está associada ao elemento correto do formulário (`<id>`) [6];
* Verificar se elementos obrigatórios do formulário estão devidamente identificados (`aria-required=true`) [7];
* Verificar se o feedback do formulário direciona o usuário para o campo a ser corrigido, através de link [8]
![Verificar se feedback do formulário direciona o usuário para o campo a ser corrigido, através de link](http://lab.a2comunicacao.com.br/metodologia/testes_form-validation.gif)
* Verificar se vídeos possuem legendas e se áudios possuem transcrição [8];
* Validar (de forma automática) acessibilidade das páginas usando o [Wave](http://wave.webaim.org/) [9];
* Validar (de forma automática) HTML das páginas usando o [W3C Validator](http://validator.w3.org/);
* Verificar funcionamento das páginas sem o uso de JavaScript, Flash ou outro(s) plugin(s).

#### Referências

* [1] - [WebAIM - People with disabilities on the web](http://webaim.org/intro/#people)
* [2] - [WebAIM - “Skip navigation links](http://webaim.org/techniques/skipnav/)
* [3] - [WebAIM - Presenting document structure](http://webaim.org/techniques/aria/#structure)
* [4] - [WebAIM - Screen reader users often navigate from link to link, skipping the text in between](http://webaim.org/techniques/hypertext/#link_to_link)
* [5] - [Why your links should never say “Click here”](uxdesign.smashingmagazine.com/2012/06/20/links-should-never-say-click-here/)
* [6] - [WebAIM - Creating accessible forms](http://webaim.org/techniques/forms/controls)
* [7] - [W3C - ARIA2: Identifying required fields with the aria-required property](http://www.w3.org/TR/WCAG20-TECHS/ARIA2.html)
* [8] - [WebAIM - Usable and accesible form validation and error recovery](http://webaim.org/techniques/formvalidation/#error)
* [9] - [Issue #3: Acessibilidade - Qual norma e validador devemos utilizar?](https://github.com/a2comunicacao/metodologia/issues/3)
* [Acessibilidade na Web: Principais problemas e soluções - FISL14](http://www.slideshare.net/julianafrost/acessibilidade-na-web-principais-problemas-e-solues)
* [WebAIM - Web captioning overview](http://webaim.org/techniques/captions/)

=

### CMS

=

### Compatibilidade (Cross-browser)
Funcionamento em diferentes browsers, sistemas operacionais e servidores. Atualmente o teste deve ser feito nos principais browsers (Chrome, Internet Explorer, Firefox, Safari e Opera), entre sistemas operacionais (PC e Mac) e entre dispositivos (Smartphone, Tablet e Desktop).

#### O que deve ser observado em um teste cross-browser? [1]
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
* Verificar páginas no Desktop (PC ou Mac) nas seguintes resoluções: 1024x768, 1280x800, 1280x1024, 1366x768, 1440x900 e 1920x1080 [2] (Dica: Utilize a opção “resize” da extensão [Web Developer](http://chrispederick.com/work/web-developer/);
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
* Verificar se os campos de formulário estão marcados com o parâmetro _TYPE_ correto [3]

#### Referências

* [1] - [Issue #6 - Compatibilidade - O que deve ser observado em um teste cross-browser?
* [2] - [W2Counter - Global Web Stats](http://www.w3counter.com/globalstats.php)
* [3] - [Dive into HTML5 - Uma forma de loucura](http://diveintohtml5.com.br/forms.html)
* [Codrops - UI Design guidelines for Responsive Design](http://tympanus.net/codrops/2013/01/21/ui-design-guidelines-for-responsive-design/)
* [Smashing Magazine - Review of cross-browser testing tools](http://www.smashingmagazine.com/2011/08/07/a-dozen-cross-browser-testing-tools/)
* [Techniques for mobile and responsive cross-browser testing: An Envato case study](http://webuild.envato.com/blog/techniques-for-mobile-and-responsive-cross-browser-testing/)

=


