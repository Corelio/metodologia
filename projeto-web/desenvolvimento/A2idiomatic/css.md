# CSS | A2 Idiomatic

* [Sobre](https://github.com/a2comunicacao/metodologia/tree/master/projeto-web/desenvolvimento/A2idiomatic#sobre)
* [Padrões](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/desenvolvimento/A2idiomatic/padroes.md)
* [HTML](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/desenvolvimento/A2idiomatic/html.md)
* PHP - _em breve!_
* [CSS](#css)
    * [Sintaxe](#sintaxe)
    * [Ordem de Declaração](#ordem-de-declara%C3%A7%C3%A3o)
* JS - _em breve!_

## CSS

### Sintaxe

* Ao agrupar seletores, mantenha cada um em uma linha diferente.
* Inclua um espaço antes da <code>{</code>.
* Coloque a chave de fechamento dos blocos de declaração em uma nova linha.
* Inclua um espaço depois de <code>:</code> em cada propriedade.
* Cada declaração deve aparecer em sua própria linha.
* Termine todas as declarações com um ponto e vírgula.
* Valores separados por vírgula devem ter um espaço depois de cada vírgula.
* Não inclua espaços depois das vírgulas em cores RGB ou RGBa, e não preceda valores com um zero à esquerda.
* Coloque em caixa baixa todos os valores hexadecimais, e.g., <code>#fff</code> ao invés de <code>#FFF</code>.
* Use valores hexadecimais abreviados quando possível, e.g., <code>#fff</code> ao invés de <code>#ffffff</code>.
* Indique os atributos de valores no seletores, e.g., <code>input[type="text"]</code>.
* Evite especificar unidade para valores zero, e.g., <code>margin: 0;</code> ao invés de <code>margin: 0px;</code>.

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

### Ordem de Declaração

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