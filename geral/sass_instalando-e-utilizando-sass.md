---
layout: page
title: SASS - Instalando e utilizando o SASS 
subtitle: Utilizando o Terminal (MAC)
category: sass
---

Como por padrão os MAC's já vem com o Ruby instalado, basta que instalemos o Sass (que é uma "biblioteca" do Ruby):

1. No terminal digite: `sudo gem install sass`

_Obs.: No meu caso, como não estou usando a última versão do sistema operacional, ele me apontou um erro de atualização de versão, e pediu que eu rodasse o seguinte comando:  `gem install --version '~> 0.9.1' rb-fsevent`_

Para utilizar o Sass:

1. Crie as pastas sass e css no seu projeto;
2. Crie os arquivos principais de .scss (na pasta sass) e .css (na pasta css)
3. No terminal, precisamos dizer pra ele entrar nessa pasta para "olhar os arquivos", então digite:  cd /caminhocompletodoprojeto (para copiar todo o caminho da pasta, basta que você copie a pasta pra dentro do terminal, e ele faz todo o caminho pra você, no meu caso, fica assim: cd /Users/vivian/Sites/pastadoprojeto
4. Agora eu preciso "falar" pro Sass, que todas as alterações que eu fizer no arquivo .scss, que ele mande para o arquivo .css, este comando se chama watch, e que seja feito de forma minificada e que não fique guardando cache (ele cria uns arquivos estranhos de cache dentro da pasta), pra isso digite no terminal: sass --watch sass/main.scss:css/main.css --style compreesed --no-cache. 
Traduzindo: Sass, fique de olhos nas alterações que eu fizer na pasta sass e o no meu arquivo principal .scss e transforme ele no arquivo .css que esta na pasta css, faça isso de modo que ele fique compressado e não guarde cache dos arquivos.
5. Para que ele pare de "olhar" pasta digitar ctrl + c.
6. Para trocar de projeto, saia da pasta digitando: cd ../ e entre em outro projeto voltando ao passo 2.

_Obs.: Existe uma forma simplificada de rodar esses comandos mas é preciso criar um arquivo numa extensão diferenciada e, não consegui fazer no meu. A Sandra pode ajudar nesse caso, pois ela conseguiu fazer de uma outra maneira._
 
No Windows o arquito tem uma extensão que não funciona nos MAC's.
