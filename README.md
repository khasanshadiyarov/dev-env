# Development environment
This is my personal pre-configured development environment, which is based on [Micro](https://micro-editor.github.io/) text editor, [fzf](https://github.com/junegunn/fzf).

## Contents
- [Introduction](#development-environment)
- [Installation](#installation)
- [Usage](#usage)

---

## Installation
Installation process is quite simple, all configuration and binary files are ready to be used. Follow next steps to setup the environment:
1. Clone the repository to not temp location. The project directory will be used as binary files source location:
```
cd YOUR_LOCATION

git clone https://github.com/khasanshadiyarov/dev-env.git PROJECT_NAME
```
2. Copy all directories from `/.config` to `~/.config` directory. Some tools (e.g. Micro) is pre-configured within the environment:
```
cp -r .config/* ~/.config/
```
3. Add PATH to binary files. There are binary files for different OS under `/bin` directory, so add PATH according to your OS into `~/.bash_profile` file:
- Windows AMD64:
```
export PATH="$PATH:/YOUR_LOCATION/PROJECT_NAME/bin/windows-amd64"
```
- MacOS AMD64:
```
export PATH="$PATH:/YOUR_LOCATION/PROJECT_NAME/bin/macos-amd64"
```
`YOUR_LOCATION` is the location where you cloned the repository, `PROJECT_NAME` is how you named the directory where the project files were cloned. See [installation](#installation).

### MacOS
On MacOS configured key bindings require some adjustments in the System Settings, because some of key bindings are already taken by the MacOS itself. Follow the next step:
1. Go to `System Settings > Keyboard > Keyboard Shortcuts > Mission Control`;
2. Uncheck `Mission Control`, `Application Windows`, `Mission Control > Move left a space` and `Mission Control > Move right a space`.
P.s. If you need these MacOS key bindings, reconfigure Micro text editor `bindings.json` for actions, which are bind to `Ctrl-Right/Left/Up/Down`.

## Usage
After the environment is set up correctly, source your `~/.bash_profile` or reopen the terminal and you will be able to call commands. Commands:
| Command | Description                |
| :------ | :------------------------- |
| fzf     | Command-line fuzzy finder  |
| micro   | Terminal-based text editor |
You can configure your aliases based on the presented tools.

### Key bindings
Before using the environment, please take a look at Micro text editor configured [`bindings.json`](.config/micro/bindings.json) and after you understand it, you are ready to start using the environment.
