# Tutorial-de-Instala-o-Ferramentas-Synopsys
Este tutorial baseia-se na trilha design verification da Synopsys, podendo ser aplicado nas demais trilhas desde que de acordo com as ferramentas disponibilizadas.
# Ferramentas Synopsys Trilha Design Verification

# André Felipe
-------------------------
1. Instalação da distribuição Linux

Para inciar a distribuição Linux desta seção, você deve ter instalado o wsl, caso tenha feito
pode prosseguir dentro do wsl com o seguinte comando: 

```bash
https://mirror.stream.centos.org/SIGs/10-stream/altimages/images/wsl/x86_64/CentOS-Stream-Image-WSL-Base.x86_64-10-202604020202.wsl
```
Esta instalação do CentOs é uma das distribuições que suportam a ferramenta Verd e VCS que serão utilizadas nas atividades. Caso
haja difiuldade para essa instalação específica consultar o manual de instalação e as distribuições disponíveis da ferramenta dentro 
da Synopsys.

2. Instalar a imagem:

   ```bash
wsl --install --from-file 'C:\Users\55929\Downloads\CentOS-Stream-Image-WSL-Base.x86_64-10-202604020202.wsl' --name CS10
```
3. Após as instalações:

 ```bash
wsl ~ -d CS10
```

Isso permite entrar dentro da distribuição instalada anteriormente.

4. Instação de depêndencias:

A uma necessidade de instalar dependências para a distribuição, que permitem o acesso correto e
a adequação do sistema. Basta utilizar o comando abaixo:

```bash
sudo dnf install -y tcsh ksh glibc libstdc++ zlib libX11 libXext libXft libXtst libXi libXrender mesa-libGL mesa-libGLU freeglut xorg-x11-fonts-Type1 xorg-x11-fonts-misc perl libXScrnSaver net-tools libnsl libXrandr libSM nss libXcomposite libXdamage alsa-lib
```
Após essas instalações podemos prosseguir para baixar os sarquivos da Synopsys.

5. Para não ter problemas com o download falhando, use o SFTP:

   ```bash
   Por exemplo: sftp andresouza@eft.synopsys.com
   ```

   Posteriormente irá pedir sua senha, está é a que você utiliza para entrar na Synopsys.

 6. Depois no prompt do sftp, entre com os seguintes comandos:


```bash
cd site58898
cd MyProducts
cd rev/verdi_vY-2026.03
Enter "ls" or "dir" to see the list of product files
get *
Enter "quit" to log off the server
   ```
A informação do site "58898" consta nas informações coletadas pela synopsys, se duvida consultar dentro do seu acesso na 
plataforma.
Obs.: Você pode verificar todas as versões das ferramentas dentro da pasta rev.

Após isso temos o instalador.



