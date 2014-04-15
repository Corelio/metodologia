# Análise de Keywords

## Exportando dados
Para mensurarmos quais dados são mais procurados e rejeitados em um website, fazemos um estudo com base nos 100 primeiros itens do relatório de busca orgânica. Para retirar esse relatório, siga esses passos:

1. Logue no Google Analytics;
2. No menu da esquerda selecione _aquisição > palavras-chave > orgânico_;
3. No calendário, selecione o período de tempo que deseja consultar;
4. Selecione _exportar > .csv_.

Para trabalharmos nesse estudo, utilizamos o Excel. O .csv virá com os dados mostrados em apenas uma linha, então é preciso formatá-lo extraindo as seguintes informações:
* Keywords;
* Visits;
* Bounce rate.

Nesse momento temos uma listagem das keywords mais buscadas, porém, não é possível ter uma visão geral dos termos pois existem vários que são similares mas que estão desagrupados.

**Importante**: O termo “not provided” se refere às pessoas que estão logadas no serviços Google. Saiba mais em: [(Not Provided) - Por que esse termo aparece entre palavras-chave que trazem tráfego e como lidar](http://resultadosdigitais.com.br/blog/not-provided-por-que-esse-termo-aparece-entre-as-palavras-chave-que-trazem-trafego-e-como-lidar/)

## Organizando dados

Ainda no arquivo geral, começamos a trabalhar em novas colunas ao lado, agrupando os termos similares. Ex.: Quem busca pelo termo “Instagram” pode ter usado os seguintes termos:

* “Horários de mais audiência no Instagram”;
* “Duas ou mais fotos no Instagram”;
* “Hashtags mais usadas no Instagram”;
* “Mais likes no Instagram”.

Neste exemplo, agrupamos esses termos e nomeamos de uma forma mais amigável, utilizando apenas o termo “Instagram”.

Na coluna “Visits”, somamos todos os valores referentes aos termos. Na coluna “Bounce rate”, somamos todas as porcentagens do termo e depois dividimos pela quantidade de vezes que esse termo apareceu, resultando na média da rejeição total daquele termo.

Após esse organização e agrupamento, provavelmente os 100 termos serão reduzidos pela metade. Neste momento, decidimos quantos termos realmente queremos estudar. Atualmente trabalhamos com os primeiros quinze.

Dependendo do website, organizamos os termos por “categorias”. Ex.: Termos “Aplicativos para viagem”, “Aplicativo de controle financeiro” e “Aplicativo comunicação equipe android” estão ligados ao termo “Aplicativos”. Esse termo usado na categoria pode ou não estar relacionado à uma área do website.

## 15 termos mais buscados

Após fecharmos a primeira planilha, criamos uma nova, listando os 15 termos mais buscados. Os campos criados nesse novo relatório são:

* Palavra-chave;
* O que é?;
* Visitas;
* Taxa de rejeição (bounce rate);
* Por que apareceu?.

A partir de agora o trabalho torna-se ainda mais manual. Listamos primeiramente todos os 15 termos, utilizando como subtítulo as categorias pré-definidas anteriormente, assim como as visitas e a taxa de rejeição. Passamos então a pesquisar no próprio website sobre o que se tratam os termos buscados e preenchendo o campo “O que é?”.

Para preencher o campo “Por que apareceu?”, é preciso refazer a busca no Google pelo termo, para sabermos qual página foi indexada (as vezes no relatório bruto do GA esse link é apontado) e se ela possui um resultado de acordo com o que o usuário procurou. Nesse momento, também tentamos identificar a causa da rejeição.
