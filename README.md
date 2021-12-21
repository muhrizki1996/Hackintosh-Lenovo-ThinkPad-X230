# Hackintosh-Lenovo-ThinkPad-X230

[![ThinkPad](https://img.shields.io/badge/ThinkPad-X230-blue.svg)](https://psref.lenovo.com/syspool/Sys/PDF/withdrawnbook/ThinkPad_X230.pdf)
[![MacOS High Sierra](https://img.shields.io/badge/High_Sierra-10.15-red.svg)](https://www.apple.com/)
[![MacOS Mojave](https://img.shields.io/badge/Mojave-10.14-red.svg)](https://www.apple.com/)
[![MacOS Catalina](https://img.shields.io/badge/Catalina-10.15-red.svg)](https://www.apple.com/)
[![MacOS BigSur](https://img.shields.io/badge/Big_Sur-11.5-red.svg)](https://www.apple.com/)
[![MacOS Monterey](https://img.shields.io/badge/Monterey-12.1-red.svg)](https://www.apple.com/)
[![Release](https://img.shields.io/badge/Download-latest-brightgreen.svg)](https://github.com/muhrizki1996/Hackintosh-Lenovo-ThinkPad-X230/releases/latest)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.7.1-blue.svg)](https://github.com/acidanthera/OpenCorePkg/releases/latest)

This is my complete EFI folder to be used for hackintosh on Lenovo ThinkPad X230 notebook with multibooting:
- macOS High Sierra 10.13.x
- macOS Mojave 10.14.x
- macOS Catalina 10.15.x
- macOS Big Sur 11.x
 
<img src="/img/Screenshot.png?raw=true" alt="macOS Screenshot" align="center">
 
> ## How to Get
- Clone whole repo: $ `git clone https://github.com/muhrizki1996/Hackintosh-Lenovo-ThinkPad-X230`
- Download [Specific Folder](https://minhaskamal.github.io/DownGit/#/home) only.
 
> ## Notebook Specs
<img src="/img/Lenovo-ThinkPad-X230.png?raw=true" alt="Lenovo ThinkPad X230" align="right" width="433" height="325">

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
- [x] <b>BIOS</b>: 2.51
 
> ## EFI Contains
- [x] <b>OpenCore binary, config.plist</b>, drivers for uefi, themes, etc..
- [x] <b>Patched ACPI Tables (DSDT-SSDT)</b> for Audio, Sleep, etc..
- [x] <b>3rd party kexts</b> for working devices under macOS High Sierra (10.13), macOS Mojave (10.14), and macOS Catalina (10.15)
 
<details>
<summary><strong> What's Worked </strong></summary>
<br>

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| QE/CI Enabled Graphics               | ✅   | OpenCore Inject + WhateverGreen.kext |
| Brightness Adjustments               | ✅   | PNLF DSDT Patch + WhateverGreen.kext + BrightnessKeys.kext |
| Realtek ALC269 Audio out             | ✅   | HDEF DSDT Patch + AppleALC.kext with Layout ID = 55 |
| Intel Centrino Advanced-N 6205 Dual-Band       | ✅   | Airportitlwm.kext + Force IO80211Family.kext on OpenCore |
| Intel 82579LM Gigabit Network Connection | ✅   | IntelMausi.kext |
| Broadcom BCM20702A0 Bluetooth        | ✅   | BlueTooth.kext (not working on macOS Monterey) |
| Synaptics TouchPad + Track Point     | ✅   | VodooPS2Controller.kext |
| Multimedia Keys                      | ✅   | BrightnessKeys.kext + [YogaSMC](https://github.com/zhen-zen/YogaSMC) |
| Battery Indicator                    | ✅   | ECEnabler.kext |
| WebCam                               | ✅   | Native + UVC2FaceTimeHD.kext for spoofing UVC WebCams as FaceTime HD (not working on macOS Big Sur and newer) |
| USB2.0 Port + USB 3.0 Port           | ✅   | USBPorts.kext |
| Sleep and Wake                       | ✅   | DSDT + SSDT Patch |
| Mac App Store Access                 | ✅   | Native |
| iMessage and FaceTime                | ✅   | if you are using MLB and ROM from original Macs |
| Hand Off                             | ✅   | Native |
| miniDP Port                          | ✅   | Tested using miniDP to HDMI Adapter |
 
</details>

<details>
<summary><strong> List of Gestures </strong></summary>
<br>

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| 2 Finger Swipe Left                  | ✅   | Forward. |
| 2 Finger Swipe Right                 | ✅   | Backward. |
| 3 Finger Swipe Left                  | ✅   | Right Space/Full Screen apps switch. |
| 3 Finger Swipe Right                 | ✅   | Left Space/Full Screen apps switch. |
| 3 Finger Swipe Up                    | ✅   | Toggle Full screen Switch. |
| 3 Finger Swipe Down                  | ❌   | Do Nothing (on work progress). |
| 4 Finger Swipe Up                    | ❌   | Do Nothing (on work progress). |
| 4 Finger Swipe Down                  | ❌   | Do Nothing (on work progress). |

</details>
 
<details>
<summary><strong> Not Working </strong></summary>
<br>

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| VGA Ports                            | ❌   | Real macs doesn't have. |
| Builtin SDHC Reader                  | ❌   | Sometimes work, sometimes not. |
| ThinkVantage Button                  | ❌   | Maybe something to do with [YogaSMC](https://github.com/zhen-zen/YogaSMC). |

</details>
 
<details>
<summary><strong> Not Tested </strong></summary>
<br>

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| Express Card Slot                    | ❌   | I don't have one of Express Card. |
| ThinkPad Docking                     | ❌   | I don't have ThinkPad Dock |

</details>
 
> ## Notes

1. macOS versions used are <b>Retail from Mac App Store</b>, using <b>createinstallmedia</b> for USB Installer
2. Please read [banhbaoxamlan README_HARDWARE.md](https://github.com/banhbaoxamlan/X230-Hackintosh/blob/master/Other/README_HARDWARE.md) for BIOS configuration, etc.. and [banhbaoxamlan README_OTHERS.md](https://github.com/banhbaoxamlan/X230-Hackintosh/blob/master/Other/README_OTHERS.md) for Post Install
 
> ## Support

<details>
<summary><strong> Video Tutorials </strong></summary>
<br>

- [Multibooting](https://www.youtube.com/watch?v=vXMNyiEgD6o) Windows, Ubuntu, PhoenixOS & macOS using Clover (UEFI)
- Video demonstration about [Full Graphics Acceleration support](https://www.youtube.com/watch?v=) (QE/CI enabled) under macOS [Soon!].

</details>

<details>
<summary><strong> Credits </strong></summary>
<br>

- [Apple](https://www.apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for all the kexts/utilities that they made.
- [Rehabman](https://github.com/RehabMan) and [Daliansky](https://github.com/daliansky) for the patches and guides and kexts.
- [Dortania](https://github.com/dortania) for for the OpenCore Install Guide.
- [badruzeus](https://github.com/badruzeus) for inspirational Repo and Repo README Layout.
- [banhbaoxamlan](https://github.com/banhbaoxamlan) for inspirational ThinkPad configurations and Repo README Layout.
- [migftw](https://github.com/migftw) for inspirational ThinkPad DSDT and SSDTs.
- [zhen-zen](https://github.com/zhen-zen) for **YogaSMC**.

</details>
