# Ubuntu post-install guide
### Add Flatpak support
```sudo apt install flatpak && flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo```
### Add AppImage support
```sudo apt install libfuse2 -y```
### Additional multimedia codecs, proprietary drivers & fonts for better compatibility with Microsoft Office documents
```sudo apt install ubuntu-restricted-extras fonts-crosextra-caladea fonts-crosextra-carlito```
### Install Nvidia drivers
If the drivers did not install during setup, use **Additional drivers** app to install the Nvidia drivers. Always use the recommended version!
### Enable NTSYNC (helps improve performance in games. Make sure to run them with Proton-GE!)
```echo ntsync | sudo tee /etc/modules-load.d/ntsync.conf && sudo modprobe ntsync```

# Optional tweaks.
### For Kubuntu: Get rid of Snaps
Use the scripts provided in [this guide](https://gitlab.com/scripts94/kubuntu-get-rid-of-snap)
