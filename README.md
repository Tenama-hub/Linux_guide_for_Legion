# 🐧 Linux guide for Legion laptops, handhelds & PCs 🐧

Feel free to join our [discord group as well](https://discord.gg/legionseries). 

# __General advice and websites recommendation__
* **It's best to do research on how to use Linux instead of jumping ship and expect the same workflow as on Windows. This is one of the many newbie traps!!**
* Don't install packages from the internet unless necessary. Always trust your **SOFTWARE/PACKAGE MANAGER** bundled with your distribution.
* Don't jump the distrohop wagon whenever a new shiny distribution hits the market with niche benefits. Many of those benefits are very negligible and only harm the Linux ecosystem by fragmenting it even further. Use distributions that are popular, mainstream, well-known and come from reputable sources. You can game on any distro and apply the same tweaks on a "non-gaming" distribution.
* Don't rely on custom kernels to give you significant performance gains. Using the kernel bundled with your distribution is more than enough.
* Don't run scripts that claim to give you more performance, especially if they were not tested or come from a untrusted source/maintainer. Those are the equivalent of running registry tweaks on windows to get free fps (aka a scam.)
* Don't rely too much on AI tools to debug your problems, unless you know and read carefully what it gives you instead of blindly copy-pasting. You will have a hard time.
  
To check if your games work on linux, these websites will help you keep yourself updated:   
https://areweanticheatyet.com/<br>
https://www.protondb.com/<br>
https://appdb.winehq.org/
### Websites for linux news (desktops, distributions etc)
https://9to5linux.com/<br>
https://gamingonlinux.com/
###
<br>

# __Distribution recommendation__
Based on my own experience + community feedback. <br> Treat this as a way to begin your Linux journey. These are mainstream, well-known, supported linux distributions with huge user-bases and documentation.
| Name | Pros | Cons | Links |
| ------------- | ------------- | ------------- | ------------- |
| **[Fedora](https://fedoraproject.org/)** | • Comes with GNOME or KDE Plasma by default, alongside multiple desktop flavors.<br>• Provides a near-vanilla Linux desktop experience.<br>• Up-to-date drivers with strong focus on stability.<br>• Excellent documentation and large community support.<br>• Security-focused defaults.<br>• Semi-rolling release model. | • Nvidia drivers and codecs require manual setup.<br>• Secure Boot setup requires manual signing post-install. | [Post-Install Guide](https://github.com/Tenama-hub/Linux_guide_for_Legion/blob/main/fedora_post_install_guide.md) |
| **[OpenSUSE Tumbleweed](https://www.opensuse.org/)** | • Ships with GNOME or KDE Plasma by default.<br>• Rolling-release distro with strong stability focus.<br>• Secure Boot configured by default.<br>• Includes Snapper for easy system rollback after bad updates.<br>• Excellent hardware package optimizations.<br>• Available in both rolling-release (Tumbleweed) and LTS (Leap) variants.<br>• Strong documentation. | • Nvidia drivers and codecs require manual setup.<br>• YaST/sysadmin tools may feel overwhelming for beginners.<br>• The installer can sometimes bork itself, pre or post-install. The network install ISO seems to work better in this regard. | [Post-Install Guide](https://youtu.be/0T02xd9qVmM?si=_op_kdpDzYjRkK5F) |
| **[Kubuntu](https://kubuntu.org/)** | • Ships with KDE Plasma by default. <br>• Secure Boot configured by default.<br>• Minimal install skips snaps (if you are interested in that) <br>• Huge documentation, inherits Ubuntu's popularity.<br>• Available in both non-LTS or LTS. <br>• Everything works out of the box. | • Non-LTS variants aren't as "stable" as the LTS counterpart. <br> • Inherits Ubuntu's choices, but it's not that big of a deal. | [Post-Install Guide](https://github.com/Tenama-hub/Lenovo_Legion_Linux-Guide/blob/main/ubuntu%26kubuntu_post_install_guide.md) |
| **[Linux Mint](https://linuxmint.com/)** | • Comes with Cinnamon as the primary desktop environment (Other editions offer XFCE/MATE).<br>• Ships with many useful tools pre-installed.<br>• Cinnamon edition supports customizable touchpad gestures.<br>• Stable release model focused on reliability. | • Uses older package bases and technologies, which may affect newer hardware support.<br>• Still relies on X11, which is behind certain modern features (dual screens may not work as intended for example).<br>• Secure Boot setup requires manual signing post-install. | [Post-Install Guide](https://github.com/Tenama-hub/Linux_guide_for_Legion/blob/main/linux_mint_post_install_guide.md) |

If you feel adventurous...<br> Try out these distributions that are highly praised by the Linux community.
| Name | Pros | Cons | Links |
| ------------- | ------------- | ------------- | ------------- |
| **[Bazzite](https://bazzite.gg/)** | • Comes with Plasma/Gnome by default<br>• Pre-installed Steam, Nvidia drivers and codecs<br>• Can be used for any use case, not just gaming<br>• Great alternative to SteamOS<br>• Very hard to break and requires little to no maintenance due to its "atomic" nature<br>• Atomic distribution based on Fedora. Updates can be done in the background and are relatively quick | • Apps can only be installed as Flatpaks, AppImages, HomeBrew or through Distrobox/Kontainer.<br>• You cannot do system-level changes like on traditional distros, unless you create your own fork of the project.<br>• Support outside their official Discord leaves more to be desired.<br>• No secure boot post-install. Needs to be signed manually (can be done through Ujust) <br> • Uses more power on idle than other distros (could be a bug) | [Post-Install Guide](https://docs.bazzite.gg/General/Installation_Guide/post-installation/) |
| **[EndeavourOS](https://endeavouros.com/)** | • Comes with Plasma by default. Can install a different desktop environment during the installation process (same for the bootloader)<br>• Pure Arch Linux experience, with several tools and tuning done to get you up and running<br>• Bleeding edge distribution based on Arch Linux, which means you will get frequent updates<br>• Nvidia drivers pre-installed<br>• Great documentation & community | • More terminal focused, as it doesn't come bundled with a GUI package manager.<br>• Updates can go bad due to it's bleeding edge nature and you will experience several bugs here and there.<br>• AUR isn't the safest place to get your packages from.<br>• Requires prior linux knowledge in order to properly use it. Not suitable for newbies or for production environments.<br>• No secure boot post-install. Needs to be signed manually. | |
| **[CachyOS](https://cachyos.org/)** | • Comes with Plasma by default. Can install a different desktop environment during the installation process (same for the bootloader)<br>• Pre-configured snapshots in case updates go bad (If you choose BTRFS+Limine by default)<br>• One-click install for gaming packages (Steam, Lutris, Heroic, Mangohud with Goverlay + libraries needed) + nvidia drivers pre-installed<br>• A functional software center that allows installing AUR and Flatpaks<br>• Bleeding edge distribution based on Arch Linux, which means you will get frequent updates<br>• Optimized for your hardware, meaning you can get a boost in performance<br>• Great documentation | • "Optimizations" can be a hit or miss on some scenarios.<br>• Updates can go bad due to it's bleeding edge nature and you will experience several bugs here and there.<br>• AUR isn't the safest place to get your packages from.<br>• Requires prior linux knowledge in order to properly use it. Not suitable for newbies or for production environments.<br>• No secure boot post-install. Needs to be signed manually. | [Post-Install guide](https://wiki.cachyos.org/configuration/post_install_setup/) |

# __Distributions to avoid__
| Name | Reason |
| ------------- | ------------- |
| **Debian (stable branch)** | Unless you use Debian Sid/testing, updates are released very slowly and packages tend to get outdated pretty quick. |
| **Pop!_OS** | The new Cosmic desktop variant lacks critical fixes and it is still currently in alpha. For now, there are better options. |
| **Ubuntu** | A lot of decisions are tailored for enterprise solutions + [pushing for AI](https://www.zdnet.com/article/ubuntu-26-04-is-os-for-ai-agentic-era-says-canonical-mark-shuttleworth-why/). Snap packages are okay, but some apps aren't 100% officially supported and come with their own issues (especially if you remove snap support on Ubuntu. Kubuntu and the derivatives can safely remove snaps.)|
| **SteamOS** | Doesn't have an nvidia alternative and is not finished for **non-handheld devices**. If you REALLY need something similar, use Bazzite. |
| **Manjaro** | It's future is uncertain as it has a history of a lot of wrongdoings, strange decisions and updates that led to broken systems or significant bugs. Was on a hiatus due to [disagreements and developers being on strike](https://forum.manjaro.org/t/manjaro-2-0-manifesto/186171). There are much better options out there. |
| **ZorinOS** | The development team is basically 2 main developers + community contributions, demands money for custom desktop layouts. Gets a lot more outdated compared to the other Ubuntu-based distributions. Not worth your time (at that point, just use Ubuntu) |
| **Hacking/Cybersecurity distributions** | Parrot, Tails, Kali Linux and alike are meant to be used either through VMs or external devices, not on actual hardware. |
| **Obscure/outdated distributions** | Avoid distributions maintained by randoms/single developer, that are **"too good to be true"** (nonsense promises) or try to replicate Windows 1:1. |
| **Hobby/niche distributions** | Do keep in mind you won't have any guarantee they won't die off in the future or have proper support outside their forums (forums being just a Discord server). They also come with problems of their own, such as: unorthodox way of handling packages (some packages are updates often more than others, for example), low-quality in-house tools, kernel problems, questionable community, low amount of maintainers etc. <br> Some example of such distros are **Nobara, RegataOS, Garuda, PikaOS** etc. |
###
<br>

# __Desktop environments (DE)__
Linux does not have a single desktop experience. There are plenty of them, each with their own pros, cons & querks. This part of the guide should give a brief summary or the most popular desktop environments that are provided by default on almost all distributions out there. <br>
For the tech nerds, I will **not** cover window managers. <br>
Based on my own experience + community feedback.
| Name | Pros | Cons |
| ------------- | ------------- | ------------- |
| [**KDE Plasma**](https://kde.org/plasma-desktop/) | <br>• Provides a Windows-like desktop experience. <br>• Highly customizable OOTB + plenty of plugins in [KDE Store](https://store.kde.org/browse/). <br>• Has the most development for gaming & general use than other desktops. <br>• Not very taxing on hardware resources <br>• Is updated pretty regularly. | <br>• Settings can feel overwhelming & get easily lost. <br>• Some of the default apps are pretty average. <br>• Bugs & stability issues may occur (although very rare nowadays.) |
| [**Gnome**](https://www.gnome.org/) | <br>• Provides a MacOS-like experience, fixated on simplicity. <br>• [Has plenty of extensions](https://extensions.gnome.org/) to customize your desktop environment. <br>• Default apps are beautifully designed & has the best animations (hands down) <br>• Not very taxing on hardware resources (by default) <br>• Is updated every ~6 months. | <br>• Extensions can break on desktop updates. <br>• Certain quirks & bugs can be off-putting for some users. <br>• Some settings are behind certain 3rd party apps. <br>• Inconsistency with some non-gnome apps. <br>• Is very opinionated. | 
| [**Cinnamon**](https://en.wikipedia.org/wiki/Cinnamon_(desktop_environment)) | <br>• Provides a Windows 7/10 like experience, based on Gnome <br>• Default apps are simple & easy to use for fresh converts. <br>• Touchpad gestures for laptop users. <br>• Has its fair share of customization + [Plugin store](https://cinnamon-spices.linuxmint.com/extensions)  | <br>• Still based on X11, which is legacy at this point. <br>• Plugin store is quite lacking compared to Plasma/Gnome offerings. <br>• Is updated yearly (not a really big con, considering Linux Mint's stable nature) | 
| [**XFCE**](https://xfce.org/) | <br>• Provides a Windows(XP/7)-like experience. <br>• Is very basic & fast (lacks animations by default) <br>• Pretty customizable, considering it's very minimalist nature. <br>• Default apps are simple & easy to use <br>• Runs on pretty much any hardware & has very low hardware requirements. | <br>• Customization is quite lacking + doesn't offer a plugin store. <br>• Doesn't have the same gaming/general use tweaks like Plasma/Gnome. <br>• Is updated once in a blue moon (not a really big con, depending on your perspective). |
| [**Cosmic**](https://system76.com/cosmic) | <br>• Provides a MacOS-like experience. <br>• Developed for performance, productivity and gaming in mind. <br>• Has its fair share of customization options. <br>• Default apps are pretty good (a combination of Gnome's simplicity & Plasma's usability). <br>• Is updated regularly. | <br>• Still not finished & in alpha. Has a lot of bugs that affect daily usage. <br>• Lack of customization outside their offerings (for now...) |
###
<br>

# __Installing Legion tools and drivers (LEGACY)__ 
> [!WARNING]
> As of Kernel 6.17, power profiles switching and battery conservation don't require the Legion Driver. Kernel 7.1 and up should introduce native fan control too.\
> This driver is now marked as LEGACY, due to it being slowly introduced with each kernel update. Tools that depend on this driver may no longer work.

This allows you to use most, if not all the legion exclusive features on linux (fan control, panel overdrive, etc). Comes with a GUI to easily access these said features.   
If you use Plasma and you want to have a tool that gives you the important options at a glance, I recommend using [PlasmaVantage](https://gitlab.com/Scias/plasmavantage) or Cinnamon's inspired counterpart from the [desktop plugin store](https://cinnamon-spices.linuxmint.com/applets/view/395)   
## Distro packages (highly recommended)
These packages are maintained by the community.
| Distribution | Links |
| ------------- | ------------- |
| Debian/Ubuntu | https://github.com/MrDuartePT/pacstall-programs/tree/lll-repo |
| Fedora | https://copr.fedorainfracloud.org/coprs/mrduarte/LenovoLegionLinux/ \| [Alternate link](https://mrduartept.github.io/LLL-pkg-repo) |
| Arch Linux | [lenovolegionlinux-git](https://aur.archlinux.org/packages/lenovolegionlinux-git) \| [lenovolegionlinux-dkms-git](https://aur.archlinux.org/packages/lenovolegionlinux-dkms-git) |
| Gentoo | [GURU Overlay](https://gitweb.gentoo.org/repo/proj/guru.git) \| [ebuild](https://gpo.zugaina.org/sys-firmware/lenovolegionlinux) |
| NixOS | https://search.nixos.org/packages?channel=unstable&from=0&size=50&sort=relevance&type=packages&query=lenovo-legion |
## Manual Install Module
The project's [github page](https://github.com/johnfanv2/LenovoLegionLinux?tab=readme-ov-file#bulb-instructions) should give you enough instructions to aid you in the process.\
After it's done, to check if module is built and installed correctly, enter the following command
```sudo lsmod |grep legion_laptop```\
The output should show that legion_laptop and platform profile modules are loaded.
###
<br>

# __App & Tools recommendation__
| App  | Description |
| ------------- | ------------- |
| [Bazaar](https://flathub.org/en/apps/io.github.kolunmi.Bazaar) | Front-end for managing Flatpak packages, if your distribution's package manager app is not good enough for this use case. Used by default on Bazzite. |
| [Retrodeck](https://flathub.org/en/apps/net.retrodeck.retrodeck) | An all-in-one emulation front-end that ships with the most popular emulators. You can configure and add BIOS files for each component through its configurator app. |
| [EasyEffects](https://flathub.org/en/apps/com.github.wwmm.easyeffects) | Front-end equalizer for managing your microphone and speakers. Useful for filtering microphone background noise and improving overall audio quality. |
| [Warehouse](https://flathub.org/en/apps/io.github.flattool.Warehouse) | All-in-one Flathub package manager for installing Flatpaks, deleting leftover data, and managing Flatpak data. A more technical alternative to Bazaar. |
| [Flatseal](https://flathub.org/en/apps/com.github.tchx84.Flatseal) | Manage Flatpak permissions. Especially useful on non-KDE Plasma distributions. |
| [Gear Lever](https://flathub.org/en/apps/it.mijorus.gearlever) | Front-end AppImage manager that allows installing and managing AppImage packages without manually handling them in the file manager. |
| [PeaZip](https://flathub.org/en/apps/io.github.peazip.PeaZip) | A powerful and user-friendly alternative to WinRAR and 7-Zip for archive management. |
| [WinBoat](https://www.winboat.app/)  | A powerful app that allows running Windows apps through a VM that seamlessly integrates with your system. The VM is lightweight and easy to configure. It (currently) does not support GPU pass-through, so GPU accelerated apps (including games) will not run or will run but slower. | 
###
<br>

# __Battery saving tools__
The tool that comes bundled with your distribution of choice should be good enough. For advanced users only!
> [!WARNING]
> Some of the tools will not work together with the rest (exceptions may apply). Make sure you remove all the tools besides the one you want to currently use.\
> Do **NOT** use configuration files from laptops you don't **OWN**. This may cause severe issues with your hardware! You have been warned.

| Tool | Description |
| ------------- | ------------- |
| [Tuned](https://github.com/redhat-performance/tuned) | A mix between Power Profiles Daemon and TLP. Easily integrates with desktop environments that support power profile switching and can be customized to your needs. Used by default on Fedora and Bazzite. |
| [Power Profiles Daemon](https://gitlab.freedesktop.org/upower/power-profiles-daemon) | Default power profile management service used by most Linux distributions. Works well with `pstate` CPU scaling and most hardware configurations. Simpler than TLP, but effective for general usage. Conflicts with most other power management tools except Powertop. |
| [TLP](https://linrunner.de/tlp/index.html) | Advanced power management tool that applies extensive optimizations depending on whether the system is running on battery or AC power. Highly configurable, but incorrect setup can cause issues. Conflicts with other power management tools. GUI frontend available through [TLPUI](https://github.com/d4nj1/TLPUI). |
| [Auto-Cpufreq](https://github.com/AdnanHodzic/auto-cpufreq) | Lightweight automatic CPU power optimization tool that dynamically adjusts CPU scaling and governors based on battery or AC status. Works well with `pstate`, though some hardware may experience compatibility issues. |
| [Powertop](https://wiki.archlinux.org/title/Powertop) | Terminal-based power analysis and tuning utility for monitoring system power consumption and enabling hardware power-saving optimizations. Best used for diagnosing power draw, since most automatic optimizations are already handled by other tools. |
###
<br>

# __Wine front-ends__
[Wine](https://www.winehq.org/) is a special tool that allows running Windows apps in Linux. This sparked the creation of proton, that is actively used for games.
| App | Description |
| ------------- | ------------- |
| [Lutris](https://lutris.net/) | Unified game and application launcher for Linux that supports installing, configuring, and managing games from multiple sources. Features community installation scripts and library imports from Steam, GOG, and Epic Games Store. Avoid using installer scripts, as many still rely on outdated Wine-GE runners. |
| [Heroic Games Launcher](https://heroicgameslauncher.com/) | Open-source launcher for managing games from Epic Games Store, GOG, Amazon Games, Humble Bundle, Ubisoft Connect, Origin, and local backups. Includes built-in Wine and Proton management tools. |
| [Faugus Launcher](https://github.com/Faugus/faugus-launcher) | Lightweight and easy-to-use launcher built around UMU. Less feature-rich, but provides a simpler and more straightforward experience without unnecessary complexity. |
| [Port-Proton](https://github.com/Castro-Fidel/PortWINE) | User-friendly launcher focused on simplifying Wine game setup and launcher installation. Includes a custom prefix with preinstalled .NET frameworks and various configuration tools. It has some usability limitations, slower startup times, and fewer advanced customization options compared to alternatives. Best used as a fallback option. |
###
<br>

# __General bugs and fixes__
<details>
<summary>Fix games stuttering/lagging/bugging out only on Legions</summary>
  
Some legion hardware have a problem where some games will randomly stutter or lag more than other devices with the same specs. This is caused by [HPET](https://en.wikipedia.org/wiki/High_Precision_Event_Timer). To check if you have it enabled, run this command: \
`cat /sys/devices/system/clocksource/clocksource0/current_clocksource` \
If it shows HPET, then you will have to change it to TSC. Check if you have it: \
`cat /sys/devices/system/clocksource/clocksource0/available_clocksource` \
If it doesn't show up, you will have to do the following: \
1. Use a Kernel that patches TSC (Like CachyOS's kernel)
2. Patch it automatically to your current kernel by [using this patch](https://github.com/CachyOS/linux-cachyos/issues/925).

After you did one of the two, you will have to add `tsc=directsync` in your bootloader.

Even if you have TSC enabled and your games have dubious anomalies, give this one a try. (for example: Risk of rain 2 exaggerated loading times/audio stuttering, Death stranding stuttering/sped up animations, games have crackling in audio or lesser fps than the usual)

</details>

<details>
<summary>Fix laptop speakers not working (Gen 10 Legions)</summary>
  
* You will need [this special driver](https://github.com/marco-giunta/legion-pro7-gen10-audio), until it gets pushed in the kernel.

</details>

<details>
<summary>System swappiness (if you have >= 16GB ram)</summary>
  
* Setting your swappiness to 10 will reduce stuttering when your RAM memory is almost full, as the system will not prioritize using your SWAP partition as system memory for apps.<br>
 ```sudo nano /etc/sysctl.conf```
* Add ```vm.swappiness=10``` Then save. (ctrl+O then hit enter)
</details>
<details>
<summary>Zram tweaks</summary>

**This should be already tweaked by the majority of mainstream distributions.** <br>
* (Make sure your distribution has zram enabled by running ```zramctl``` in the terminal!)
* If you have games crashing due to memory leaks, tweaking zram would help ameliorate the problem. To do so, do the following: <br>
 ```sudo nano /etc/systemd/zram-generator.conf```
* Inside the new configuration file, paste this:   
```[zram0]```\
```compression-algorithm=zstd```\
```zram-size = min(ram / 2, 16384)```
* Save & Reboot. What this does is it tweaks zram to compress half of your total ram. While it will fix games crashing due to low ram, it will also add a little performance hit. It shouldn't be noticable at all.
</details>
<details>
<summary>Bad speakers quality</summary>

* If your speakers sound shallow and bad, try out [this preset](https://github.com/Tomiscout/Lenovo-Legion-5-Pro-Linux-guide/tree/main/easyeffects). If you use handhelds, [better give this one a try](https://www.reddit.com/r/LegionGo/comments/1m7632y/legion_go_s_steam_os_audio_fix_pipewire_eq/).
* If you don't want to use Easyeffects for your legion laptop, download & extract the pipewire archive in .config, open convolver-sink.conf and change YOURUSERNAME with your linux's username. This method may cause issues with external speakers, so be wary!<br>
  **Restart pipewire and change your sound profile in settings!**
</details>
<details>
<summary>Bad laptop mic quality</summary>

* Set your microphone volume to 30-50%, then install this [noise cancelling module](https://github.com/Rikorose/DeepFilterNet/blob/main/ladspa/README.md) or use EasyEffects\NoiseTorch.
</details>



<details>
<summary>Refresh rate/ VRR not working</summary>
  
* Some screen panels will force you to use either the highest or the lowest refresh rate (even keep you at the highest resolution). Edid.bin tells your screen what resolutions and refresh rates it supports. This is a problem that affects some panels due to generic drivers being used instead of the ones provided by the screen providers.
1. In WINDOWS, download the CRU tool. Open it, then click on **EXPORT**. Save the file as edid.bin. (Make sure that you can see your refresh rates in Windows too. Otherwise, add them by yourself, then
2. Copy the file to a usb drive and boot back to linux.
3. Open a terminal and type the following commands:
```cd /lib/firmware && sudo mkdir edid && sudo cp (path to file)/edid.bin /lib/firmware/edid```
4. To make sure your edid file is recognized, use the following:   
```for p in /sys/class/drm/*/status; do con=${p%/status}; echo -n "${con#*/card?-}: "; cat $p; done```
   
For the below commands, replace **{display_id}** with the output of the connected display from the command in number 4.

| Name | Command |
|-------------|-------------|
| **systemd-boot** | `sudo kernelstub -a 'drm.edid_firmware={display_id}:edid/edid.bin'` |
| **GRUB** | `sudo nano /etc/default/grub`<br>Add `drm.edid_firmware={display_id}:edid/edid.bin` to `GRUB_CMDLINE_LINUX_DEFAULT`<br><br>Then run one of the following:<br>`sudo update-grub`<br>OR<br>`sudo grub2-mkconfig -o /boot/grub2/grub.cfg` |

  
Reboot. <br>
For Immutable/atomic distros based on Fedora( e.g. Bazzite), use the following (make sure you replace {display_id} with the output from number 4, as well as path-to-file with the actual path): \
`sudo mkdir -p /etc/firmware/edid`<br>`sudo cp (path-to-file)/edid.bin /etc/firmware/edid`<br>`sudo rpm-ostree kargs --append-if-missing=drm.edid_firmware={display_id}:edid/edid.bin`<br><br>**In case it hasn't fixed yet, run these 2 as well:**<br>`sudo echo 'install_items+=" /etc/firmware/edid/edid.bin "' | sudo tee /etc/dracut.conf.d/edid.conf`<br>`sudo rpm-ostree kargs --append-if-missing=firmware_class.path=/etc/firmware`

If you switch between hybrid and dedicated mode, you may encounter issues with your display. This can be fixed by adding the other display (run step 4) in the edid firmware variable like so (replace display_id with your current display id in hybrid and display_id_2 with the display id in dedicated graphics): \
```drm.edid_firmware={display_id}:edid/edid.bin,{display_id_2}:edid/edid.bin``` \
If none of these commands/variables work, you will have to also add ```video={display_id}:e```.
</details>


> [!WARNING]
> UNDER NO CIRCUMSTANCE, DO NOT INCREASE/DECREASE THE RESOLUTION OF YOUR SCREEN/REFRESH RATE PAST YOUR SPECS! DOING SO WILL CAUSE SEVERE ISSUES!
