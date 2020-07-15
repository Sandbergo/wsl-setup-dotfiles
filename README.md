<h1 align="center">WSL Setup Dotfiles</h1>

<div align="center">

  [![Status](https://img.shields.io/badge/status-active-success.svg)]() 
  [![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center">
<img src="img/desktop.PNG" alt="Example terminal">
</p>
<br> 

## 📝 Table of Contents
- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## 🧐 About <a name = "about"></a>
An (almost) automatic script for setting up a liveable bash terminal via Ubuntu in Windows Subsystem for Linux, as well as the home for (some of my) dotfiles. 

## 🏁 Getting Started <a name = "getting_started"></a>

First, Install DejaVu Sans Mono from nerd fonts, download the Windows Compatible version.

### Install WSL

If you do not already have `WSL`, follow these steps to install. First, download the Windows Terminal from the Microsoft Store. Open `Powershell`, and run the following commands:

```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

Additionally, if you want to make WSL 2 your default architecture you can do so with this command:

```
wsl --set-default-version 2
```

After restarting, install Ubuntu from the [Microsoft Store](https://www.microsoft.com/pt-br/p/ubuntu/9nblggh4msv6?activetab=pivot:overviewtab) or through the terminal:

```
curl.exe -L -o ubuntu.appx https://aka.ms/wsl-ubuntu
```

Launch `Ubuntu.exe` from the _Start Menu_. You’ll be asked to enter a username and password.

### Install packages 

LSDeluxe:
Download the latest `.deb` package from the [release page](https://github.com/Peltoche/lsd/releases) and install it via:

```sh
sudo dpkg -i lsd_7.2.0_amd64.deb
```

Github CLI:
Download the latest `.deb` file from the [releases page](https://github.com/cli/cli/releases/)
and install it via:

```sh
sudo apt install ./gh_*_linux_amd64.deb
```
### Set up dotfiles

If you already have `Windows 10` and `WSL` installed, run these commands in the bash terminal:

```
git clone https://github.com/Sandbergo/wsl-setup-dotfiles
chmod 700 wsl-setup-dotfiles/ -R
cd wsl-setup-dotfiles
./install.sh
./symlinks.sh
```

### Remote - WSL

Install the [Remote - WSL](https://aka.ms/vscode-remote/download/wsl) extension in VSCode to get a better experience with `WSL`.


## 🎈 Usage <a name="usage"></a>
Fork the repository and track your own dotfiles.

## ✍️ Authors <a name = "authors"></a>
- Lars Sandberg [@Sandbergo](https://github.com/Sandbergo)


## 🎉 Acknowledgements <a name = "acknowledgement"></a>
- Trent Nicholson [@NICHTJ3](https://github.com/NICHTJ3)
- Samuel Ramos [@samuelramox](https://github.com/samuelramox)