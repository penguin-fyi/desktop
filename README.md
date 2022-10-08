# The Penguin Desktop

The [Penguin Desktop](https://penguin.fyi) is a light-weight, general-purpose, [X](https://x.org)/[XDG](https://www.freedesktop.org/wiki/Specifications/)/[GTK](https://gtk.org/)-centric  Desktop Environment for [Arch Linux](https://archlinux.org) based on [AwesomeWM](https://awesomewm.org).
 
![Penguin Desktop R15](https://github.com/penguin-fyi/.github/profile/penguin-desktop-15.png) 

## About



### Features

* User-friendly, traditionally styled UI combined with dynamic window tiling
* Equally balanced mouse and keyboard controls with consistent, layered design
* Good selection of default apps (including xed, xreader, xviewer, xplayer from X-Apps)
* Made with real penguins

## Installation
There are currently several ways to install Penguin Desktop.

#### New Install (manual)
Installing Penguin Desktop during a manual Arch Linux installation is the most straight-forward, and therefore most recommended, method. We will not cover the entire Arch Linux install; can read more about that [here](https://wiki.archlinux.org/title/Installation_guide).

**Step 1:** Follow Arch install guide up to ***Select the mirrors***

**Step 2:**  Add the Penguin mirrorlist, by creating `/etc/pacman.d/mirrorlist-penguin`

    Server = https://repo.penguin.fyi/packages/$repo/$arch
    SigLevel = Optional TrustAll

**Step 3:** Add mirrorlist to `/etc/pacman.conf`

    [penguin]
    Include = /etc/pacman.d/mirrorlist-penguin

**Step 4:** Install complete Penguin Desktop

    pacstrap /mnt penguin-base penguin-desktop

**Step 5:** Continue Arch install as usual

#### New Install (archinstall)
Installing Penguin Desktop during Arch installation via `archinstall` is also possible. This method is two part: `archinstall` and `arch-chroot`

##### archinstall:
In this part of the installation, you may setup your system as needed, but the following points are required.

* Do not create **User account**; this will be done later
* For **Profile**; choose **minimal**
* For **Audio**; choose **pipewire**
* For **Network configuration**; choose **NetworkManager**

When the installation is complete, select **Yes** to enter `chroot`

##### arch-chroot:
**Step 1**: Run setup script to add mirrorlist and install 

    curl https://repo.penguin.fyi/setup_mini.sh | sh

**Step 2**: Add **User Account**
	    
	useradd -m username
	passwd username

**Step 3**: Exit `chroot` with `Ctrl+D` and reboot to new system

#### Existing Install [unsupported]

...

#### Via PKGBUILD [unsupported]

...

## Support

To get help with Penguin Desktop, please open an issue on the appropriate repository
| | |
|-|-|
| [pkgbuilds](https://github.com/penguin-fyi/pkgbuilds/issues) | For issues building or installing the packages |
| [awescome-config](https://github.com/penguin-fyi/awesome-config/issues) | For issues with AwesomeWM |
| [desktop-config](https://github.com/penguin-fyi/awesome-config/issues) | For issues with the default desktop configuration (`/etc/skel`) |

Nothing is documented. Maybe [this](https://wiki.archlinux.org/) will help.

