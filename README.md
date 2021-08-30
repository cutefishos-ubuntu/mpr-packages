<div align="center">
    <h1>MPR Package Repositorie</h1>
    <img height="150" src="https://dl.uploadgram.me/6119620f0356eh?raw">
</div>

This repository contains the PKGBUILDs of **Cutefish Desktop** environment in [MPR](https://mpr.hunterwittenborn.com/packages/?K=titenko&SeB=m) (*Makedeb Package Repository*) . If there is problem with each of them, please submit an issue and explain the problem.

# Installation

## Tap

These packages are available in [MPR](https://mpr.hunterwittenborn.com/packages/?K=titenko&SeB=m). You can install them easily with your [Tap](https://github.com/hwittenborn/tap)  helper of choice.

    tap install fishui libcutefish cutefish-wallpapers cutefish-statusbar cutefish-settings cutefish-qt-plugins cutefish-launcher cutefish-kwin-plugins cutefish-icons cutefish-filemanager cutefish-dock cutefish-core cutefish-screenlocker cutefish-calculator 

## Mpm

These packages are available in [MPR](https://mpr.hunterwittenborn.com/packages/?K=titenko&SeB=m). You can install them easily with your [Mpm](https://github.com/cutefishos-ubuntu/mpm)  helper of choice.

    mpm install fishui libcutefish cutefish-wallpapers cutefish-statusbar cutefish-settings cutefish-qt-plugins cutefish-launcher cutefish-kwin-plugins cutefish-icons cutefish-filemanager cutefish-dock cutefish-core cutefish-screenlocker cutefish-calculator

## Local build

[makedeb](https://github.com/makedeb/makedeb) takes PKGBUILD files and creates Debian packages installable with APT.

To build a package, you need to clone this repository:

    git clone https://github.com/cutefishos-ubuntu/mpr-packages.git

Download and install **makedeb**

**Using Tap or Mpm**

**Tap:**
    
    tap install makedeb

**Mpm:**

    mpm install makedeb

**From the official repository:**

First, add the signing key:

    wget -qO - 'https://proget.hunterwittenborn.com/debian-feeds/makedeb.pub' | gpg --dearmor | sudo tee /usr/share/keyrings/makedeb-archive-keyring.gpg &> /dev/null

Next, add the repository information to your system:

    echo 'deb [signed-by=/usr/share/keyrings/makedeb-archive-keyring.gpg arch=all] https://proget.hunterwittenborn.com/ makedeb main' | sudo tee /etc/apt/sources.list.d/makedeb.list

Lastly, update the repository cache on your system:

    sudo apt update

Install makedeb

    sudo apt install makedeb

**Building the package:**

Open the folder with the required package and run the `makedeb` command in the terminal

For detailed instructions use the command `makedeb --help`
