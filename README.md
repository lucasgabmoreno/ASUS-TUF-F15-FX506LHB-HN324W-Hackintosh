# ASUS TUF F15 FX506LHB HN324W - Hackintosh

- OpenCore x.x.x
- MacOS 11.3 Big Sur ~ 13.x Ventura
- 
### Working
- iGPU Intel Core i5-10300H Comet Lake
- Wifi & BT Broadcom BCM94350ZAE / DW 1820A
- Audio ALC256 (alcverbs=1 alcid=?)
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

## Solutions

### Wifi not working?
1. Press power button at least 30 seconds
2. Reboot

### 5Ghz wifi signal not detected?
1. Get into your rooter (192.168.0.1)
2. If your 5Ghz wifi signal channel is 36, change it to 40.

