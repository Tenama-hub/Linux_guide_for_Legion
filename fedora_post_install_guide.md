# Fedora post-install guide
If you are lazy and you want to build your own install script, [click here](https://nattdf.streamlit.app/)<br>
Honorable mentions: [Noble guide](https://github.com/wz790/Fedora-Noble-Setup)
| Tweak Name | Command/Link |
| ------------- | ------------- |
| **Enable 3rd party repositories** | Enable them during the "welcome" post-install or use the command below:<br>`sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm && sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm`  |
| **Enable full flatpak access** | Fedora packs its own version of flatpak, which is inferior compared to the main repo. `flatpak remote-delete fedora && flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo` |
| **Install Nvidia drivers** | Install the driver by using the command below, then wait 10-15 minutes before rebooting!!!<br>`sudo dnf install akmod-nvidia xorg-x11-drv-nvidia-cuda -y`<br>[Click here for more details](https://rpmfusion.org/Howto/NVIDIA?highlight=%28%5CbCategoryHowto%5Cb%29) |
| **Install multimedia codecs** | Follow the [official RPMFusion guide](https://rpmfusion.org/Howto/Multimedia?highlight=%28%5CbCategoryHowto%5Cb%29)  |
| **Enable Secure Boot** | [Click here for more details](https://github.com/roworu/nvidia-fedora-secureboot) |
| **Enable Terra repository (optional)** | If you want to use a package that isn't provided by either RPMFusion or Fedora, [Terra repos](https://terrapkg.com/) can provide that. Do remember that they provide extra repositories, and will conflict with both Negativo17 and RPMFusion. The base repo should be more than enough. <br> Run this in terminal: `dnf install --nogpgcheck --repofrompath 'terra,https://repos.fyralabs.com/terra$releasever' terra-release` |
