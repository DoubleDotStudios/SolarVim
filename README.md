# SolarVim

- [Introduction](#introduction)
  - [What is it?](#what-is-it?)
  - [What does it include?](#what-does-it-include?)
  - [Why call it SolarVim?](#why-call-it-solarvim?)
- [Installation](#installation)
  - [Dependencies](#dependencies)
  - [Backing up old configs](#backing-up-old-configs)
  - [SolarVim](#solarvim)
  - [Packages](#packages)
  - [Syntax Highlighters](#syntax-highlighters)
  - [LSPs](#lsps)

---
# Introduction

## What is it?
SolarVim is a custom configuration based on the [kickstart-modular.nvim](https://github.com/dam9000/kickstart-modular.nvim) framework. It uses a transparent Catppuccin Mocha colorscheme that's perfect for development at any time of the day.

## What does it include?

It includes:
- Neotree
- Lualine
- Snacks
- Telescope
- Treesitter
- Which-key
- Conform
- Autopairs

These are used to provide a lightweight, fully functional development environment that's ready out of the box.

## Why call it SolarVim?
The name SolarVim is a small nod to [LunarVim](https://www.lunarvim.org/) which I believe is a great startpoint for those who want to ease into Neovim which allows you to worry less about configuration and more about how the editor works (and how you escape).

SolarVim is pretty much a next step. Most of the configuration is done for you with simple commands for install syntax highlighters ans LSPs. A lot of this is thanks to [kickstart-modular.nvim](https://github.com/dam9000/kickstart-modular.nvim) which does a lot of the hard work setting up Lazy and Mason.

# Installation

## Dependencies

Basic tools: 
- git
- make
- unzip
- C Compiler (gcc)
- ripgrep
- Clipboard tool (xclip/xsel/win32yank or other depending on platform)

Looks:
- Any Nerd Font
  
Language Setup:
- The compiler/interpreter for the language

## Backing up old configs
If you have Neovim installed already then it's worth backing up your config to make sure you can go back to it if you want.
This can be done using `mv` on each of the folders your config uses:
```sh
mv ~/.config/nvim ~/.config/nvim.bak
mv ~/.local/share/nvim ~/.local/share/nvim.bak
mv ~/.local/state/nvim ~/.local/state/nvim.bak
```

## SolarVim
Clone the SolarVim repo to your Neovim config directory and then start Neovim:
```sh
git clone https://github.com/DoubleDotStudios/SolarVim.git ~/.config/nvim
nvim
```

## Packages
Once Neovim is opened after installing SolarVim, Lazy should open and install some packages. If it doesn't then type `:Lazy sync` and the packages will be installed.

After that's finished, type `:MasonInstallAll` and that will install the rest of the packages that SolarVim uses.

## Syntax Highlighters
To install a syntax highlighter simply type `:TSInstall language_name` and the highlighter will be installed.

## LSPs
To install an LSP simply type `:LspInstall language_name` and a popup will be displayed asking which LSP you would like to install for that language. Select the one you want and it'll be installed.
