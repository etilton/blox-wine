# blox-wine

This is a PPA for [winehq-staging](https://wiki.winehq.org/Download) built with the mouse fix.
I may add other patches in as necessary/requested.
My current focus is making it easier for those with limited hardware or knowledge of
software compilation to install a Roblox-friendly wine package on Debian/Ubuntu.

In the future I hope to debianize wine-tkg-git, so we can get that to more users as well.

### Installing from this Repository

In order for Wine to install your system must be set up for multilib support. To achieve this enter the command:

    sudo dpkg --add-architecture i386

Next, you need to add the the gpg key to the Apt keyring.

Using curl:

    curl -s --compressed "https://etilton.github.io/blox-wine/BLOXKEY.gpg" | sudo apt-key add -

Using wget:

    wget -qO - "https://etilton.github.io/blox-wine/BLOXKEY.gpg" | sudo apt-key add -
    
Now you can add the repository to your sources list(codename is bionic,bullseye,etc):
    
    echo "deb https://etilton.github.io/blox-wine/ <codename>/" > /tmp/blox_wine.list && sudo mv /tmp/blox_wine.list /etc/apt/sources.list.d/
    sudo apt update
    sudo apt install --install-recommends winehq-staging
