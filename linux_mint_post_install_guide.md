# Linux Mint post-install guide
### Get the very latest Nvidia Drivers  (if necessary)
Go to **Software Sources -> PPAs**, click on **ADD** and paste the following:
```ppa:graphics-drivers/ppa```
### Get the very latest Mesa drivers (if necessary)
Go to **Software Sources -> PPAs**, click on **ADD** and paste the following:
```ppa:kisak/kisak-mesa```
### Install the latest Mint kernel (Much safer method!)
Update manager -> Linux kernels. Choose the very latest kernel version provided by Mint. Using kernels outside what Linux Mint provides will break Nvidia drivers. Unless you know what you are doing, please do not use external repositories on Mint!
### Install additional codecs
Either install them during the installer, or post-installation by going to **Start Menu -> Sound & Video -> Install Multimedia Codecs.**
### [Enable z-ram (optional)](https://forums.linuxmint.com/viewtopic.php?t=427964)
### [Speed up Linux Mint (optional)](https://easylinuxtipsproject.blogspot.com/p/speed-mint.html)
### Enable NTSYNC (helps improve performance in games. Make sure to run them with Proton-GE!)
```echo ntsync | sudo tee /etc/modules-load.d/ntsync.conf && sudo modprobe ntsync```
