# A2idiomatic

** Índice **
* [Arquivos](#idiomatic1)
* [Comentários](#idiomatic2)
* [HTML](#idiomatic3)
  * [Sintaxe](#idiomatic4)
  * [Atributos](#idiomatic5)
  * [Comentários](#idiomatic6)
* [CSS](#idiomatic7)
  * [Sintaxe](#idiomatic8)
  * [Ordem de declaração](#idiomatic9)
  * [Espaçamento](#idiomatic10)
* [Referências](#idiomatic11)

=

O A2 Idiomatic é o guia de estilos de código da A2 Comunicação.Todo código, em quaquer aplicação, deve parecer como se tivesse sido escrito por uma única pessoa, independente de quantas pessoas tenham contribuído.

Seu principal objetivo então é **auxiliar no entendimento do código, principalmente numa fase posterior de manutenção**, nas linguagens mais utilizadas: HTML, CSS, JS e PHP.

## <a name="idiomatic1"></a>Arquivos
Para nomenclatura de arquivos, utilize sempre _traço_ ao invés de _underline_.
`nome-do-arquivo.html` e não `nome_do_arquivo.html`.

## <a name="idiomatic2"></a>Comentários
Independente da linguagem, os comentários devem ser sempre em inglês.

## <a name="idiomatic3"></a>HTML

### <a name="idiomatic4"></a>Sintaxe
* Elementos inseridos dentro de outros elementos sempre devem ser indentados uma vez;
* Para nomes de classes, IDs ou quaisquer outros atributos, sempre use aspas duplas;
* Não incluia uma barra invertida de fechamento em elementos de fechamento automático.

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

### <a name="idiomatic5"></a>Atributos
Atributos HTML devem vir nessa ordem particular, para uma leitura mais fácil do código:
* Classe;
* ID;
* Data-*;
* forltypelhref.

Com isso, a marcação ficaria mais ou menos assim:
````html
<a class="" id="" data-modal="" href="">Example link</a>
````

### <a name="idiomatic6"></a>Comentários
Sempre que possível, para uma melhor leitura do código, insira comentários entre o *HTML* que possam auxiliar na compreensão geral do fluxo.
````html
<!-- Header -->
<header class="header">
    <!-- Menu principal -->
    <nav class="nav-bar">
    .....
````

## <a name="idiomatic7"></a>CSS

### <a name="idiomatic8"></a>Sintaxe
* Ao agrupar seletores, mantenha cada um em uma linha diferente;
* Inclua um espaço antes da `{`;
* Coloque a chave de fechamento dos blocos de declaração em uma nova linha;
* Inclua um espaço depois de `:` em cada propriedade;
* Cada declaração deve aparecer em sua própria linha;
* Termine todas as declarações com um ponto e vírgula;
* Valores separados por vírgula devem ter um espaço depois de cada vírgula;
* Não inclua espaços depois das vírgulas em cores RGB e RGBa, e não preceda valores com um zero à esquerda;
* Coloque em caixa baixa todos os valores hexadecimais, e.g., `#fff` ao invés de `#FFF`;
* Use valores hexadecimais abreviados quando possível, e.g., `#fff` ao invés de `#ffffff`;
* Indique os atributos de valores nos seletores, e.g., `input[type="text"]`;
* Evite especificar unidade para valores zero, e.g., `margin: 0;` ao invés de `margin: 0px;`.
````css
.seletor,
.seletor-secundario,
.seletor[type="text"] {
padding: 15px;
    margin: 0 0 15px;
    background-color: rgba(0,0,0,.5);
    box-shadow: 0 1px 2px #ccc, inset 0 1px 0 #fff;
}
````

### <a name="idiomatic9"></a>Ordem de declaração
Declarações relacionadas devem ser agrupadas juntas, colocando as propriedades de posicionamento e box-model próximas do topo, seguidas por tipografia e propriedades visuais.
````css
.ordem-de-declaracao {
   /* Posicionamento */
   position: absolute;
   top: 0;
   right: 0;
   bottom: 0;
   left: 0;
   z-index: 100;
   margin: 0;
   padding: 0;

   /* Box-model */
   display: block;
   float: right;
   width: 100px;
   height: 100px;

   /* Tipografia */
   font: normal 13px "Helvetica Neue", sans-serif;
   line-height: 1.5
   color: #333;
   text-align: center;

   /* Visual */
   background-color: #f5f5f5;
   border: 1px solid #e5e5e5;
   border-radius: 3px;

   /* Diversos */
   opacity: 1;
}
````

### <a name="idiomatic10"></a>Espaçamento
Sempre utilize **4 espaços** e não tabulação.
Um _commit_ com configurações diferentes pode detectar inúmeras mudanças e talvez até conflitos, apenas pela diferença existente entre os arquivos.

## <a name="idiomatic11"></a>Referências
* [SitePoint - Title CSS: A simple approach to CSS class naming](http://www.sitepoint.com/title-css-simple-approach-css-class-naming/)
* [CSS Wizardry - Naming UI components in OOCSS](http://csswizardry.com/2014/03/naming-ui-components-in-oocss/)
* [Metodologia BEM](http://bem.info/method/)

