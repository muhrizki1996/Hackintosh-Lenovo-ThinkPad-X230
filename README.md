# Hackintosh-Lenovo-ThinkPad-X230

[![ThinkPad](https://img.shields.io/badge/ThinkPad-X230-blue.svg)](https://psref.lenovo.com/syspool/Sys/PDF/withdrawnbook/ThinkPad_X230.pdf)
[![MacOS Catalina](https://img.shields.io/badge/Catalina-10.15-red.svg)](https://www.apple.com/)
[![MacOS Big Sur](https://img.shields.io/badge/Big_Sur-11.4-blue.svg)](https://www.apple.com/macos/big-sur/)
[![MacOS Monterey](https://img.shields.io/badge/Monterey-12.0-purple.svg)](https://www.apple.com/macos/monterey-preview/)
[![Release](https://img.shields.io/badge/Download-latest-brightgreen.svg)](https://github.com/muhrizki1996/Hackintosh-Lenovo-ThinkPad-X230/releases/latest)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.7.1-blue.svg)](https://github.com/acidanthera/OpenCorePkg/releases/latest)

This is my complete EFI folder to be used for hackintosh on Dell Inspiron 14-3442 notebook with multibooting:
- macOS High Sierra 10.13
- macOS Mojave 10.14
- macOS Catalina 10.15
 
<img src="/img/Screenshot.png?raw=true" alt="macOS Screenshot" align="center">
 
### How to Get
- Clone whole repo: $ `git clone https://github.com/muhrizki1996/Hackintosh-Lenovo-ThinkPad-X230`
- Download [Specific Folder](https://minhaskamal.github.io/DownGit/#/home) only.
 
--------------------------------------------------------------------------------------------
 
### Notebook Specs
<img src="/img/Lenovo-ThinkPad-X230.png?raw=true" alt="Dell Inspiron 14-3442" align="right" width="433" height="325">

- [x] <b>Model</b>: Lenovo ThinkPad X230
- [x] <b>CPU</b>: Intel i5-3210M (3) @ 2.50GHz (3rd Gen)
- [x] <b>Chipset</b>: Intel® QM77 Express Chipset
- [x] <b>GPU</b>: Intel HD Graphics 4000 @ 1GB
- [x] <b>RAM</b>: 4GB DDR3 @ 1333MHz (upgrade to 8GB DDR3L @ 1600Mhz)
- [x] <b>Storage</b>: 320GB SATA HDD @ 7200rpm (GUID Partition Table) (upgrade to 120GB SATA SSD)
- [x] <b>Audio</b>: Realtek ALC269 HD Audio Controller
- [x] <b>Wifi</b>: Intel Centrino Advanced-N 6205 Dual-Band
- [x] <b>Ethernet</b>: Intel 82579LM Gigabit Network Connection
- [x] <b>Bluetooth</b>: Broadcom BCM20702A0
- [x] <b>Others</b>: 1 USB 2.0 ports, 2 USB 3.0 ports Synaptics PS/2 TouchPad + Track Point, VGA port, Mini Display port, WebCam, 12.5" 16:9 HD (1366x768) TN Panel, Express Card Slot, 3.5mm Combo Headphone Jack, (SD/ MS/ MS Pro/ MMC) Card Reader, 6/9-Cell @5.6Ah/8.4Ah Lithium-ion Battery
- [x] <b>BIOS</b>: 
 
--------------------------------------------------------------------------------------------
 
### EFI Contains
- [x] <b>OpenCore binary, config.plist</b>, drivers for uefi, themes, etc..
- [x] <b>Patched ACPI Tables (DSDT-SSDT)</b> for Audio, Sleep, etc..
- [x] <b>3rd party kexts</b> for working devices under macOS High Sierra (10.13), macOS Mojave (10.14), and macOS Catalina (10.15)
 
--------------------------------------------------------------------------------------------
 
### What Worked
- [x] QE/CI Enabled Graphics, 1366x768 @ 60MHz Native Display resolution
- [x] ACPI Display brightness with hot keys / slider (PNLF DSDT Patch + WhateverGreen.kext + BrightnessKeys.kext)
- [x] Realtek ALC269 Audio out (HDEF DSDT Patch, with Lilu + AppleALC)
- [x] Intel Centrino Advanced-N 6205 Dual-Band (Airportitlwm.kext + Force IO80211Family.kext on OpenCore)
- [x] Intel 82579LM Gigabit Network Connection (IntelMausi.kext)
- [x] Broadcom BCM20702A0 Bluetooth (BlueTooth.kext)
- [x] Synaptics TouchPad + Track Point (VodooPS2Controller.kext)
- [x] Multimedia Keys (BrightnessKeys.kext + [YogaSMC](https://github.com/zhen-zen/YogaSMC))
- [x] Battery Indicator (ECEnabler.kext)
- [x] WebCam (works OOB + UVC2FaceTimeHD.kext for spoofing as FaceTime HD)
- [x] USB2.0 Port + USB 3.0 (USBPorts.kext)
- [x] Sleep and Wake (DSDT + SSDT Patch)
- [x] Mac App Store Access.
- [x] iMessage and FaceTime (if you using MLB and ROM from original Macs)
- [x] Hand Off

--------------------------------------------------------------------------------------------

### List of Gestures
- [X] 2 Finger Swipe Left = Forward
- [X] 2 Finger Swipe Right = Backward
- [X] 3 Finger Swipe Left = Right Space/Full Screen apps switch
- [X] 3 Finger Swipe Right = Left Space/Full Screen apps switch
- [X] 3 Finger Swipe Up = Toggle Full screen Switch
- [X] 3 Finger Swipe Down = Do Nothing (on work progress)
- [X] 4 Finger Swipe Up = Do Nothing (on work progress)
- [X] 4 Finger Swipe Down = Do Nothing (on work progress)

--------------------------------------------------------------------------------------------
 
### Not Worked / Bugs
- [ ] Builtin SDHC Reader
 
--------------------------------------------------------------------------------------------
 
### Notes
1. macOS versions used are <b>Retail from Mac App Store</b>, using <b>createinstallmedia</b> for USB Installer
2. Please read [banhbaoxamlan Readme](https://github.com/banhbaoxamlan/X230-Hackintosh/blob/master/Other/README_OTHERS.md) for Post Install
 
--------------------------------------------------------------------------------------------

### Video Tutorials
- [Multibooting](https://www.youtube.com/watch?v=vXMNyiEgD6o) Windows, Ubuntu, PhoenixOS & macOS using Clover (UEFI)
- Video demonstration about [Full Graphics Acceleration support](https://www.youtube.com/watch?v=) (QE/CI enabled) under macOS [Soon!].
 
> ## SUPPORT

<details>
<summary><strong> CREDITS </strong></summary>
<br>

- [Apple](https://www.apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for all the kexts/utilities that they made.
- [Rehabman](https://github.com/RehabMan) and [Daliansky](https://github.com/daliansky) for the patches and guides and kexts.
- [George Kushnir](https://github.com/n4ru) for modified BIOS.
- [Dortania](https://github.com/dortania) for for the OpenCore Install Guide.
- [simprecicchiani](https://github.com/simprecicchiani) for inspirational ThinkPad configurations.
- [zhen-zen](https://github.com/zhen-zen) for **YogaSMC**.

</details>
