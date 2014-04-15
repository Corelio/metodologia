# Plano de métricas

Para documentar as informações do plano de métricas, utilize o [Google Drive](https://drive.google.com/a/a2comunicacao.com.br/#folders/0B22JM_OaMGxdQjEzV0M1VGREamc)

## Plano de mensuração
Passos para definir o plano de mensuração:

1. Documentar (o)s objetivo(s) de negócio(s);
2. Identificar as estratégias e táticas;
3. Definir KPI’s (Key Performance Indicators);
4. Definir os segmentos.

## Documentação da infraestrutura/ambiente
Informações básicas para a documentaão da insfraestrutura/TI:

* Qual é o parâmetro de query string? (Ex.: q);
* Há redirecionamento feitos no servidor? Se sim, quais?
* Existem páginas que possuem eventos em Flash ou Ajax?;
* O website possui subdomínios? Eles serão analisados?
* O website é responsível? Quais são os breakpoints?
* Quais events tracking implementados? E como foram implementados?

## Plano de implementação

**ETAPA 1**

1. Criar uma conta no Google Analytics;
2. Criar uma propriedade com o nome do website;
3. Criar duas visualizações: 
* **Unfiltered View**: `3 - www.nomedowebsite.com.br - unfiltered view`;
* **Test View**: `2 - www.nomedowebsite.com.br - test view`;
4. Instalar o snippet (código de rastreamento) do Google Analytics no website.

**ETAPA 2**

Na visualização **Test view**, configure:
1. Filtros;
2. Goals (metas);
3. Painel de controle personalizado/relatórios customizados.

**ETAPA 3**

Uma vez que as configurações implementadas na visualização **Test view** surtirem efeito, faça uma cópia dela dando o nome de **Master view** `1. www.nomedosite.com.br - master view.

**Observações**
* Todo e qualquer ajuste das metas e filtros devem ser feitos primeiro na visualização **Test view** e depois repassados a visualização **Master view**;
* Não exclua a visualização **Unfiltered view**, ela tem a função de mensurar e fazer backup dos dados brutos de um website.

## Referências

* [Criando um plano de mensuração](https://www.youtube.com/watch?v=EpDA3XaELqs)
* [Configurando filtros básicos](https://www.youtube.com/watch?v=dzwRzUEc_tA)
* [Configurando os goals (metas) no Google Analytics](https://www.youtube.com/watch?v=tisVDXFgapU)
* [Como criar propriedades/visualizações](https://www.youtube.com/watch?v=OyixJ7A9phg)
* [Implementação de Event Tracking](https://developers.google.com/analytics/devguides/collection/analyticsjs/events?hl=pt-BR#implementation)
