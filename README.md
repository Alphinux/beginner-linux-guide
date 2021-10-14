# Linux Guide
## Introduction
This guide aims to explain how to use some basic linux features and software like github.
## Contents
- [Introduction](#introduction)
- [Glossary](#glossary)
- [Distrobutions](#distrobutions)
## Glossary
| Word | Description |
| --- | --- |
| GUI | Graphical User Interface |
| WM | (Window Manager) Controls the windows in a GUI |
| DE | (Desktop Enviroment) A WM with additional Software |
| BIOS | (Basic Input/Output System) The software that controls the components of your device |
| BIOS-Settings | Settings you can access by hitting a devicespecific key during startup |
| Secure Boot | Option in the BIOS-Settings that needs to be disabled to boot linux |
| Distribution | The linux kernel bundelt with the software to make it usable |
| Package Manager | A piece of software that lets you install software from a repository |
| Repository | A collection of software often used by a package manager |
## Distrobutions
A distribution - short distro - is basically the linux kernel - the core of an os - bundelt with the software necessary to make it usable. 

When picking a distro it important to take your technical knowledge and expertise in account. Some distros are better for beginners than others. 
For example there are some like Ubuntu, Pop_OS, ZorinOS which focus more on beginners. 
And on the other side of the spectrum there are distros like Archlinux, Gentoo and Voidlinux, 
these are for power-users and therefor harder to use and understand.

One thing that I think is also important, is what the distros package manager is and its repositorys - short repo.
Some repos are more focused on cutting edge and availability while other are more focused on stability.

Most of the distros that are not as popular as Ubuntu, Debian, Arch etc. are based on one of the popular distros. 
But there are also distros that are made from scratch.
### [Ubuntu](Ubuntu.com)
A distro used by **beginner and advanced users**. It has a **big community** so its easy to find support. It uses Gnome as its Desktop Enviroment and **apt** as its package manager.
#### Distros based on Ubuntu
- [Linux Mint](linuxmint.com)
- [ZorinOS](zorinos.com)
- [Pop!_OS](pop.system76.com)
- [Elementary OS](elementary.io)
### [Debian](debian.org)
Debian is a distro used by **advanced users**. It's more **stable and lightweight** than Ubuntu. It uses **dpkg** as its package manager
#### Distros based on Debian
- [MX Linux](mxlinux.org)
- [Deepin](deepin.org)
- [ParrotOS](parrotsec.org)
### [Archlinux](archlinux.org)
Archlinux - short Arch - is a distro used by **expert users**. It's extremly **lightweight and also stable**. It uses **pacman** as its package manager.
#### Distros based on Arch
- [Manjaro](manjaro.org)
- [EndeavourOS](endeavouros.com)
- [Garuda Linux](garudalinux.org)
- [ArcoLinux](arcolinux.com)
## Installation
Now if you have selected a distro, we can install it. This isn't a difficult process most of the time but depends on your distro. 
### Steps
- Disabling secure boot
- Creating boot usb
- Booting
- Installation
- Reboot
### Disabling secure boot
Secure boot limits the operating systems you can boot up to "offical" ones like Windows. 
To disable it you need to access your BIOS-Settings. This can be done by pressing a key during startup.
Which key depends on your manufacturer. You might have to do a google search.

If you have managed to boot into your BIOS-Settings, it should look something like this:
![BIOS](https://lab4sys.com/wp-content/uploads/2020/03/bios-1320x743.jpg)
![UEFI BIOS](https://kids.pplware.sapo.pt/wp-content/uploads/2013/11/uefi_01-560x352.jpg)
