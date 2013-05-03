---
layout: page
title: SASS - Instalando e utilizando o SASS 
subtitle: Utilizando o Terminal (MAC)
category: sass
---

## Instalando

### MAC

Por padrão já vem com o Ruby instalado, basta que instalemos o Sass (que é uma *biblioteca* do Ruby):

1. No terminal digite:

`sudo gem install sass`

**Obs.:** Pode acontecer, caso a versão do sistema operacional não seja a mais recente, de dar um erro, pedindo que rodemos algum comando para atualização, como esse:
`gem install --version '~> 0.9.1' rb-fsevent`_

### Windows

[Tutorial](http://www.tidbits.com.br/desenvolvendo-css-de-forma-mais-produtiva-usando-sass) explicando como instalar o *Ruby* e o *Sass* no Windows.

## Utilizando o SASS

Para utilizar o Sass:

1. Crie as pastas *SASS* e *CSS* no seu projeto;
2. Crie seus arquivos de estilo com a extensão `.scss` dentro da pasta *SASS* (no [repositório do Grid A2](https://github.com/a2comunicacao/Grid-A2/tree/master/sass), deixamos por padrão alguns arquivos iniciais);
3. Ainda dentro da pasta *SASS*, crie um arquivo que vai importar todos os arquivos de estilo (por padrão utilize `main.scss` ou `style.scss`):
  ```
  @import "normalize";
  @import "base";
  @import "typography";
  @import "font-awesome";
  ```

4. Agora, utilizando o terminal, entramos na pasta do projeto: 
  ```
  cd nomedoprojeto
  ```
5. Dentro da pasta do projeto, precisamos passar um comando para o *SASS* ficar vigiando nossos arquivos e compilar em um arquivo de saída:
  ```
  sass --watch sass/main.scss:css/main.css --style compressed --no-cache
  ```
(resumidamente o comando acima pega o arquivo `main.scss` que contém todos os arquivos de estilo *SASS* e compila um arquivo minificado `main.css` dentro da pasta *CSS*.
6. A qualquer momento, é só digitar `ctrl + c` que o *SASS* para de vigiar a pasta.

No Windows é possível deixar o comando automatizado através de um arquivo `.bat`.
