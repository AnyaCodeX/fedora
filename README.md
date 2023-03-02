## Fedora Terminal Commands
Some commands that i use for fedora installs on virtual machines.

## update
```
sudo dnf update
sudo dnf autoremove
sudo dnf distro-sync
```
## Tweeks for dnf.conf
```
echo 'max_parallel_downloads=10' | sudo tee -a /etc/dnf/dnf.conf
echo 'fastestmirror=True' | sudo tee -a /etc/dnf/dnf.conf
echo 'deltarpm=True' | sudo tee -a /etc/dnf/dnf.conf
echo 'defaultyes=True' | sudo tee -a /etc/dnf/dnf.conf
```
## Enable RPM Fusion free and the nonfree repository
```
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```
## Enable RPM Fusion AppStream metadata
```
sudo dnf group update core
```
## Enable Audio & Video Plugins
```
sudo dnf install gstreamer1-plugins-{bad-\*,good-\*,base} gstreamer1-plugin-openh264 gstreamer1-libav --exclude=gstreamer1-plugins-bad-free-devel
sudo dnf install lame\* --exclude=lame-devel
```
## Enable Flatpacks
```
sudo dnf install -y flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
## sudo dnf remove
```
sudo dnf remove akregator bluedevil dragon elisa-player fedora-bookmarks kamoso kmahjongg kmail kmines konversation korganizer kpat krdc krfb kwrite libreoffice-core okular spectacle
```
```
akregator - Feed Reader
bluedevil - Bluetooth stack for KDE
dragon - Media player
elisa-player - Elisa music player
fedora-bookmarks - Fedora bookmarks
kamoso - Application for taking pictures and videos from a webcam
kmahjongg - A tile matching game
kmail - Mail client
kmines - A classic Minesweeper game
konversation - A user friendly IRC client
korganizer - Personal Organizer
kpat - A selection of solitaire card games
krdc - Remote desktop client
krfb - Desktop sharing
kwrite - Text Editor
libreoffice-core - Core modules for LibreOffice
okular - A document viewer
spectacle - Screenshot capture utility
```
### Hyperlinks
- https://getfedora.org/
- https://docs.fedoraproject.org/en-US/quick-docs/
- https://rpmfusion.org/Configuration
