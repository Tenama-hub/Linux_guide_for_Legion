# 🐧 Linux guide for Legion laptops, handhelds & PCs 🐧
# ⭐ LAST UPDATE :  05 JANUARY 2025 ⭐
A simple how-to-guide for legion products. Can be universal if you know what you are doing. A little opinionated, but it was made with the purpose of making linux easy-to-use and simple for Windows migrants or linux newbies. A backup of my guide from the Legion discord, just in case :)   
Contribution is always welcomed! Feel free to join our [discord group as well](https://discord.gg/yGkfEUVa). 
# Table of contents
### [Distribution recommendation](https://github.com/Tenama-hub/Linux_guide_for_Legion/tree/main?tab=readme-ov-file#distribution-recommendation-1)
### [Installing Legion tools and drivers](https://github.com/Tenama-hub/Linux_guide_for_Legion/tree/main?tab=readme-ov-file#installing-legion-tools-and-drivers-1)
### [Apps & Tools recommendation](https://github.com/Tenama-hub/Linux_guide_for_Legion/tree/main?tab=readme-ov-file#app--tools-recommendation)
### [Battery saving tools](https://github.com/Tenama-hub/Linux_guide_for_Legion/tree/main?tab=readme-ov-file#battery-saving-tools-1)
### [Wine front-ends](https://github.com/Tenama-hub/Linux_guide_for_Legion/tree/main?tab=readme-ov-file#wine-front-ends-1)
### [NVIDIA fixes](https://github.com/Tenama-hub/Linux_guide_for_Legion/tree/main?tab=readme-ov-file#nvidia-fixes-1)
### [General bugs and fixes](https://github.com/Tenama-hub/Linux_guide_for_Legion/tree/main?tab=readme-ov-file#general-bugs-and-fixes-1)
### [General advice and websites recommendation](https://github.com/Tenama-hub/Linux_guide_for_Legion/tree/main?tab=readme-ov-file#general-advice-and-websites-recommendation-1)

# __Distribution recommendation__
Based on my own experience + community feedback. You are not forced to follow this recommended list.
### Linux Mint ([Post-Install guide](https://github.com/Tenama-hub/Linux_guide_for_Legion_laptops_-_handhelds/blob/main/linux_mint_post_install_guide.md))
* Comes with Cinnamon/XFCE/Mate (replicate windows 7/10 layout)
* Comes with many useful tools OOTB
* Customizable touchpad gestures like on Windows (Cinnamon only)
* Fantastic for daily use, especially for beginners
* Stable release distribution   
o Lags behind some of the newer technologies and packages. May cause issues on newer legion laptops   
o Still uses X11, which is behind certain modern features (dual screens may not work as intended for example)
### Fedora ([Post-Install Guide](https://github.com/Tenama-hub/Linux_guide_for_Legion_laptops_-_handhelds/blob/main/fedora_post_install_guide.md))
* Comes with Gnome/Plasma by default. Offers different flavors of desktops too
* Power saving tools pre-installed
* Offers the "vanilla" experience that desktop developers have envisioned
* Solid for gaming and general use
* Semi-Rolling release distribution    
o Codecs & Nvidia drivers are not pre-installed   
o Requires a little knowledge and maintanence when necessary due to it being semi-rolling
### Ubuntu ([Post-install guide](https://github.com/Tenama-hub/Linux_guide_for_Legion_laptops_-_handhelds/blob/main/ubuntu_post_install_guide.md))
- Comes with Gnome by default. Can use other variants with different desktops
- Pre-install Nvidia drivers and codecs during the installation process
- Pretty good documentation & huge active base
- Great for daily use
- Offers both a rolling release model or LTS   
o Prioritizes Snaps over any other package formats and may have their own issues (depending on the app). You can still use Debs, Appimages (install GearLever) or Flatpaks (install Warehouse from Flathub) as alternatives   
o System issues may occur on non-LTS versions
### CachyOS
- Comes with Plasma by default. Can choose a different desktop during installation
- Nvidia drivers pre-installed and pre-configured
- Packages are optimized based on your hardware, which might increase performance and smoothness
- GUI package manager and small tools to get you up and running
- Can convert existing arch distributions (EndeavourOS/Arch) to CachyOS
- Rolling release distribution   
o Package optimizations don't apply to Flatpaks/AppImages/Snaps(main reason why they aren't preinstalled)   
o Not suitable for beginners/those that don't want to rely on the terminal most of the time   
o Requires a in-depth knowledge of Arch Linux
### Bazzite
- Comes with Plasma/Gnome by default
- Pre-installed Steam, Nvidia drivers and codecs
- Can be used for any use case, not just gaming
- Great alternative to SteamOS for handhelds
- Very hard to break and requires little to no maintenance due to its atomic nature
- Atomic distribution based on Fedora. Updates can be done in the background and are relatively quick   
o Apps can only be installed through Flatpaks, AppImages, HomeBrew and Distrobox   
o You cannot do system-level changes like on traditional distros   
o Support leaves more to be desired
### ***AVOID!***
### Debian (**Unless you use Debian Testing/Sid**)
Despite being extremely stable with little to no breakages, it is not suitable for legion laptops. Updates (especially MAJOR ones) are released very slowly. You can use it if you know what you are doing.
### Pop!_OS (**for now**)
The new Cosmic desktop variant lacks critical fixes for gaming and it is still in alpha.
### SteamOS 
Doesn't have an nvidia alternative and is not finished for **non-handheld devices**. If you REALLY need something similar, use Bazzite.
### Manjaro
It's future is uncertain as it has a history of a lot of wrongdoings, strange decisions and updates that led to broken systems or significant bugs. Although, there have been less incident reports of broken systems over the recent years.
### Business-related distributions
Oracle Linux, Clear Linux or anything made for business purposes. Self explanatory.
### Hacking/Cybersecurity distributions
Parrot, Tails, Kali Linux and alike are meant to be used either through VMs or external devices, not on actual hardware.
### Obscure/outdated distributions
Avoid distributions maintained by randoms/single developer, that are **"too good to be true"** (nonsense promises) or try to replicate Windows 1:1. 
### Hobby/niche distributions
Do keep in mind you won't have any guarantee they won't die off in the future or have support outside their forums. They also come with issues of their own (unorthodox way of handling packages, low-quality in-house tools, kernel problems, questionable community, very low amount of maintainers etc). Some example of such distros are Nobara, RegataOS, Garuda, ZorinOS, PikaOS etc.

# __Installing Legion tools and drivers__ 
### **As of Kernel 6.17, power profiles switching and battery conservation don't require the Legion Driver.**   
This allows you to use most, if not all the legion exclusive features on linux (fan control, panel overdrive, etc). Comes with a GUI to easily access these said features.   
If you use Plasma and you want to have a tool that gives you the important options at a glance, I recommend using [PlasmaVantage](https://gitlab.com/Scias/plasmavantage) or Cinnamon's inspired counterpart from the [desktop plugin store](https://cinnamon-spices.linuxmint.com/applets/view/395)   
## Distro packages (highly recommended)
- [**Debian/Ubuntu**](https://github.com/MrDuartePT/pacstall-programs/tree/lll-repo)
- [**Fedora**](https://copr.fedorainfracloud.org/coprs/mrduarte/LenovoLegionLinux/)
  - [Alternate link](https://mrduartept.github.io/LLL-pkg-repo)
- **Arch Linux**:
    - [lenovolegionlinux-git](https://aur.archlinux.org/packages/lenovolegionlinux-git)
    - [lenovolegionlinux-dkms-git](https://aur.archlinux.org/packages/lenovolegionlinux-dkms-git)
- **Gentoo**:
    - [GURU Overlay](https://gitweb.gentoo.org/repo/proj/guru.git)
    - [ebuild](https://gpo.zugaina.org/sys-firmware/lenovolegionlinux)
- [**NixOS**](https://search.nixos.org/packages?channel=unstable&from=0&size=50&sort=relevance&type=packages&query=lenovo-legion)
## Manual Install Module
The project's [github page](https://github.com/johnfanv2/LenovoLegionLinux?tab=readme-ov-file#bulb-instructions) should give you enough instructions to aid you in the process.
After it's done, to check if module is built and installed correctly, enter the following command
```sudo lsmod |grep legion_laptop```.
The output should show that legion_laptop and platform profile modules are loaded.

# __App & Tools recommendation__
### [Bazaar](https://flathub.org/en/apps/io.github.kolunmi.Bazaar)
Front-end for managing Flatpak packages, if your distribution's package manager is not good enough for this use case. Used by default on Bazzite.
### [Retrodeck](https://flathub.org/en/apps/net.retrodeck.retrodeck)
An all-in-one emulation front-end that comes with the most popular emulators, pre-configured OOTB. You can configure and add BIOS files for each component through its configurator app.
### [Easyeffects](https://flathub.org/en/apps/com.github.wwmm.easyeffects)
Front-end equalizer for managing your microphone and speakers. Want to filter your microphone background sounds? Want to have a better sound quality? Then this app is for you.
### [Warehouse](https://flathub.org/en/apps/io.github.flattool.Warehouse)
All-in-one flathub package manager (install flatpaks, delete leftover data, manage flatpak data). A more technical variant of Bazaar.
### [Flatseal](https://flathub.org/en/apps/com.github.tchx84.Flatseal)
Manage Flatpak permissions. Useful for non-KDE Plasma distributions.
### [GearLever](https://flathub.org/en/apps/it.mijorus.gearlever)
Front-end Appimage manager. Allows "installing" said packages, without needing to fetch them in the file manager.
# __Battery saving tools__
The tool that comes bundled with your distribution of choice should be good enough.
### WARNING
* Some of the tools will not work together with the rest (exceptions may apply). Make sure you remove all the tools besides the one you want to currently use.
* Do **NOT** use configuration files from laptops you don't **OWN**. This may cause severe issues with your hardware! You have been warned.
### Tuned 
A mix between power profiles daemon and TLP. Easily integrated with all desktops that feature Power profiles switching and can be customized to your needs. Used on Fedora & Bazzite by default.
[More info](https://github.com/redhat-performance/tuned)
### Power Profiles Daemon
Used in majority of distros. Plays well with pstate scalers and any hardware in general. Not as powerful as TLP but it gets the job done. Conflicts with the rest of the tools besides powertop
[More info](https://gitlab.freedesktop.org/upower/power-profiles-daemon)
### TLP 
A shell script that applies extensive configurations based on battery or AC. Will cause issues if incorrectly configured. Conflicts with other tools.   
- **Debian/Ubuntu**:
```sudo apt install tlp```
- **Fedora**:
```sudo dnf install tlp```
- **Arch Linux**:
```sudo pacman -S tlp```
   
For easier tool access, [install the gui version](https://github.com/d4nj1/TLPUI)   
After that we can configure TLP.   
Open TLPUI and change your settings(Strictly optional. Default settings are fine) . Enable the tool by typing in terminal:   
```sudo systemctl enable tlp.service && sudo systemctl start tlp.service```
### Auto-Cpufreq
A simple script that changes how the cpu should scale depending if you are on AC or Battery. Plays well with pstate, but it may cause issues with some hardware.
- **Debian/Ubuntu**:
```git clone https://github.com/adnanhodzic/auto-cpufreq.git && cd auto-cpufreq && sudo ./auto-cpufreq-installer```
- **Fedora**:
```git clone https://github.com/adnanhodzic/auto-cpufreq.git && cd auto-cpufreq && sudo ./auto-cpufreq-installer```
- **Arch Linux**:
```sudo pacman -S auto-cpufreq```
   
[More Info](https://github.com/AdnanHodzic/auto-cpufreq/tree/fdb20f5ea2f94ed9146299b87ad03dc1f64c79ec#auto-cpufreq-installer)
### Powertop 
A shell script tool that allows you to optimize some parts of the hardware to go on a low power state when not in use. I'd recommend using it only to check your power draw, as the optimization feature is already applied by other power saving tools.
- **Debian/Ubuntu**:
```sudo apt install powertop```
- **Fedora**:
```sudo dnf install powertop```
- **Arch Linux**:
```sudo pacman -S powertop```

After installing it, you can use the app by typing:   
```sudo powertop```   
If you want to use it to optimize the hardware power usage (power-profiles/auto-cpufreq ONLY), run this command:   
```sudo powertop --calibrate && sudo powertop --auto-tune```

# __Wine front-ends__
[Wine](https://www.winehq.org/) is a special tool that allows running Windows apps in Linux. This sparked the creation of proton, that is actively used for games.
### [Lutris](https://lutris.net/)
Allows installing, configuring games & apps in one-in-all tool. Comes with features like automatic installation of games through community patches and importing game libraries from steam, GOG and Epic Games Store. Several scripts are outdated and could cause issues, some still relying on the discontinued WINE-GE runner.
### [Heroic game launcher](https://heroicgameslauncher.com/) 
Allows installing & configuring games & apps in one-in-all tool from Epic Games Store, Humble, Amazon, GoG, Origin, Ubisoft Connect and local games/backups.
### [Faugus-Launcher](https://github.com/Faugus/faugus-launcher) 
A WIP project that takes advantage of [UMU](https://github.com/Open-Wine-Components/umu-launcher) and Proton-GE. It's not as feature complete as Lutris, but it gets the job done without extra shenanigans.
### [Bottles](https://usebottles.com)
Allows creating separate prefixes for each use case. Can auto install game launchers and apps. Can also use other wine versions besides the ones provided by the dev. There are some questions regarding the status of the project and founding, but it's still usable...for now.
### [WineZGUI](https://github.com/fastrizwaan/WineZGUI)
A simple, easy to use and straight-forward wine frontend.
### [Port-Proton](https://github.com/Castro-Fidel/PortWINE)
Formerly PortWINE. It's simple to use, can auto-install game launchers and has enough configuration tools. There are some trust issues (mainly the dev is Russian, take that how you will), doesn't allow custom wine launch options, apps start slower than the competition and some options are counter-intuitive.

# __NVIDIA fixes__
All of these parameters need to be put in your bootloader config file (GRUB/Systemd/Limine etc)
- Fix Wayland performance/smoothness. May not fully fix it, but it's worth a shot.   
  ```nvidia-drm.modeset=1 nvidia-drm.fbdev=1```
- Fix Nvidia card not powering down (There is a regression in the driver 590, making this fix useless for now)
  ```nvidia.NVreg_EnableGpuFirmware=0```
- Fix sleep/suspend issues showing screen artefacts or other problems   
  ```nvidia.NVreg_PreserveVideoMemoryAllocations=1```

# __General bugs and fixes__
### System swappiness (if you have >= 16GB ram)
Setting your swappiness to 10 will reduce stuttering when your RAM memory is almost full, as the system will not prioritize using your SWAP partition as system memory for apps.   
```sudo nano /etc/sysctl.conf```
Add ```vm.swappiness=10``` Then save. (ctrl+O then hit enter)
### Bad speakers quality 
If your speakers sound shallow and bad, try out [this preset](https://github.com/Tomiscout/Lenovo-Legion-5-Pro-Linux-guide/tree/main/easyeffects) (I might tweak it to not require easyeffects. Stay tuned!). If you use handhelds, [better give this one a try](https://www.reddit.com/r/LegionGo/comments/1m7632y/legion_go_s_steam_os_audio_fix_pipewire_eq/).
### Bad laptop mic quality
Set your microphone volume to 30-50%, then install this [noise cancelling module](https://github.com/Rikorose/DeepFilterNet/blob/main/ladspa/README.md) or use EasyEffects
### Refresh rate/ VRR not working
Some screen panels will force you to use either the highest or the lowest refresh rate (even keep you at the highest resolution). Edid.bin tells your screen what resolutions and refresh rates it supports. This is a problem that affects some panels due to generic drivers being used instead of the ones provided by the screen providers.
### WARNING
* **UNDER NO CIRCUMSTANCE, DO NOT INCREASE/DECREASE THE RESOLUTION OF YOUR SCREEN/REFRESH RATE PAST YOUR SPECS! DOING SO WILL CAUSE SEVERE ISSUES**
1. In WINDOWS, download the CRU tool. Open it, then click on **EXPORT**. Save the file as edid.bin. (If you are able to switch between the highest and lowest refresh rate but you can't use VRR in Linux, extract the edid file from your distro and add what is needed)
2. Copy the file to a usb drive and boot back to linux.
3. Open a terminal and type the following commands:
```cd /lib/firmware && sudo mkdir edid && sudo cp (path to file)/edid.bin /lib/firmware/edid```
4. To make sure your edid file is recognized, use the following:   
```for p in /sys/class/drm/*/status; do con=${p%/status}; echo -n "${con#*/card?-}: "; cat $p; done```
   
For the below commands, replace [display_id] with the output of the connected display from the command ran earlier.
### For systemd-boot
```sudo kernelstub -a 'drm.edid_firmware={display_id}:edid/edid.bin video={display_id}:e'```
### For GRUB:
```sudo nano /etc/default/grub```, add ```drm.edid_firmware={display_id}:edid/edid.bin video={display_id}:e``` to **GRUB_CMDLINE_LINUX_DEFAULT**

Then run either ```sudo update-grub``` or ```sudo grub2-mkconfig -o /boot/grub2/grub.cfg```
Reboot.   
For Immutable/atomic distros based on Fedora( e.g. Bazzite), use the following:
```
sudo mkdir -p /etc/firmware/edid
sudo cp edid.bin /etc/firmware/edid
sudo rpm-ostree kargs --append-if-missing=drm.edid_firmware={display_id}:edid/edid.bin
sudo rpm-ostree kargs --append-if-missing=video={display_id}:e
```
In case the above commands don't work after running them, run these 2 as well:
```
sudo echo 'install_items+=" /etc/firmware/edid/edid.bin "' | sudo tee /etc/dracut.conf.d/edid.conf
sudo rpm-ostree kargs --append-if-missing=firmware_class.path=/etc/firmware
```

# __General advice and websites recommendation__
### General advice
* **It's best to do research on how to use Linux instead of jumping ship and expect the same workflow as on Windows. This is one of the many newbie traps!!**
* Don't install packages from the internet unless necessary. Always trust your SOFTWARE/PACKAGE MANAGER bundled with your distribution.
* Keep your system clean and up to date. Don't bloat it with useless tools or scripts that will cause more harm than good.
* Use distributions that are popular and come from reputable sources. You can game on any distro and apply the same tweaks to a "non-gaming" distribution.
* Don't rely on custom kernels to give you significant performance gains, unless necessary. Your mileage may vary, as always. Using the kernel bundled with your distribution is more than enough.
* Don't run scripts that claim to give you more performance, especially if they were not tested/from a untrusted source/maintainer. Those are the equivalent of running registry tweaks on windows to get free fps (aka a scam.)
* Don't distro-hop because some shiny new distribution hit the web or some distro promises better this & that. Remember : Distributions are just vanilla Linux with packages and such. They are all the same, but maintained differently.
* Don't bloat your distribution with custom repositories, unless you feel adventurous.
### Useful websites
To check if your games work on linux, these two websites will help you keep yourself updated:   
https://areweanticheatyet.com/   
https://www.protondb.com/   
https://appdb.winehq.org/
### Websites for linux news (desktops, distributions etc)
https://9to5linux.com/   
https://gamingonlinux.com/
