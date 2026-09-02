# dotfiles

The structure follow the recommendations for [GNU Stow](https://www.gnu.org/software/stow/).

This repository should be cloned into `~`.
If it's cloned to another subfolder the _stow directory_ (`-d <path>/dotfiles`) and 
the _target directory_ (-t `~`) must be specified on every stow command.

## Terminology

```
~                                                     ~                    <-- target directory
|-- dotfiles                 <-- stow directory       |-- .config
    |-- starship             <-- package directory        |-- starship.toml
        |-- .config
            |-- starship.toml
```

## Add a new application to Stow

1. Creating the package directory and the structure in the stow directory
2. Move the files to the package directory
3. Create the symlinks with stow

eg. Ghostty

```shell
mkdir -p ~/dotfiles/ghostty/.config/ghostty
mv ~/.config/ghostty/config.ghostty ~/dofiles/ghostty/.config/ghostty/
cd ~/dotfiles && stow ghostty

```

## Link files from Stow to `.config`

To stow a package go to the `dotfiles` folder and execute `stow <package>`.

eg. Ghostty

```shell
cd ~/dotfiles && stow ghostty
```

