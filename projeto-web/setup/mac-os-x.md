# Mac OS X

## Como configurar máquinas virtuais com Windows

1. Baixe e instale a [Virtual Box](https://www.virtualbox.org/wiki/Downloads);
2. Após instalar, crie uma nova máquina, clicando em _new_;
3. Nomeie a máquina virutal e selecione a versão do Windows que irá instalar (estamos utilizando a versão 7 de 64bit);
4. Defina 512mb de memória;
5. Crie um novo disco rígido selecionando _create hard drive_;
6. Selecione a opção _VDI (virtualbox disk image)_;
7. Selecione _dinamically allocated_;
8. Selecione um espaço mínimo de 20gb para o drive, caso contrário não será possível instalar os softwares básicos na máquina;
9. Inicie a máquina e aponte o arquivo de instação do Windows (ele está arquivado em _webhost > design > biblioteca > softwares > vm windows_;
10. Escolha a versão do Windows novamente (windows 7 professional) e faça a instalação personalizada, apontando para o drive criado anteriormente;
11. Após a instalação, basta inserir os dados básicos de usuário e rede;
12. Para ativar o Windows, rode na máquina virtual um executável que está dentro do arquivo .dmg de instalação, utilizando uma [pasta compartilhada](#mac1)

=

## <a name="mac1"></a>Como criar uma pasta compartilhada com a Virtual Box

1. Abra a Virtual Box e selecione no menu superior: _devices > insert guest additions_, selecione o .exe indicado e instale com suas configurações básicas;
2. Crie uma pasta no Mac com os arquivos que deseja transferir para a máquina virtual;
3. Volte na Virtual Box, e no menu superior selecione: _devices > share folder settings_;
4. Clique no botão “+”, selecione “Other” e aponte a pasta criada no Mac e seus arquivos ficarão acessíveis também na máquina virtual.
