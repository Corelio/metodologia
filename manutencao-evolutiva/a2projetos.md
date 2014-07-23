# A2Projetos

## 2013.04.a2comunicacao

_As informações sobre este projeto foram migradas para [/projetos/2013.04.a2comunicacao.md](https://github.com/a2comunicacao/metodologia/blob/master/projetos/2013.04.a2comunicacao.md)_

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
