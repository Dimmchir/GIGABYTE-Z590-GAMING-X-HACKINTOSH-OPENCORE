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
- Boot-chime
- Sleep and wake
- Ethernet/Bluetooth
- Custom USB port mapping with USBToolBox
```
_________________________________
# What doesnt work : 
```
Wi-Fi not working with PCIe Wi-Fi Fenvi T919
```
_________________________________
![IMac](https://github.com/user-attachments/assets/8a2d8313-bbd0-4f94-97f2-716029d3b6e0)
![collage](https://github.com/user-attachments/assets/cad557dd-deb8-4a3a-a849-c5802d8b2830)

# Warning!
Smbios serial numbers have been removed from Config.plist:
![PlatformInfo](https://github.com/user-attachments/assets/8737621c-39cc-4430-8997-d657643834f8)

You need to make your own Smbios. It is convenient to do this using the [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
_________________________________
# USB map

![USB Map Gigabyte Z590](https://github.com/user-attachments/assets/d2f624b4-63fc-4237-bc9d-149b4b8893fa)

The USB port map was made using [USBToolBox](https://github.com/USBToolBox/tool).
Since the number of USB ports on the motherboard exceeds the permitted number of 15, some ports had to be disabled.

The following ports are disabled here:
```
- USB 2 Port 03(03)
- USB 2 Port 04(04)
- USB 2 Port 07(07)
- USB 3 Port 23(17)
- USB 2 Port 08(08)
- USB 2 Port 24(18)
```
You can change the USB map by editing UTBMap.kext
_________________________________
AppleALC.kext is modified, it only contains the ALC897 codec.
_________________________________
When updating Mac OS, you must change the config.plist in the Misc/Security/SecureBootModel section to temporarily set the value to Disabled, otherwise there will be an endless reboot.

![Disabled](https://github.com/user-attachments/assets/8c9835c9-a4f5-444b-9333-03335fbacb4f)

After updating, you can return the value to Default in the Misc/Security/SecureBootModel section.
_________________________________
To edit config.plist it is better to use [ProperTree](https://github.com/corpnewt/ProperTree)
