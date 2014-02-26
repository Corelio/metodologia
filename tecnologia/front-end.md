# Front-end

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

Para utilizar o Sass:

1. Crie as pastas *SASS* e *CSS* na raiz do seu projeto;
2. Crie seus arquivos de estilo com a extensão `.scss` dentro da pasta *SASS* (no [repositório do Grid A2](https://github.com/a2comunicacao/Grid-A2/tree/master/sass), deixamos por padrão alguns arquivos iniciais);
3. Ainda dentro da pasta *SASS*, crie um arquivo que vai importar todos os arquivos de estilo (por padrão utilize `main.scss` ou `style.scss`):
Seu arquivo ficaria mais ou menos assim:
```
@import "normalize";
@import "base";
@import "typography";
@import "layout";
```

4. Agora, utilizando o terminal, entramos na pasta do projeto: 
  ```
  cd nomedoprojeto
  ```
5. Dentro da pasta do projeto, precisamos passar um comando para o *SASS* ficar vigiando nossos arquivos e compilá-los em um único arquivo:
```
  sass --watch sass/main.scss:css/main.css --style compressed --no-cache
```
> Resumidamente o comando acima pega o arquivo `main.scss` que contém todos os arquivos de estilo *SASS* e compila um arquivo minificado `main.css` dentro da pasta *CSS*.
> 
6. A qualquer momento, é só digitar `ctrl + c` que o *SASS* para de vigiar a pasta.

Para facilitar, no Windows é possível deixar esse comando automatizado através de um arquivo `.bat` com as instruções.

**Obs.** Fique a vontade para a criação das pastas *SASS* e *CSS*. Sugerimos dessa maneira, por já trabalharmos com essa estrutura de pastas em projetos anteriores.
