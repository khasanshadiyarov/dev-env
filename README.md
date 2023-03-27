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
3. Add PATH to binary files. There are binary files for different OS under `/bin` directory, so add PATH according to your OS into `~/.bashrc` file:
- Windows AMD64:
```
export PATH="$PATH:/YOUR_LOCATION/PROJECT_NAME/bin/windows-amd64"
```
- MacOS AMD64:
```
export PATH="$PATH:/YOUR_LOCATION/PROJECT_NAME/bin/macos-amd64"
```
`YOUR_LOCATION` is the location where you cloned the repository, `PROJECT_NAME` is how you named the directory where the project files were cloned. See [installation](#installation).

## Usage
After the environment is set up correctly, source your `~/.bashrc` or reopen the terminal and you will be able to call commands. Commands:

| Command | Description                |
| :------ | :------------------------- |
| fzf     | Command-line fuzzy finder  |
| micro   | Terminal-based text editor |

You can configure your aliases based on the presented tools.
