# Garbware-Hackintosh
Collection of personal references for restoring Mac's with Linux

## Restoring T2 Macbook Pro 15,1

Made the ISO following: [T2Fedora-Repo](https://github.com/t2linux/fedora-iso)
In the live env Wi-Fi worked out of the box, props to the devs. 

Followed initial WiFi instructions to copy to EFI firmware, but I don't even think you really need to [T2-Wiki](https://wiki.t2linux.org/guides/wifi-bluetooth/)
Also had to go into into a TTY: and use `sudo localectl set-x11-keymap fr` for keymap to work with SDDM login screen. 

But then post install wifi was gone again becauseI'm an idiot and deleted everything from the Mac OS partitions.
