

## SASS

### Instalação

#### MAC / Linux

Por padrão já vem com o Ruby instalado, basta que instalemos o Sass (que é uma *biblioteca* do Ruby):

1. No terminal digite:

`sudo gem install sass`

**Obs.:** Caso a versão do sistema operacional não seja a mais recente, pode ocorrer um erro, pedindo que rodemos algum comando para atualização, como esse:
`gem install --version '~> 0.9.1' rb-fsevent`

#### Windows

[Tutorial](http://www.tidbits.com.br/desenvolvendo-css-de-forma-mais-produtiva-usando-sass) explicando como instalar o *Ruby* e o *Sass* no Windows.

### Utilização

As principais vantagens do SASS são você poder utilizar _mixins_ e funções para realizar cálculos, a possibilidade de criar vários arquivos de estilo melhorando assim a modularização e divisão, além de gerar apenas um arquivo de estilo.

A extensão dos arquivos é `.scss` e, em um arquivo específico você importa todos os arquivos SASS que criou. Seu arquivo ficaria mais ou menos assim:
```
@import "normalize";
@import "base";
@import "typography";
@import "layout";
```

Para rodar, você precisa abrir o termina na pasta do projeto e passar a seguinte instrução: 
```
  sass --watch diretorioSASS/arquivo.scss:diretorioCSS/arquivo.css --style compressed --no-cache
```

> Resumidamente o comando acima pega o arquivo principal que importa todos os arquivos `.scss` e compila em um arquivo CSS minificado.
