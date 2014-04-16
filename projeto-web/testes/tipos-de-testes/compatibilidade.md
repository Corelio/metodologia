# Compatibilidade (Cross-browser)
Funcionamento em diferentes browsers, sistemas operacionais e servidores. Atualmente o teste deve ser feito nos principais browsers (Chrome, Internet Explorer, Firefox, Safari e Opera), entre sistemas operacionais (PC e Mac) e entre dispositivos (Smartphone, Tablet e Desktop).

## O que deve ser observado em um teste cross-browser? [[1]](#compatibilidade1)
1. A diagramação das páginas e posição dos elementos estão compatíveis com o layout original?;
2. Links, menus e dropdowns são fáceis de clicar em interfaces de toque (tablets e smartphones)?;
3. Elementos clicáveis mudam visualmente ao passar o cursor do mouse (mouse over)?;
4. Efeitos de animação, transições da interface e janelas modais (pop-ups) estão funcionando corretamente?;
5. Fontes tipográficas estão bem renderizadas e num tamanho coerente?;
6. A resolução das imagens é suficiente? Elas estão adaptadas para telas LCD ([Retina display](http://pt.wikipedia.org/wiki/Tela_retina))?;
7. Existe alguma barra de navegação horizontal que não foi planejada?;
8. Palavras com acento são exibidas corretamente?;
9. Validação e envio de formulários está funcionando?

## Checklist
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

## Referências

* [<a name="compatibilidade1"></a>1] - [Issue #6 - Compatibilidade - O que deve ser observado em um teste cross-browser?](https://github.com/a2comunicacao/metodologia/issues/6)
* [<a name="compatibilidade2"></a>2] - [W2Counter - Global Web Stats](http://www.w3counter.com/globalstats.php)
* [<a name="compatibilidade3"></a>3] - [Dive into HTML5 - Uma forma de loucura](http://diveintohtml5.com.br/forms.html)
* [Codrops - UI Design guidelines for Responsive Design](http://tympanus.net/codrops/2013/01/21/ui-design-guidelines-for-responsive-design/)
* [Smashing Magazine - Review of cross-browser testing tools](http://www.smashingmagazine.com/2011/08/07/a-dozen-cross-browser-testing-tools/)
* [Techniques for mobile and responsive cross-browser testing: An Envato case study](http://webuild.envato.com/blog/techniques-for-mobile-and-responsive-cross-browser-testing/)
