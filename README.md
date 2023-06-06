# debian
Arquivos de configuraçao e instalacoes feitas no Debian 11/12.

Inserir o usuário wwagner no .sudoer.

```sh
sudo apt install build-essental net-tools git wget curl linux-headers-$(uname -r) manpages-dev
```
Instalação do AASDF seguindo o passo a passo presente no endereço [https://asdf-vm.com/pt-br/guide/getting-started.html#_2-download-asdf](https://asdf-vm.com/pt-br/guide/getting-started.html#_2-download-asdf).

```sh
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.11.3

```
Inserir no arquivo .bashrc as linhas:

```sh
. "$HOME/.asdf/asdf.sh"
. "$HOME/.asdf/completions/asdf.bash"
```

Trocar todo o conteúdo do arquivo /etc/apt/sources.list por:

```sh
# deb cdrom:[Official Debian GNU/Linux Live 11.7.0 gnome 2023-04-29>

# deb cdrom:[Official Debian GNU/Linux Live 11.7.0 gnome 2023-04-29>

deb http://debian.pop-sc.rnp.br/debian/ bookworm main contrib non-f>
deb-src http://debian.pop-sc.rnp.br/debian/ bookworm main contrib n>

deb http://security.debian.org/debian-security bookworm-security ma>
deb-src http://security.debian.org/debian-security bookworm-securit>

# bookworm-updates, to get updates before a point release is made;
# see https://www.debian.org/doc/manuals/debian-reference/ch02.en.h>
deb http://debian.pop-sc.rnp.br/debian/ bookworm-updates main contr>
deb-src http://debian.pop-sc.rnp.br/debian/ bookworm-updates main c>

# This system was installed using small removable media
# (e.g. netinst, live or single CD). The matching "deb cdrom"
# entries were disabled at the end of the installation process.
# For information about how to configure apt package sources,
# see the sources.list(5) manual.
deb http://debian.pop-sc.rnp.br/debian/ bookworm-proposed-updates n>

deb https://fasttrack.debian.net/debian-fasttrack/ bookworm-fasttra>
deb https://fasttrack.debian.net/debian-fasttrack/ bookworm-backpor>
deb http://deb.debian.org/debian/ sid main contrib non-free
``` 
Atualizar os arquivos instalados e a distribuição Debian 11 para 12.

```sh
sudo apt update
sudo apt upgrade
sudo apt dist-upgrade
``` 

Instalação do Snap e o Snap Store.


```sh
sudo apt install snapd
sudo snap install core
sudo snap install snap-store
``` 
Instalação do Visual Studio Code.


```sh
sudo snap install --classic code
```

