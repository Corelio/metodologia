# A2Projetos

## 2013.04.a2comunicacao

* URL: http://a2comunicacao.com.br/
* CMS: A2siteBox - http://a2comunicacao.com.br/a2sitebox/login/
* Hospedagem: Hostgator - https://financeiro.hostgator.com.br/
* <a name="projetos1"></a>Repositório GIT: `www-data@192.168.0.241:/Dados/A2Projetos/2013.04.a2comunicacao/www`
* FTP:
	* a2comunicacao.com.br;
	* Login: `a2com691`;
	* Senha: `p60vbK62gV`.
* Dependências:
	* Composer (deve ser instalado na pasta do projeto);
	* [Grunt](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/setup/grunt.md#grunt) (deve ser instalado na pasta do tema).

### Configurando o projeto

1. Atualize/baixe o projeto para sua máquina usando o [GIT](#projetos1)
2. Baixe a pasta _/web/uploads_ do servidor, via FTP (ela não vem com o projeto)
3. Instale o Composer na pasta raiz do projeto via terminal: `php composer.phar install`
4. Instale o Grunt na pasta do tema _/web/themes/site_ via terminal: `npm install`

### Atualizações no código CSS/JS <a name="atualiza-css"></a>

1. Rode o Grunt na pasta do tema e execute o comando via terminal: `cd caminho-ate-a-pasta`; tecle _Enter_ e `grunt w`
2. Faça as modificações necessárias (o arquivo minificado deve ser gerado automaticamente via Grunt);
3. Suba os arquivos via FTP:
	* **Se forem alterações de CSS**: Além dos arquivos modificados, suba o _style.css_ (em _/web/themes/site/css_);
	* **Se forem alterações de JS**: Além dos arquivos modificados, suba a basta _build_ (_/web/themes/site/js/build_). Essa pasta não vem com o projeto, é gerada automaticamente via Grunt;
	* **Se forem alterações em templates**: Simplesmente suba os arquivos modificados.

Obs.: O site da A2 Comunicação tem cache ativado, após subir é preciso limpá-lo (instruções abaixo).

### Limpando o cache no servidor

1. Acesse o FTP do site via terminal: `ssh [user-ftp]@a2comunicacao.com.br -p2222` (onde 2222 é o número da porta);
2. Resposta (só no 1º acesso): Are you sure you want to continue connecting (yes/no)? Yes;
3. Entre com a password (do FTP);
4. Acesse: cd public_html;
5. Entre com a instrução de limpeza: `rm -rf app/cache/*`.

### Atualizações da seção Quem somos

#### Área: Equipe

1. Salve a imagem original com o nome padronizado (nome_sobrenome.jpg) na pasta do projeto, no servidor Design: _2013.04.a2comuniacacao/design/imagens/Fotos novas da A2/Fotos da Equipe_;
2. Trate a imagem:
	* Abra o arquivo com as imagens tratadas _todos.psd_ (na mesma pasta onde a imagem foi salva) e inclua a nova imagem;
	* Faça as modificações necessárias, de modo que a nova imagem fique com o aspecto semelhante às demais: com o fundo branco e leve “luz” alaranjada;
	* Salve a imagem final no tamanho 120x120 pixels, dentro da pasta (120x120_tratadas) com o nome padronizado.
3. Copie a imagem para a pasta do projeto _/themes/site/img/equipe_;
4. Edite o template _/2013.04.a2comunicacao/app/Resources/SiteBundle/views/Templates/quem-somos.html.twig_:
	* Duplique o bloco `<div class=”thumb”>`. Importante: repare que há um limite máximo de 6 membros por linha. Caso precise de uma nova linha, basta acrescentar `<div class=”linha-thumb”></div>` após a última linha e então incluir o bloco na nova linha;
	* Altere o nome, texto do curriculum, o caminho da imagem e salve o arquivo.
5. Suba a imagem e o template para o servidor, via FTP;
6. Execute a limpeza do cache e verifique a atualização no browser.

## 2013.07.intranetemtu

* URL: http://200.144.29.93:8080 (user: willianc; pass: a2comunica)
* CMS: A2siteBox - http://200.144.29.93:8080/a2sitebox/login (user: admin; senha: a2@345box)
* Hospedagem: Servidor interno da EMTU
* <a name="projetos1"></a>Repositório GIT: `www-data@192.168.0.241:/Dados/A2Projetos/2013.07.intranetemtu/www`
* FTP: não temos acesso; são gerados [pacotes de atualização](#pacote-atualizacao) e enviados à equipe de TI da EMTU
* Dependências:
	* Composer (deve ser instalado na pasta do projeto);
	* [Grunt](https://github.com/a2comunicacao/metodologia/blob/master/projeto-web/setup/grunt.md#grunt) (deve ser instalado na pasta do tema).

### Configurando o projeto

1. Atualize/baixe o projeto para sua máquina usando o GIT
2. Instale o Composer na pasta raiz do projeto via terminal: `php composer.phar install`
3. Instale o Grunt na pasta do tema _/web/themes/intranet_ via terminal: `npm install`

### Atualizações no código CSS/JS
Veja os passos para [atualização](#atualiza-css).

OBS.: O controle de _cache_ é feito pelos responsáveis pelo servidor (EMTU)

### Gerando pacote de atualização <a name="pacote-atualizacao"></a>

1. Envie as alterações para o GIT
2. No terminal, digite `git diff HEAD 'HEAD~1' --name-only`  para listar os arquivos que serão incluídos no pacote
3. Digite ``tar czfv nome-do-arquivo.tar.gz 'git diff HEAD 'HEAD~1' --name-only'``  para gerar o arquivo .tar.gz
