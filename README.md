# vim + tmux + WSL2

## Setup Windows WSL2:
[Official guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10
)

### Step 1 - Enable the Windows Subsystem for Linux:
Open PowerShell as Administrator and run:
`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux
/all /norestart`

### Step 2 - Update to WSL 2:
To update to WSL 2, you must be running Windows 10.

### Step 3 - Enable Virtual Machine feature:
Open PowerShell as Administrator and run:
`dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all
/norestart`

Restart your machine to complete the WSL install and update to WSL 2.

### Step 4 - Download the Linux kernel update package:
[download](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

### Step 5 - Set WSL 2 as your default version:
Open PowerShell and run this command to set WSL 2 as the default version when
installing a new Linux distribution:
`wsl --set-default-version 2`

### Other WSL commands:
`wsl --set-default-version 2`, `wsl --list --verbose`, `wsl -l -v`, `wsl --shutdown`, `wsl --set-version Ubuntu-20.04 2`

## Setup Linux Distro:

### Update and install all Packages:
`sudo apt update && sudo apt upgrade`

### Install Python3 and pip:
`sudo apt install python3-pip`

### How to install pip on ubuntu 20.04:
[guide](https://linuxize.com/post/how-to-install-pip-on-ubuntu-20.04/)

### Install XDG-utils:
`sudo apt-get install -y xdg-utils`

### Install Git:
`sudo apt install git`

### Install Curl:
`sudo apt install curl`

### Install Zsh:
`sudo apt install zsh`,
`chsh -s $(which zsh)`

### Install Oh-My-Zsh:
`sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

### Install Autosuggestions:
`git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
plugins=(zsh-autosuggestions)`

### Install Zplug:
`curl -sL --proto-redir -all,https https://raw.githubusercontent.com/zplug/installer/master/installer.zsh | zsh
zplug install`

### Install Pure Prompt:
`npm install --global pure-prompt`

### Manually:
`mkdir -p "$HOME/.zsh"`, `git clone https://github.com/sindresorhus/pure.git "$HOME/.zsh/pure"`

### Install Nodejs:
[guide](https://github.com/nodesource/distributions/blob/master/README.md)

### Using Ubuntu:
`curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get install -y nodejs`

### Using Debian:
`curl -sL https://deb.nodesource.com/setup_14.x | bash -
sudo apt-get install -y nodejs`

### Install Gulp:
`sudo npm install --global gulp-cli`

### Install Vifm:
`sudo apt install vifm`

### Install Neovim:
[unstable release](https://launchpad.net/~neovim-ppa/+archive/ubuntu/unstable)

[stable release](https://launchpad.net/~neovim-ppa/+archive/ubuntu/stable)

Install:

`sudo add-apt-repository ppa:neovim-ppa/stable`,

`sudo apt-get update`,

`sudo apt install neovim`

### Remove Neovim:

[remove guide](https://installlion.com/debian/stretch/main/n/neovim/uninstall/index.html)

`sudo apt-get remove --auto-remove neovim`

### Install VimPlug:

`sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'`
       
### Install Win32yank - Clipboard:

`curl -sLo /tmp/win32yank.zip https://github.com/equalsraf/win32yank/releases/download/v0.0.4/win32yank-x64.zip`,

`unzip -p /tmp/win32yank.zip win32yank.exe > /tmp/win32yank.exe`,

`chmod +x /tmp/win32yank.exe`,

`sudo mv /tmp/win32yank.exe /usr/local/bin/`

### Install Tmux:

`sudo apt install tmux`,

Tmux Plugins:
`git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`

Tmux Commands:

source tmux config: `tmux source ~/.tmux.conf`,

install plugins: `prefix + I`,

reload: `prefix + R`
