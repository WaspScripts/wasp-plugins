# wasp-plugins
This repository holds plugins for [WaspLib](https://github.com/WaspScripts/WaspLib).

If you are on Linux and using a somewhat modern kernel you'll need to either compile [RemoteInput](https://github.com/Brandon-T/RemoteInput) yourself or patch the one included in this repo.

To patch it you'll want to install `patchelf`:
```
# Debian:
sudo apt install patchelf
# Arch:
sudo pacman -S patchelf
# Fedora:
sudo dnf install patchelf
```
And patch the binary:
```
patchelf --clear-execstack wasp-plugins/libremoteinput/libremoteinput64.so
```
