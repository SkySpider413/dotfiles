# dotfiles
dtt

change /etc/nixos/configuration.nix bootloader config to here
set your timezone in configuration.nix (this, not /etc)
change user stuff

backup existing config
```console
sudo mv /etc/nixos/configuration.nix /etc/nixos/configuration.nix.bak
```
create symlinks
```console
sudo ln -s ~/dotfiles/configuration.nix /etc/nixos/configuration.nix
```

create i3 config
```console
mkdir ~/.config ~/.config/i3 ~/.config/i3status
ln -s ~/dotfiles/i3config ~/.config/i3/config
ln -s ~/dotfiles/i3statusconfig ~/.config/i3status/config
ls -la /etc/nixos/
ls -la ~/.config/i3/
ls -la ~/.config/i3status/
sudo nixos-rebuild switch
sudo reboot

mkdir -p ~/.local/share/fonts
mv <path_of_extracted_fonts> ~/.local/share/fonts/
fc-cache -vf ~/.local/share/fonts/
```
