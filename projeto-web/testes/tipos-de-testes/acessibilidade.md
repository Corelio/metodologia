# Acessibilidade

Estima-se que 20% da população mundial possue algum tipo de deficiência [[1]](#acessibilidade1). Além de ser comercialmente imprudente excluir esses clientes em potencial, para a maioria dos governos é uma questão de seguir a legislação. Testes de acessiblidade incluem o cumprimento das normas como [ADA](http://www.ada.gov/index.html), [Seção 508](https://www.section508.gov) ou [WCAG (W3C)](http://www.w3.org/TR/WCAG/).

## Checklist
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

## Referências

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

##Tipos de testes
* [Acessibilidade](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/testes/tipos-de-testes/acessibilidade.md#acessibilidade)
* CMS
* [Compatibilidade](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/testes/tipos-de-testes/compatibilidade.md#compatibilidade-cross-browser)
* [Conteúdo](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/testes/tipos-de-testes/conteudo.md#conte%C3%BAdo)
* [Funcional](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/testes/tipos-de-testes/funcional.md#funcional)
* [Newsletter](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/testes/tipos-de-testes/newsletter.md#newsletter)
* [Performance](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/testes/tipos-de-testes/performance.md#performance)
* [Segurança](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/testes/tipos-de-testes/seguranca.md#seguran%C3%A7a)
* [SEO e Marketing](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/testes/tipos-de-testes/seo.md#seo-e-marketing)
* [Usabilidade](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/testes/tipos-de-testes/usabilidade.md#usabilidade)
