# Config

A home for my config files. These config files can be installed on their own, but it is probably more useful to bring these in as a submodule of my development environment.

## Requirements

```
macOS >= 13.0.1
```

## Installation Instructions

1. Clone this repo into the [development directory specified in the .zshenv file](https://github.com/mbmjensen/zsh/blob/0ea51c4d6728dfb51f7c29785494d27717c6ebd9/.zshenv#L20).
   ```zsh
   git clone https://github.com/mbmjensen/config ~/Development
   ```

2. Initialize and recursively clone all submodules that make up the config files
   ```zsh
   git submodule update --init --recursive
   ```

3. Symlink the config directory to the home directory. Even though most programs respect $XDG_CONFIG_HOME, some, such as tmux, expect the config directory to be in the user home directory.
   ```zsh
   ln -s "$HOME/Development/config" "$HOME/.config`
   ```

4. Copy or symlink the zshenv file into the home directory
    ```zsh
    ln -s "$HOME/Development/config/zsh/.zshenv" "$HOME/.zshenv"
    ```
