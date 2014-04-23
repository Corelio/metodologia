# SASS

## Instalação
### MAC / Linux
O SASS é um biblioteca do Ruby. Por padrão, MAC e Linux já vem com o Ruby instalado, então basta que instalemos o SASS. No terminal, digite: 
`sudo gem install sass`

Obs.: Caso a versão do sistema operacional não seja a mais recente, pode ocorrer um erro, pedindo que rodemos algum comando para atualização, como esse: `gem install --version '~> 0.9.1' rb-fsevent`.

### Windows
[Este tutorial](http://www.tidbits.com.br/desenvolvendo-css-de-forma-mais-produtiva-usando-sass)  explica como instalar o Ruby e o SASS no Windows.

## Utilização
As principais vantagens do SASS são você poder utilizar _mixins_ e funções para realizar cálculos, a possibilidade de criar vários arquivos de estilo melhorando assim a modularização e divisão, além de gerar apenas um arquivo de estilo.

A extensão dos arquivos é _.scss_ e, em um arquivo específico você importa todos os arquivos SASS que criou. Seu arquivo ficaria mais ou menos assim:

````
@import "normalize";
@import "base";
@import "typography";
@import "layout";
````

Para rodar, você precisa abrir o terminal na pasta do projeto e passar a seguinte instrução:

` sass --watch diretorioSASS/arquivo.scss:diretorioCSS/arquivo.css --style compressed --no-cache`

Resumidamente, o comando acima pega o arquivo principal que importa todos os arquivos _.scss_ e compila em um arquivo CSS minificado.
