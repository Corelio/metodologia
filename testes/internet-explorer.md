# Internet Explorer

## Como configurar máquinas virtuais para testar no Internet Explorer?

### Instalando máquina virtual no MAC

1. Baixe e instale a [Virtual Box](https://www.virtualbox.org/wiki/Downloads);
2. Após instalar, crie uma nova máquina, clicando em _new_;
3. Nomeie a máquina virtual e selecione a versão do Windows que você vai instalar (estamos utilizando a versão 7 de 64bit);
4. Defina 512mb de memória;
5. Crie um novo disco rígido selecionando _create hard drive_;
6. Selecione a opção _VDI (virtual box)_;
7. Selecione _dinamically allocated_;
8. Selecione um espaço mínimo de 20gb para o drive, caso contrário não será possível instalar os softwares básicos na máquina virtual;
9. Inicie a máquina e aponte o arquivo de instalação do Windows (ele está arquivado em _webhost_ > _design_ > _biblioteca_ > _softwares_ > _vm windows_);
10. Escolha a versão do Windows novamente (windows 7 professional) e faça a instalação personalizada, apontando para o drive criado anteriormente;
11. Após a instalação, basta inserir os dados básicos de usuário e rede;
12. Para ativar o windows, rode na máquina virtual um executável que está dentro do arquivo .dmg de instalação utilizando uma [pasta compartilhada](https://github.com/a2comunicacao/metodologia/blob/master/tecnologia/maquina-virtual.md#como-criar-uma-pasta-compartilhada-com-a-virtual-box-no-mac).

