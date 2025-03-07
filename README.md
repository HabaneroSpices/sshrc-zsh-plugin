# sshrc-zsh-plugin

Better host completion for **sshrc** in Zsh.

[![asciicast](https://asciinema.org/a/381405.svg)](https://asciinema.org/a/381405)

- [sshrc-zsh-plugin](#sshrc-zsh-plugin)
    - [Installation](#installation)
        - [Zinit](#zinit)
        - [Antigen](#antigen)
        - [Oh My Zsh](#oh-my-zsh)
        - [Sheldon](#sheldon)
        - [Manual (Git Clone)](#manual-git-clone)
    - [Usage](#usage)
        - [SSH Config Example](#ssh-config-example)

## Installation

Make sure you have [fzf](https://github.com/junegunn/fzf) installed.

### Zinit

```shell
zinit light habanerospices/sshrc-zsh-plugin
```

### Antigen

```shell
antigen bundle habanerospices/sshrc-zsh-plugin
```

### Oh My Zsh

1. Clone this repository into `$ZSH_CUSTOM/plugins` (by default `~/.oh-my-zsh/custom/plugins`)

    ```shell
    git clone https://github.com/habanerospices/sshrc-zsh-plugin ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/sshrc
    ```

2. Add the plugin to the list of plugins for Oh My Zsh to load (inside `~/.zshrc`):

    ```shell
    plugins=(sshrc ...)
    ```

3. Start a new terminal session.

### Sheldon

1. Add this config to `~/.config/sheldon/plugins.toml`

    ```toml
    [plugins.sshrc]
    github = 'habanerospices/sshrc-zsh-plugin'
    ```

2. Run `sheldon lock` to install the plugin.

3. Start a new terminal session.

### Manual (Git Clone)

1. Clone this repository somewhere on your machine. For example: `~/.zsh/sshrc`.

    ```shell
    git clone https://github.com/habanerospices/sshrc-zsh-plugin ~/.zsh/sshrc
    ```

2. Add the following to your `.zshrc`:

    ```shell
    source ~/.zsh/sshrc/sshrc.zsh
    ```

3. Start a new terminal session.

## Usage

Just press <kbd>Tab</kbd> after `sshrc` command as usual.

### SSH Config Example

You can use `#_Desc` to set description.

~/.ssh/config

```text
Host Bastion-Host
    Hostname 1.1.1.1
    User sunlei

Host Development-Host
    Hostname 2.2.2.2
    IdentityFile ~/.ssh/development-host
    #_Desc For Development
```
