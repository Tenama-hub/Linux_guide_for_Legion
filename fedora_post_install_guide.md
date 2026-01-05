# Fedora post-install guide
If you are lazy and you want to build your own install script, [click here](https://nattdf.streamlit.app/)

Cherry-picked from [this website](https://rpmfusion.org/Howto). Honorable mentions: [Noble guide](https://github.com/wz790/Fedora-Noble-Setup)
### Enable 3rd party repositories (MANDATORY!)
```sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm && sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm```
### Enable full flatpak access (non-filtered version that isn't bundled by default on Fedora)
```flatpak remote-delete fedora && flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo```
### Install Nvidia drivers
This can be easily done through the provided package manager. If you want to use secure boot, please [check this guide before continuing!](https://github.com/roworu/nvidia-fedora-secureboot)   
If you can't do it for some reason, install the driver by using the command below, then wait 10-15 minutes before rebooting!!!   
```sudo dnf install akmod-nvidia xorg-x11-drv-nvidia-cuda -y```
### Install additional codecs
```dnf swap ffmpeg-free ffmpeg --allowerasing -y && dnf update @multimedia --setopt="install_weak_deps=False" --exclude=PackageKit-gstreamer-plugin -y && dnf update @sound-and-video -y ```   
If you use Intel:   
```sudo dnf install intel-media-driver -y```   
If you use AMD:   
```sudo dnf swap mesa-va-drivers mesa-va-drivers-freeworld -y && sudo dnf swap mesa-vdpau-drivers mesa-vdpau-drivers-freeworld -y```   
If you have an Nvidia gpu:   
```sudo dnf install libva-nvidia-driver -y```   
### Enable NTSYNC (helps improve performance in games. Make sure to run them with Proton-GE!)
```echo ntsync | sudo tee /etc/modules-load.d/ntsync.conf && sudo modprobe ntsync```
