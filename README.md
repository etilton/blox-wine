# blox-wine

This is a PPA for [winehq-staging](https://wiki.winehq.org/Download) built with the mouse fix.
I may add other patches in as necessary/requested.
My current focus is making it easier for those with limited hardware or knowledge of
software compilation to install a Roblox-friendly wine package on Debian/Ubuntu.

In the future I hope to debianize wine-tkg-git, so we can get that to more users as well.

### Installing this Repository

**Using curl:**

    curl -s --compressed "https://etilton.github.io/blox-wine/BLOXKEY.gpg" | sudo apt-key add -
    sudo curl -s --compressed -o /etc/apt/sources.list.d/blox-wine.list "https://etilton.github.io/blox-wine/blox-wine.list"
    sudo apt update
    sudo apt install --install-recommends winehq-staging

**Using wget:**

    wget -q -o /tmp/BLOXKEY.gpg "https://etilton.github.io/blox-wine/BLOXKEY.gpg" && sudo apt-key add /tmp/BLOXKEY.gpg
    sudo  wget -q -o /etc/apt/sources.list.d/blox-wine.list "https://etilton.github.io/blox-wine/blox-wine.list"
    sudo apt update
    sudo apt install --install-recommends winehq-staging
