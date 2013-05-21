---
layout: page
title: Verificação de links da homepage
subtitle: 
category: testes
---

* Frequência de verificações: Todas as segundas
* Sites: [São Paulo SP](http://www.saopaulo.sp.gov.br/), [Cidadão SP](http://www.cidadao.sp.gov.br/), [Desenvolve SP](http://desenvolvesp.com.br/), [Canal do Empresário](http://www.canaldoempresario.com.br/) e [Idort](http://idort.com.br/). 
* Software utilizado: Extensão para Firefox chamado [LinkChecker](https://addons.mozilla.org/pt-br/firefox/addon/linkchecker/)

##Instalação e como usar
Após adicionar a extensão ao Firefox, um ícone de "certo" aparecerá no Browser. 
Para fazer a verificação dos links, abra o site que deseja verificar, clique no ícone e aguarde enquanto a extensão roda. Não é possível rodar em mais de um site por vez. 
Os links ficaram marcados com cores:
* Verde: Link funcionando corretamente;
* Amarelo: Link demorando para carregar ou quebrado;
* Vermelho: Link quebrado.

Quando os ícones estiverem amarelos/vermelhos, abra-o em uma nova aba e veja se ele carrega. Se carregar, OK. Caso esteja quebrado, faça uma busca no site por outro link que corresponda ao mesmo serviço e informe ao atendimento via Basecamp sobre o problema, o cliente então informará se o link encontrado está correto ou qual link deverá ser usado (ou até removido). Lembrando que o link não funcionando pode ser apenas uma instabilidade no site. 

*Obs.:* Não estamos com acesso ao FTP da IO (São Paulo SP e Cidadão SP) portanto alguns links já não estão funcionando há algum tempo e foram listados no Basecamp para uma futura alteração. Verifico então se não há nenhum link novo quebrado e, se tiver, deixo a tarefa aberta. Caso contrário, fecho a tarefa.

Caso o acesso seja liberado, os links que conseguimos trocar sem ajuda da equipe de sistemas são os que estão no Cidadão nos blocos:
"Mais acessados" (sis/in/class_busca.php (linha 1022)) e "Eventos da vida"(lib/content/themes/cidadaosp/in/eventosdavida.php). Lembrando que estes projetos não estão no Git e são acessados diretamente pela pasta em Doors > Sites.