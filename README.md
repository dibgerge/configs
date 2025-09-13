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
  

## Gvim

vim does not have gtk support, and need to replace is with `gvim`: `sudo pacman -S gvim`. This allows for copy/paste from the system registers (`"+p`/`"+yy`)
 

## Setup zsh

ML4W uses `oh-my-zsh` and `oh-my-posh` by default. The `power10k_theme` is going out of maintenance, but I used the `oh-my-posh` implementatioin of it.

1. Copy the file `~/.config/zshrc/20-customization` to `~/.config/zshrc/custom/20-customization`
2. Copy the file `powerlevel10k_rainbow.toml` to the `~/.config/ohmyposh/` directory. This file is slightly modified version of the theme to add conda environment info.
4. Change the `oh-my-posh` init command to the following:
   `eval "$(oh-my-posh init zsh --config $HOME/.config/ohmyposh/powerlevel10k_rainbow.toml)"`

## Waybar theme

This is the top bar which comes with Hyprland and in particular ML4W theme. The waybar has its own theme, and the given theme config customize it to look nicer (to my taste) than the built in themes that come with ML4W. To use it, copy the folder `waybar/themes/colorful` to the location `~/.config/waybar/themes` on local machine. 


## Tmux 

Instal TPM package manager and Nord-theme https://www.nordtheme.com/docs/ports/tmux/installation
