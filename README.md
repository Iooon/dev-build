# Development build

Ansible scripts to build my development setup.
The build contains the following tasks:
- Update the system
- Download [dotfiles](https://github.com/Iooon/dotfiles.git) from Github
- Download neovim from Github, build neovim and install it
- Install tmux with apt
- Link tmux and neovim config files from dotfiles to system

## Target systems

Ubuntu/Debian


# Instructions

- Be on Debian/Ubuntu
- Install ansible (``python3 -m pip install ansible`` or ``sudo apt install ansible``)
- Clone and change into this respository (``git clone https://github.com/Iooon/dev-build.git && cd dev-build``)
- Make sure you have sudo token (``sudo test``)
- Execute ansible (``ansible-playbook main.yml``)

## Variables

Variables like clone paths can be changed in the [defaults](/roles/dev-setup/defaults/main.yml) file.
The overwrite variables are set so that existing config files are not overwritten and execution of ansible stops.
If the script should overwrite exisiting config files set the repective variable to true.

