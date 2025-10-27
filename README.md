# Garbware-Hackintosh
Collection of personal references for restoring Mac's with Linux
> I would recommend fedora spins for this because immutability with proprietary drivers is just better.

To check your chip in live env `lspi | grep "Apple Inc."`

## Restoring T2 Macbook Pro 15,1 (Also applies to many of late 2017 to 2020 releases) 

Followed disk partitionning step from MacOS. 

Made the ISO following: [T2Fedora-Repo](https://github.com/t2linux/fedora-iso)
In the live env Wi-Fi worked out of the box, props to the devs. 

Followed initial WiFi instructions to copy to EFI firmware, but I don't even think you really need to [T2-Wiki](https://wiki.t2linux.org/guides/wifi-bluetooth/)
Also had to go into into a TTY: and use `sudo localectl set-x11-keymap fr` for keymap to work with SDDM login screen. 

But then post install wifi was gone again because, I'm an idiot and deleted everything from the Mac OS partitions.

### WIFI/BT

Luckily I tethered USB internet from my phone and used https://wiki.t2linux.org/guides/wifi-bluetooth/#__tabbed_2_5 **Method 5.** 
> Funnily enough uses a script from: https://github.com/kholia/OSX-KVM

Also the method is to curl https://wiki.t2linux.org/tools/firmware.sh

Then `./firmware` where the script was downloaded and pick is actually nbr `3`. A bit confusing. Then I picked option 4 for Big Sur and it downloads the system and extracts the Wifi/Bluetooth support.

Most impressive part is that touchbar also works out of the box. Almost just like the original design. 

## Apple Silicon (M1/M2/M3/M4):

Asahi Linux (usually fedora related) project - https://asahilinux.org

And for arch (more manual) - https://asahi-alarm.org/ 

## Regular Intel Macs

Should be much more straightforward. Perhaps just a few wiki articles for broadcom from your distro package manager.
