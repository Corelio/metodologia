---
layout: page
title: Clonagem de repositórios GIT na Doors
subtitle: Utilizando o Source Tree, XAMPP e Terminal (MAC)
category: git
---

1. Para clonar, no Source Tree aponte o caminho: www.data@192.168.0.201:/Dados/A2Projetos/nomedoprojeto/www . Aponte para a pasta onde serão instalados os websites, no MAC configurei o XAMPP para apontar para a pasta "Sites" e sempre os nomeio com o mesmo nome da Doors;

2. Para criar o ambiente local, abra a pasta Xampp dentro de Aplicativos: Xampp > etc > extra > httpvhosts.conf e edite o arquivo inserindo o código apontando a pasta onde o site foi instalado (para facilitar, nomeio sempre como local.nomedoprojeto.a2 - pois para ver se tudo está ok na Doors, só retiro o termo local da url): 

	``<VirtualHost 127.0.0.1> 
	ServerName local.pastadoprojetoclonado
	DocumentRoot "/Users/Vivian/Sites/pastadoprojetoclonado" 
	<Directory "/Users/Vivian/Sites/pastadoprojetoclonado"> 
	    Options Indexes FollowSymLinks Includes ExecCGI 
	    AddType text/shtml .shtml 
	    AddOutputFilter INCLUDES .shtml 
	    AllowOverride All 
	    Order allow,deny 
	    Allow from all 
	</Directory> 
	</VirtualHost>``

3. Para terminar de configurar o domínio local, abra o Terminal e digite o comando: 
sudo/applications/textedit.app/contents/macOS/textedit/etc/hosts
Digite sua senha, e insita a url que você vai utilizar entre as linhas "127.0.0.1    localhost" e "255.255.255.255    broadcasthost".

4. Inicie ou reinicie o XAMPP para que funcione. 

5. Se por um acaso mesmo assim aparecer algum outro site no lugar: desligue o XAMPP, abra novamente o Terminal, e limpe o cache da máquina: dscacheutil -flushcache.

6. Reinicie o XAMPP.
