# ASUS TUF F15 FX506LHB HN324W - Hackintosh

- OpenCore x.x.x
- MacOS Catalina ~ Monterey

### Working
- iGPU Intel Core i5-10300H Comet Lake
- Wifi & BT Broadcom BCM94350ZAE / DW 1820A
- Audio ALC256 (alcid=?)
- LAN Realtek RTL8168
- Trackpad & Keyboard
- Brightness (keepsyms=1 debug=0x100 -wegnoegpu)

### Not Working
- dGPU NVIDIA GTX 1650 Turing: [Not supported](https://dortania.github.io/GPU-Buyers-Guide/modern-gpus/nvidia-gpu.html#native-nvidia-gpus)
- Wifi & BT Realtek Mediatek MT7921: [Replaced](https://dortania.github.io/Wireless-Buyers-Guide/unsupported.html#supported-chipsets)
- SMBUS: ?

---

## BIOS
1. Into the BIOS (turn on the computer and press F2) change settings to:
   
| Var   | Status |
|:---|:---|
| Secure Boot | Disabled|
| Fast Boot | Disabled |

---

## Install
1. Download [Monterey](https://apps.apple.com/us/app/macos-monterey/id1576738294?mt=12)
2. Open terminal:
```
sudo /Applications/Install\ macOS\ Monterey.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled
```
---

## Post install
Open terminal and disabel Sleep/Wake:
```
sudo pmset autopoweroff 0
sudo pmset powernap 0
sudo pmset standby 0
sudo pmset proximitywake 0
sudo pmset tcpkeepalive 0
```
If you need to fix iCloud Ban/iMessages Ban or WiFi/Ethernet Issues
```
sudo rm /Library/Preferences/SystemConfiguration/NetworkInterfaces.plist
sudo rm /Library/Preferences/SystemConfiguration/preferences.plist
```

---

### Credits

- [RobyRew](https://github.com/RobyRew/ASUS-FX506LHB-Hackintosh_OpenCore#post-installation)
- [Taarkov](https://github.com/taarkov/ASUS-TUF-Gaming-F15-FX-506LH-Hackintosh)
