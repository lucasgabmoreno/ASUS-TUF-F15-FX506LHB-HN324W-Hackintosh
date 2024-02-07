# ASUS TUF F15 FX506LHB HN324W - Hackintosh

- OpenCore x.x.x
- MacOS 11.3 Big Sur ~ 13.x Ventura
  
### Working
- iGPU Intel Core i5-10300H Comet Lake
- Wifi & BT Broadcom BCM94350ZAE / DW 1820A
- Audio ALC256 (alcid 17, 21 and 33 works, 56 and 88 works but low sound at mic)
- LAN Realtek RTL8168
- Trackpad & Keyboard
- Brightness (keepsyms=1 debug=0x100 -wegnoegpu)

### Not Working
- dGPU NVIDIA GTX 1650 Turing: [Not supported](https://dortania.github.io/GPU-Buyers-Guide/modern-gpus/nvidia-gpu.html#native-nvidia-gpus)
- Wifi & BT Realtek Mediatek MT7921: [Replaced](https://dortania.github.io/Wireless-Buyers-Guide/unsupported.html#supported-chipsets)
- Jack microphone

---

## BIOS
1. Into the BIOS (turn on the computer and press F2) change settings to:
   
| Var   | Status |
|:---|:---|
| Secure Boot | Disabled|
| Fast Boot | Disabled |

---

## Solutions

### Wifi not working
1. Press power button at least 30 seconds
2. Reboot

### 5Ghz wifi signal not detected
1. Get into your rooter (192.168.0.1)
2. If your 5Ghz wifi signal channel is 36, change it to 40.

### Sleep/Wake
1. Open terminal and disabel Sleep/Wake:
```
sudo pmset autopoweroff 0
sudo pmset powernap 0
sudo pmset standby 0
sudo pmset proximitywake 0
sudo pmset tcpkeepalive 0
```
2. Go to system preferences and disable sleep/awake

### iCloud Ban/iMessages Ban or WiFi/Ethernet
If you need to fix iCloud Ban/iMessages Ban or WiFi/Ethernet Issues
```
sudo rm /Library/Preferences/SystemConfiguration/NetworkInterfaces.plist
sudo rm /Library/Preferences/SystemConfiguration/preferences.plist
```

---

## Credits
[Olarila](https://www.olarila.com/topic/5676-hackintosh-efi-folder-with-clover-and-opencore/)
