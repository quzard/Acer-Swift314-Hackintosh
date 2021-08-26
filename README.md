# Acer-Swift314-Hackintosh

## Just for backup

## Specification

| Specifications      | Detail                       |
| ------------------- | ---------------------------- |
| Computer model      | Acer Swift 3 SF314-52 (2018) |
| Processor           | Intel Core i5-8250U          |
| Memory              | 8GB DDR4 2400MHz             |
| Hard Disk           | NVME SN 730                  |
| Integrated Graphics | Intel UHD Graphics 620       |
| Monitor             | FHD 1920x1080 (14 inch)      |
| Sound Card          | Realtek ALC255               |
| Wireless Card       | Swapped with a DW1820A       |
| SD Card Reader      | Realtek                      |

**macOS version**: 11.5.2 (20G95) **OpenCore version**: 0.7.2

## How to use

1. Make your USB installer with [**this guide**](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
2. Clone the repository and paste "BOOT" and "OC" directories into your's pendrive "EFI" folder
3. Download [**GenSMBIOS**](https://github.com/corpnewt/GenSMBIOS) to generate unique SMBIOS information. Run it and select **Generate SMBIOS**, as the model select **MacBookPro15,2**.
4. Open config.plist with [**ProperTree**](https://github.com/corpnewt/ProperTree) and go to PlatformInfo > Generic. Set MLB (Board Serial), SystemSerialNumber (Serial) and SystemUUID (SmUUID) to generated values. Change ROM to your network card's MAC address without the `:` character. [**How to get MAC Address?**](https://www.wikihow.com/Find-the-MAC-Address-of-Your-Computer)
5. Boot it!

## All work

- CPU
- HDMI
- Audio
- USB
- App store, iCloud, iMessage, iTunes, FaceTime, etc
- Sleep, Wakeup, Shutdown, Restart

## HIDPI fix

```
git clone https://github.com/xzhih/one-key-hidpi.git
cd one-key-hidpi
./hidpi.command
```

# Solve the problem of not being able to add applications to "Privacy-Accessibility"

```
sudo chmod 777 /Library/Application\ Support/com.apple.TCC
sudo rm -rf /Library/Application\ Support/com.apple.TCC/TCC.db
```