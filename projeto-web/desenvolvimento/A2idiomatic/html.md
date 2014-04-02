# HTML | A2 Idiomatic

* [Sobre](https://github.com/a2comunicacao/metodologia/tree/master/projeto-web/desenvolvimento/A2idiomatic)
* [Padrões](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/desenvolvimento/A2idiomatic/padroes.md)
* [HTML](#html)
    * [Sintaxe](#sintaxe)
    * [Atributos](#atributos)
    * [Comentários](#coment%C3%A1rios)
* PHP - _em breve!_
* [CSS](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/desenvolvimento/A2idiomatic/css.md)
* JS - _em breve!_

## HTML

### Sintaxe

* Elementos inseridos dentro de outros elementos sempre devem ser indentados uma vez.
* Para nomes de classe, *ID*s ou quaisquer outros atributos, sempre use aspas dupla e não aspas simples.
* Não inclua uma barra invertida de fechamento em elementos de fechamento automático.

````html
<!DOCTYPE html>
<html>
    <head>
        <title>Título da Página</title>
    </head>
    <body>
        <img src="img/image-example.png" alt="Company">
        <h1 class="hello">Olha aí!</h1>
    </body>
</html>
````

### Atributos

Atributos HTML devem vir nessa ordem particular para uma leitura mais fácil do código.

* classe
* id
* data-*
* for|type|href

Com isso a marcação ficaria mais ou menos assim::

````html
<a class="" id="" data-modal="" href="">Example link</a>
````

### Comentários

Sempre que possível, para uma melhor leitura do código, insira comentários entre o *HTML* que possam auxiliar na compreensão geral do fluxo.

````html
<!-- Header -->
<header class="header">
    <!-- Menu principal -->
    <nav class="nav-bar">
    .....
````