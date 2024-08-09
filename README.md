# GIGABYTE-Z590-GAMING-X-HACKINTOSH-OPENCORE
Hackintosh settings for Gigabyte Z590 GAMING X (rev. 1.0) Sonoma OpenCore 1.0.0
_________________________________
| Specifications | Detail                                                  |
| ------------------- | ------------------------------------------- |
| Motherboard | Gigabyte Z590 GAMING X (rev. 1.0) |
| Processor | Intel Core i7-10700K|
| Discrete Graphics | ASRock AMD Radeon RX 6600 XT |
| Integrated Graphics | Intel UHD Graphics 630 (not used) |
| Wireless/Bluetooth Card | PCIe Wi-Fi Fenvi T919 (Wi-Fi not working)|
| Sound chip | Realtek ALC897 (layout-id:12 (0C000000)) |
_________________________________

# What works : 
```
- Sound
- Sleep and wake
- Ethernet/Bluetooth
- Custom USB port mapping with USBToolBox
```
_________________________________
# What doesnt work : 
```
Wi-Fi not working with PCIe Wi-Fi Fenvi T919
- 
```
_________________________________
![IMac](https://github.com/user-attachments/assets/8a2d8313-bbd0-4f94-97f2-716029d3b6e0)
![collage](https://github.com/user-attachments/assets/cad557dd-deb8-4a3a-a849-c5802d8b2830)

# Warning!
Smbios serial numbers have been removed from Config.plist:
![PlatformInfo](https://github.com/user-attachments/assets/af01b6ce-f366-4dce-ba14-38ad629d4333)
You need to make your own Smbios. It is convenient to do this using the [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
