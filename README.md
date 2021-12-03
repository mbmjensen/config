# Config

A home for my config files. These config files can be installed on their own, but it is probably more useful to bring these in as a submodule of my development environment.

## Requirements

```
macOS >= 12.0.1
```

## Installation Instructions

1. Clone this repo into the location of your choice, e.g.
   ```zsh
   git clone https://github.com/mbmjensen/config ~/Development
   ```

2. Initialize and recursively clone all submodules that make up the config files
   ```zsh
   git submodule update --init --recursive
   ```

3. Symlink the config directory to the home directory. Even though most programs respect $XDG_CONFIG_HOME, some, such as tmux, expect the config directory to be in the user home directory.
   ```zsh
   ln -s "${HOME}/Development/config" "${HOME}/.config`
   ```
