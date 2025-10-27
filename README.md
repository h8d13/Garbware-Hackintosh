# Garbware-Hackintosh
Collection of personal references for restoring Mac's with Linux
> I would recommend fedora spins for this because immutability with proprietary drivers is just better.

To check your chip in live env `lspci | grep "Apple Inc."`

## Restoring T2 Macbook Pro 15,1 FULL-DISK INSTALL (Also applies to many of late 2017 to 2020 releases) 

Followed disk partitionning step from MacOS. 

> ⚠️ Important: Don't delete macOS partitions until WiFi is working post-install, do not do full-disk install or you'll lose the EFI firmware like I did. But here is how to do it regardless...

Combine the ISO pieces from releases:[T2Fedora-Repo](https://github.com/t2linux/fedora-iso) 

`cat name_of_iso_here.iso.* > full.iso`

In the live env Wi-Fi worked out of the box, props to the devs. 

Followed initial WiFi instructions to copy to EFI firmware from [T2-Wiki](https://wiki.t2linux.org/guides/wifi-bluetooth/)

**Please read it better than I did.**

Also had to go into into a TTY: and use `sudo localectl set-x11-keymap fr` for keymap to work with SDDM login screen. 

But then post install wifi was gone again because, I'm an idiot and deleted everything from the Mac OS partitions during Fedora installer.

### WIFI/BT

Luckily I tethered USB internet from my phone and used https://wiki.t2linux.org/guides/wifi-bluetooth/#__tabbed_2_5 **Method 5.** 
> Funnily enough uses a script from: https://github.com/kholia/OSX-KVM

Also the method is to curl https://wiki.t2linux.org/tools/firmware.sh

And make sure to have `sudo dnf install dmg2img`

Then `./firmware.sh` where the script was downloaded and pick is actually nbr `3`. A bit confusing. 

Then I picked option 5 for OS version ``and it downloads the system and extracts the Wifi/Bluetooth support to our new full disk install.

Most impressive part is that touchbar also works out of the box. Almost just like the original design. 

## Apple Silicon (M1/M2/M3/M4):

Asahi Linux (usually fedora related) project - https://asahilinux.org

And for arch (more manual) - https://asahi-alarm.org/ 

## Regular Intel Macs

Should be much more straightforward. Perhaps just a few wiki articles for broadcom from your distro package manager.
