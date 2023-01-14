# ansible mac os setup

This will do most of the setup for a new mac.
There are a few things still left to be done manually however.

## Usage

```sh
ansible-galaxy install -r requirements.yml
ansible-playbook playbook.yml --ask-become-pass
```

There are a few possible tags that can be used to only run specific parts:

| tag      | description                        |
| -------- | ---------------------------------- |
| homebrew | install homebrew packages          |
| dock     | rearrange dock icons               |
| zsh      | install oh-my-zsh and customize it |
| dotfiles | copy dotfiles to .config           |
| iterm2   | configure iterm2                   |
| vscode   | configure vscode                   |
| npm      | install a few global npm packages  |

Add `-t tag1,tag2` to specify tags.


## Manual steps afterwards

These things are fairly obvious but here's a list nevertheless.
A lot of things will probably be missing as these things are easy to overlook.

- sign in to chrome, spotify, slack, ...
- install keymap (ukulele)
- install photoshop, etc.
- install xcode if needed
- configure menu bar and hiddenbar
- configure raycast
- configure openvpn profiles (tunnelblick)
- set up things which need api keys (.npmrc, mamba/quetz, ...)
- create a `$HOME/desktop/projects` folder
- configure ssh and create/distribute keys
- start all of the programs at least once to set permissions, auto-start, etc.
