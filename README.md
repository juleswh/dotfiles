# juleswh dotfiles

These files are supposed to be installed by GNU Stow. For example, if you want to install the dotfiles for `kitty` listed in this directory, then clone this repository to your `$HOME`, and then run

```shell
stow kitty
```

which will automatially create all the symlinks needed.

All subdirectories (except fonts) in this repository are structured with the assumption that you are going to put the repository directly in `$HOME`. If not, you need to change the command for stow accordingly.

## Other configuration

### SSH Agent et gnome keyring

Si utilisation de XFCE4 :

- désactiver l'agent SSH (pas sûr que ce soit nécessaire) :
	```shell
	xfconf-query -c xfce4-session -p /startup/ssh-agent/enabled -n -t bool -s false
	xfconf-query -c xfce4-session -p /startup/gpg-agent/enabled -n -t bool -s false
	```
- activer les services gnomes dans `Session et démarrage` > `Avancé` ou avec :
	```shell
	xfconf-query -c xfce4-session -p /compat/LaunchGNOME -n -t bool -s true
	```

Il peut être nécessaire d'aller configurer la clé dans `seahorse` (GUI) (?)
