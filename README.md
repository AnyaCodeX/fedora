## Fedora Terminal Commands
Some commands that i use for fedora installs on virtual machines.

## uupdate / distro-sync / autoremove
```
sudo dnf update
sudo dnf distro-sync
sudo dnf autoremove
sudo dnf update --refresh && sudo dnf distro-sync --refresh
```
## dnf.conf
```
echo 'max_parallel_downloads=6' | sudo tee -a /etc/dnf/dnf.conf
echo 'fastestmirror=True' | sudo tee -a /etc/dnf/dnf.conf
echo 'deltarpm=True' | sudo tee -a /etc/dnf/dnf.conf
echo 'defaultyes=True' | sudo tee -a /etc/dnf/dnf.conf 
```
## RPM Fusion free and nonfree repository & AppStream metadata
```
 sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
sudo dnf groupupdate core
```
## Flatpacks
```
sudo dnf install -y flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo 
```
## Fedora sudo dnf remove
```
akregator - Feed Reader
bluedevil - Bluetooth stack for KDE
dragon - Media player
elisa-player - Elisa music player
fedora-bookmarks - Fedora bookmarks
firefox - Mozilla Firefox Web browser
kamoso - Application for taking pictures and videos from a webcam
kmahjongg - A tile matching game
kmail - Mail client
kmines - A classic Minesweeper game
konversation - A user friendly IRC client
korganizer - Personal Organizer
kpat - A selection of solitaire card games
krdc - Remote desktop client
krfb - Desktop sharing
libreoffice-core - Core modules for LibreOffice
okular - A document viewer
spectacle - Screenshot capture utility 
```
### Nobara sudo dnf remove
```
bluedevil - Bluetooth stack for KDE
elisa-player - Elisa music player
firefox - Mozilla Firefox Web browser
kamoso - Application for taking pictures and videos from a webcam
okular - A document viewer
spectacle - Screenshot capture utility 
```
### Hyperlinks
- https://getfedora.org/
- https://docs.fedoraproject.org/en-US/quick-docs/
- https://rpmfusion.org/Configuration
