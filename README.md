# ASUS TUF F15 FX506LHB HN324W - Hackintosh

- OpenCore x.x.x
- MacOS Catalina ~ Monterey

### Working
- iGPU Intel Core i5-10300H Comet Lake
- Wifi & BT Broadcom ?
- Audio ALC265 (alcid=?)
- LAN Realtek RTL8168?
- Trackpad & Keyboard
- Brightness (keepsyms=1 debug=0x100 -wegnoegpu)

### Not Working
- dGPU NVIDIA GTX 1650: [Not supported](https://dortania.github.io/GPU-Buyers-Guide/modern-gpus/nvidia-gpu.html#native-nvidia-gpus)
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

## Installer 
1. Download Monterey: https://apps.apple.com/us/app/macos-monterey/id1576738294?mt=12
2. Open terminal:
```
sudo /Applications/Install\ macOS\ Monterey.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled
```
