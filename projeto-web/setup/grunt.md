# Grunt
Basicamente o Grunt é um automatizador de tarefas. Utilizamos ele para agilizar algumas tarefas comuns no desenvolvimento de um projeto e adotamos o uso dele no [A2boilerplate](https://github.com/a2comunicacao/metodologia/blob/master/a2lab/a2lab.md#a2boilerplate). Pra instalá-lo em sua máquina, você precisa do [NodeJS](http://www.voltsdigital.com.br/labs/gruntjs-por-onde-comecar/) e NPM. Na prática, você instala _plugins_ e configura tarefas que rodarão através de comandos. As tarefas que costumamos utilizar são:

* **_imagemin_**: Reduz tamanho de imagens;
* **_svg2png_**: Converte SVGs em PNGs para utilização em browsers que não tem suporte para SVG;
* **_copy_**: Copia arquivos de uma pasta para outra;
* **_concat_**: Concatena arquivos (utilizamos principalmente para arquivos JS);
* **_uglify_**: Minifica arquivos JS;
* **_jshint_**: Valida arquivos JS;
* **_sass_**: Realiza tarefa do pré-processador SASS;
* ***browser_sync***: Levanta um servidor e sincroniza todos os dispositivos que acessarem determinado IP (ótimo para testes _cross-devide_);
* **_watch_**: Atualiza a página automaticamente conforme arquivos são salvos (funciona em complemento com o plugin [LiveReload](http://livereload.com/)). 
