# Google Analytics

## Plano de Mensuração

Passos para definir o plano de mensuração:

1. Documentar o(s) objetivo(s) de negócio(s);
2. Identificar as estratégias e táticas;
3. Definir os KPI's (Key Performance Indicators);
4. Definir os segmentos;

OBS: Para documentar essas informações, use o Google Drive. 


## Documentação da Infraestrutura/Ambiente

Informações básicas para a documentação da  Infraestrutura/TI:

* Qual é o parâmetro de query string? (ex.: q)
* Há redirecionamentos feitos no servidor? Se sim, quais?
* Existem páginas que possuem eventos em Flash ou Ajax?
* O website possui subdomínios? Eles serão análisados?
* O website é responsível? Quais são os breakpoints?

OBS: Para documentar essas informações, use o Google Drive. 

## Plano de Implementação

Etapa 1

1. Criar uma conta no Google Analytics;
2. Criar uma propriedade com o nome do website;
3. Criar duas visualizacões: _Unfiltered View_ - `3 - www.nomedowebsite.com.br - unfiltered view` e _Test View_ `2 - www.nomedowebsite.com.br - test view`
4. Instalar o snippet (código de rastreamento) do Google Analytics no website

Etapa 2

Na visualização _Test View_, configure:

1. Filtros;
2. Goals (Metas);
3. Painel de Controle Personalizado / Relatórios Customizados.

Etapa 3

Uma vez que as configurações implementadas na visualização _Test View_ surtirem efeito, faça uma cópia dela dando o nome de _Master View_ `1 - www.nomedowebsite.com.br - master view`. 

OBS 1: Toda e qualquer ajuste das metas e filtros devem ser feitos primeito na visualização _Test View_ e depois repassados a visualização _Master View_. 
OBS 2: Não exclua a visualização _Unfiltered View_. Ela tem a função de mensurar os dados brutos do website e possui o caráter de ser sempre um backup. 

### Mais informações

* [Criando um plano de mensuração](https://www.youtube.com/watch?v=EpDA3XaELqs)
* [Configurando filtros básicos](https://www.youtube.com/watch?v=dzwRzUEc_tA)
* [Configurando os gols (metas) no Google Analytics](https://www.youtube.com/watch?v=tisVDXFgapU)
* [Como criar Propriedades / Visualizações ](https://www.youtube.com/watch?v=OyixJ7A9phg)

