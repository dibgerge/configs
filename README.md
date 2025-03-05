# My arch setup


1. Install arch linux following the [wiki](https://wiki.archlinux.org/title/Installation_guide)
1. After reboot, create a [new user](https://wiki.archlinux.org/title/General_recommendations#:~:text=administration%20for%20more.-,Users%20and%20groups,-A%20new%20installation)
   1. Add user to sudoer list using the command: `sudo visudo`. See details [here](https://wiki.archlinux.org/title/Sudo#Sudoers_default_file_permissions:~:text=a%20specific%20user.-,Using%20visudo,-The%20configuration%20file).
1. Install [Hyperland windows manager](https://wiki.hyprland.org/Getting-Started/Installation/)
1. Install [Kitty terminal emulator](https://sw.kovidgoyal.net/kitty/)
1. Install [mylinuxforwork](https://wiki.archlinux.org/title/Sudo#Sudoers_default_file_permissions:~:text=a%20specific%20user.-,Using%20visudo,-The%20configuration%20file) configuration files used to customize Hyprland.
   1. During ML4W install, you will be asked to install SDDM for login management, which should be accepted.
   2. Make sure that `zsh` is the default shell
1. Install `yay` AUR package manager:
      ```
      sudo pacman -S base-devel git
      git clone https://aur.archlinux.org/yay-bin.git
      cd yay-bin
      makepkg -si
      ```
1. Install [dropbox](https://wiki.archlinux.org/title/Dropbox): `yay -S dropbox nautilus-dropbox`
2. Install zotero: `yay -S zotero`, and setup sync directories within dropbox
3. Install windsurf ide: `yay -S windsurf`
4. Install chrome: `yay -S google-chrome`. Then, change default browser in ML4W to run `google-chrome-stable`
5. Install [mamba](https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html) for python package management.
   1. Do not accept to add mamba init to your shell. After install run `mamba init zsh` so that it will update `zsh` install of the default `bash`.
 

## Setup zsh

1. Install [oh-my-z](https://github.com/ohmyzsh/ohmyzsh)

## Setup theme
Install the [power10k theme](https://github.com/romkatv/powerlevel10k). Copy the file .p10k.zsh into home directory to have appropriate colors.

## Tmux 

Instal TPM package manager and Nord-theme https://www.nordtheme.com/docs/ports/tmux/installation
