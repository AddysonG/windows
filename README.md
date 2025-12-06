# My Windows Setup

This repository is mainly for me to keep track of various installation and setup steps + configuration for when I need Windows, both for general productivity and development. It also contains miscellaneous config files I use for Windows that don't fit into any other repos.

## Prerequisites

- Install JetBrainsMono Nerd Font from [the Nerd Fonts website](https://www.nerdfonts.com/font-downloads). This is the standard font I use for most configs.
- Make sure Windows Terminal and WinGet are installed.

## Contents

1. [System Settings](#system-settings)
    - [Windows 11 Settings](#windows-11-settings)
    - [Control Panel](#control-panel)
    - [PowerToys](#powertoys)
2. [Window Manager (GlazeWM)](#window-manager-glazewm)
3. [Terminal Workflow](#terminal-workflow)
    - [Git Bash](#git-bash)
    - [Windows Terminal](#windows-terminal)
4. [Text Editors](#text-editors)
    - [Vim](#vim)
    - [Neovim](#neovim)
    - [VSCode](#vscode)

---

## System Settings

This section covers changes to be made in Windows 11 Settings, Control Panel, and PowerToys.

### Windows 11 Settings

*Nothing here for now...*

### Control Panel

- Change key repeat settings and change/disable cursor blinking under *Keyboard*, which should open a new window.

### PowerToys

- Before anything else, install PowerToys.
- Set PowerToys to always run as admin (must be opened as admin to change this setting). Otherwise key rebinds may not work in some applications.
- Change keyboard *Activation shortcut* to `Alt+R` for PowerToys Run.

#### Keymaps

- Remap keys in *Input & Output > Keyboard Manager*.
- Remap `Caps Lock` to `Esc`
- To rebind the Copilot key, rebind the shortcut `Win(Left)+Shift(Left)+F23` to, depending on the kind of keyboard:
    - `Apps/Menu`
    - `Ctrl(Left)`

---

## Window Manager (GlazeWM)

1. Install GlazeWM through WinGet: `winget install GlazeWM`.
2. Git clone [my GlazeWM config](https://github.com/AddysonG/.glzr) into `~/.glzr/`. After this, open GlazeWM should always start with the custom top bar.
3. To make closing GlazeWM easier, in Windows 11 Settings, turn on GlazeWM in the system tray.
    - Found in: *Personalization > Taskbar > Other system tray icons*

---

## Terminal Workflow

This section covers setting up Git Bash and Windows terminal.

### Git Bash

1. Install Git for Windows through the [website](https://gitforwindows.org).
    - During installation, check the option to add a Windows Terminal profile.
    - It doesn't look like the WinGet package goes through setup options, which is why I'm using the GUI installer.
2. Copy `.bashrc` into `~/` for some changes to the prompt appearance and adding any installed GnuWin32 tools to PATH.
3. Copy `.inputrc` into `~/` to remove the annoying visual bell in Git Bash.

### Windows Terminal

1. Copy `settings.json` into `~/AppData/Local/Packages/Microsoft.WindowsTerminal_8wekyb3d8bbwe/LocalState/settings.json`.


---

## Editors

### Vim

1. Install Vim through WinGet: `winget install vim.vim`.

***TODO (my general dotfiles are not public, so figuring out what to do for `.vimrc`)***

### Neovim

My Neovim config requires several dependencies for the main plugins to work.

1. Install the following dependencies:
    - Install MSCV Build Tools: [this link](https://visualstudio.microsoft.com/downloads/) at the bottom of the page. If Visual Studio is already installed, this is not necessary. Certain workloads might also need to be included for the installation.
    - Install Git Bash using instructions earlier, if not installed already.
    - Install WinLibs for `gcc` through WinGet: `winget install BrechtSanders.WinLibs.MCF.UCRT`.
    - Install ripgrep through WinGet: `winget install BurntSushi.ripgrep.MSVC`.
2. Install Neovim through WinGet: `winget install Neovim.Neovim`.
3. Git clone [my Neovim config](https://github.com/AddysonG/nvim) into `~/AppData/Local/nvim/` (this is where Neovim's config is stored on Windows).

### VSCode

Refer to my [VSCode config](https://github.com/AddysonG/vscode)
