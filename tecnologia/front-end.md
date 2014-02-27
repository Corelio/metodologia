# Front-end

## Grunt

Basicamente o Grunt é um automatizador de tarefas. Utilizamos ele pra agilizar algumas tarefas comuns no desenvolvimento de um projeto e adotamos o uso dele no [A2boilerplate](https://github.com/a2comunicacao/metodologia/blob/master/a2lab/a2lab.md#a2boilerplate). Pra instalá-lo em sua máquina você precisa de [NodeJS](http://www.voltsdigital.com.br/labs/gruntjs-por-onde-comecar/) e NPM. Na prática, você instala _plugins_ e configura tarefas que rodarão através de comandos. As tarefas que costumamos utilizar são:
* _imagemin_: Reduz tamanho das imagens.
* _svg2png_: Converte SVGs em PNGs para utilização em browsers que não tem suporte para SVG.
* _copy_: Copia arquivos de uma pasta para outra.
* _concat_: Concatena arquivos (utilizamos principalmente para arquivos JS).
* _uglify_: Minifica arquivos JS.
* _jshint_: Valida arquivos JS.
* _sass_: Realiza tarefa do pré-processador SASS.
* *browser_sync*: Levanta um servidor e sincroniza todos dispositivos que acessarem determinado IP (ótimo para testes _cross-device_).
* _watch_: Atualiza a página automaticamente conforme arquivos são salvos (funciona em complemento com o plugin [LiveReload](http://livereload.com/)).


## Adobe Edge Inspect

1. Primeiro precisamos fazer o [download](https://creative.adobe.com/inspect) do aplicativo do Edge Inspect. É necessário ter/criar uma conta na Creative Cloud.
2. Depois é necessário fazermos o [download](https://chrome.google.com/webstore/detail/adobe-edge-inspect/ijoeapleklopieoejahbpdnhkjjgddem) da extensão para o Google Chrome.
3. Agora, precisamos escolher os dispositivos que vamos sincronizar com o PC e, fazer o download da app para a plataforma [Android](https://play.google.com/store/apps/details?id=com.adobe.shadow.android&hl=pt_BR) ou [IOS](https://itunes.apple.com/br/app/adobe-edge-inspect/id498621426?mt=8).
4. Feito isso, executamos o aplicativo da Adobe Edge Inspect no PC. Provavelmente será necessário logarmos com a nossa conta da Creative Cloud.
5. Agora precisamos abrir a extensão do Chrome que instalamos e ativá-la, clicando em um botão no canto superior direito.
6. O próximo passo é abrir o aplicativo no dispositivo que queremos sincronizar. Ao abrir, precisamos *Adicionar uma conexão*, clicando no ícone de **+** no canto superior direito e, inserir o *IP* do PC.
7. Após inserirmos o *IP*, um código será gerado na app. Devemos inseri-lo na extensão do Google Chrome que provavelmente irá abrir automaticamente.
8. Pronto! Tente acessar uma outra URL e automaticamente o dispositivo que sincronizamos com o PC irá atualizar automaticamente.

> A versão gratuita permite apenas a conexão de um dispositivo.

## Disqus

### Instalação

1. Criar uma conta para poder usar o serviço: [Criar a conta](https://disqus.com/profile/signup/)
2. Logar e clicar em [Dashboard](http://disqus.com/dashboard/)
3. Em **_Your Sites_** clicar em [Add](https://disqus.com/admin/signup/) para adicionar o site que vai receber o plugin

### Wordpress

1. No painel esquerdo do seu administrador Wordpress, selecione **Plugins > Adicionar Novo**
2. Procure por "Disqus Comment System"
3. Selecione **Instalar Agora > Ativar Plugin**
3. Clique em **Configure** e logue com usuário e senha que você criou
4. Selecione o site que você configurou no Disqus

**Obs:** Se já existir comentários nos posts e você quiser exporta-los para o disqus, clique em **Plugin Settings** no canto superior direito da tela, role a tela até "Import and Export" e clique em **Export Comments**.

### Universal Code

1. Clique em **Dashboard**
2. Em _**Your Sites**_ clique no site que você criou
3. Clique em **Settings** > **Install** > **Universal Code**
4. E siga os procedimentos informados

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
