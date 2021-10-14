# Linux Guide
## Introduction
This guide aims to explain how to use some basic linux features and software like github.
## Contents
- [Introduction](#introduction)
- [Glossary](#glossary)
- [Distrobutions](#distrobutions)
- [Installation](#installation)
- [Package Manager](#package_manager)
- DE / WM
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
| Command | A word (or string) you enter in a command-line |
| Options | The word option in the context of a command stands for `-<letter>` |
| Flag | The word Flag in the context of a command stands for `--<letters>` |
| Dependencies | Software that the software depends on |
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
Debian is a distro used by **advanced users**. It's more **stable and lightweight** than Ubuntu. It uses **apt** as its package manager
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
In here you have to navigate to the option for "Secure Boot". You will probably find it under Boot or Security.
Set it to off and make sure to save your changes.
### Creating boot usb
For making your usb bootable you can use a tool like Rufus or BalenaEtcher.
I prefer BalenaEtcher because its really easy to use. 
Simply choose the ISO-Image for your distro that you downloaded and select the usb drive you want it to be flashed on.
**All the data on that usb stick is going to get _deleted_**
### Booting
To boot in your recently aquired usb, you have to again hit a key during startup to open the boot menu.
This probably isn't the same as the key you use for the BIOS.
There you select the usb we made. Then Linux is going to boot.

Sometimes your required to enter a password. If the user is "liveuser", the password is very likely to be "liveuser" aswell.
### Installation
When your distro has booted (and you're logged in) the Installer will open by itself most of the time. If it doesn't look for an app launcher or a dock where you open it. The installers are going to differ but there is an installer used by a lot of distros named [Calamares](calamares.io):
![Calamares Installer](https://calamares.io/images/gallery/page-partition.png)
The installation with Calamares is pretty easy and should be no problem. 

When you are asked to select or create a partition, you have to be carefull. First of all, make sure you have selected the right drive.
Then look for free space or a partition you made where you want to install Linux. 

If there is no free space or no partition you want to install Linux on,
you will want to resize one of the existing partitions, your Windows Partition for example.
To do this you can use the [Disk Managment Tool](https://docs.microsoft.com/en-us/windows-server/storage/disk-management/overview-of-disk-management) on Windows or [GParted](gparted.org).
### Reboot
After the installation finished you will be prompted to reboot.
Do this and unplug your usb so it will boot into your fresh Linux installation. 
Log in with your previously created user account.
## Package Manager
In this chapter I will explain what a package manager is and how to use one.

A package manager lets you install/remove and update software from a repository. There are different package managers for different distribtions.

**Some systems may have [Pamac](#pamac) installed, which is a GUI way to use a package manager. You will find it in the app launcher under the name "Add/Remove software"**

The most common are:
### apt
#### Install
If you want to install a package type ` sudo apt install <package> `

Some packages might require the command ` sudo apt-get install <package> `
#### Uninstall
If you want to remove a package issue the command ` sudo apt remove <package> `

If you also want to remove the config file use the flag ` --purge ` so ` sudo apt remove --purge <package> `
#### Update
The command ` sudo apt update ` updates the local index of the repository, the index is the list of all the available packages and their versions.

After that to really update the system enter ` sudo apt upgrade `
#### Help
If you have any questions about apt try ` apt help `
## pacman
With pacman you will have to use different flags to install/remove and update.
#### Install
To install a package with pacman use the ` -S ` flag: ` sudo pacman -S <package> `
It's recommended to update the database before you install a package.
#### Remove
To remove only the package use the ` -R ` flag: ` sudo pacman -R <package> `

To remove the package and its dependencies that are not used by another program use the ` -Rs ` flag.

**Finally to remove the package, avoid orphonaged dependencies and delete it's local configureation use the ` -Rns ` flag,
which is the way to go most of the time.**
#### Update
To update the system use ` sudo pacman -Syu `

To just update the database without updating the packages use ` sudo pacman -Syy `
### Pamac
Pamac is an application which let's you interract with your package manager without using the commandline. You can install, remove, search and update packages.
It can be found in the app launcher under the name "Add/Remove software". ![Pamac](https://forum.endeavouros.com/uploads/default/original/2X/3/37c447d937f4b7d79b51757682aa531ceeefbb8d.png)
## DE / WM
To do
