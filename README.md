# dotfiles

The structure follow the recommendations for [GNU Stow](https://www.gnu.org/software/stow/).

This repository should be cloned into `~`.
If it's cloned to another subfolder the _stow directory_ (`-d <path>/dotfiles`) and 
the _target directory_ (-t `~`) must be specified on every stow command.

To stow a package go to the `dotfiles` folder and execute the following command.

```shell
stow <package>
```

