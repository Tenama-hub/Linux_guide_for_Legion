# Ubuntu/Kubuntu post-install guide


| Tweak Name | Command/Link/Path |
| ------------- | ------------- |
| **Add Flatpak support** | `sudo apt install flatpak && flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo` |
| **Add Legacy AppImage support (if Appimages crash or don't launch)** | `sudo apt install libfuse2 -y` |
| **Additional multimedia codecs, proprietary drivers & fonts for better compatibility with Microsoft Office documents** | `sudo apt install ubuntu-restricted-extras fonts-crosextra-caladea fonts-crosextra-carlito`<br>If you use Kubuntu, replace `ubuntu-restricted-extras` with `kubuntu-restricted-extras` |
| **Install Nvidia drivers** | If the drivers did not install during setup, use **Additional drivers** app to install the Nvidia drivers. Always use the recommended version! |
| **Get rid of Snaps (Kubuntu, but can be used on Ubuntu too. Just be cautious!)** | Use the scripts provided in [this guide](https://gitlab.com/scripts94/kubuntu-get-rid-of-snap) or use Kubuntu's minimal install. This is an optional step. |
