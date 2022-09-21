# <div align="center">Asus Laptop 15 X509FA Hackintosh</div> 

## Bootloader Versions

|OpenCore|
|--------|
|0.8.4 | 

## Supported macOS Versions
- Big Sur (Use SMBIOS ```MacBookPro15,3```)
## Screenshots

<div align="center">
  
![Screenshot](Screenshots/ScreenShot.png)

</div>


## Laptop Specification
 
|                     | Specifications| Note |
| ---------------------------- | ---------------------- |------------------|
| ``Chipset``| Intel Chipset |   |
| ``CPU``| QuadCore Intel Core i5-8265U 1.3GHz | Use [HFSPlus.efi](https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi) |
| ``Memory``| 8GB DDR4 2400Mhz | 2 x 4GB DDR4. |
| ``iGPU``| Intel UHD Graphics 620 | Patch with [Patch-HD4000-Monterey](https://github.com/chris1111/Patch-HD4000-Monterey) by [chris1111](https://github.com/chris1111) in Monterey. |
| ``Disk 0``| SSD Micron_2200V_MTFDHBA512TCK 512GB | Dualbooting Windows and Arch Linux. |
| ``Disk 1``| SSD Lexar 128GB | Install macOS. |
| ``Card Reader``| Realtek RTS5129 | Use [RealtekCardReader](https://github.com/0xFireWolf/RealtekCardReader/releases/tag/v0.9.6). |
| ``Fingerprint`` | Synaptics FP Sensors | Not working in macOS. |
| ``Screen``| 15.6" 1920 x 1080 |    |
| ``Ethernet``| No Ethernet |       |
| ``Wifi``| Intel® Dual Band Wireless-AC 9461 | (Replace from AR9485) Use [AirportItlwm](https://github.com/OpenIntelWireless/itlwm/releases). | 
| ``Bluetooth``| Intel (R) Wireless Bluetooth | (Replace from AR9485) Use [IntelBluetoothFirmware](https://openintelwireless.github.io/IntelBluetoothFirmware/). | 
| ``Audio``| Realtek ALC256 | Add `alcid=66` to boot-arg or add layout-id to DeviceProperties. |
| ``Keyboard``| - | Requied patching SSDT for brightness key. |
| ``Touchpad``| I2C HID Device | Use [VoodooPS2-ALPS](https://github.com/SkyrilHD/VoodooPS2-ALPS/releases/tag/1.0.7). |
| ``Dimensions``| 30mm x 345.5mm x 244mm |     |
|``Weight``| 1.92kg |     |
  
<div align="center">
  
![Screenshot](Screenshots/specs.png)
  
</div>

## Features


|                               | OpenCore             |
| ----------------------------- | -------------------- |
| ``Wifi and Bluetooth``|✅|
| ``Audio``|✅|
| ``Keyboard and Trackpad``|✅|
| ``Headphone Jack``|✅|
| ``Graphics``|✅|
| ``Battery``|✅|
| ``Card Reader``|✅|
| ``Power Management``|✅|
| ``Multigesture Trackpad``|✅|                                          
| ``Webcam``|✅|
| ``USB Port``|✅|
| ``Facetime and iMessage``|✅|
| ``Sleep``|✅|
| ``Hotkeys``|✅|
<!-- | ``Ethernet``|✅| -->

# Boot Arguments
- When Install:

Using this Boot-args: ```-v keepsyms=1 debug=0x100```

- After Installation:

```revpatch=memtab``` Enable Memory tab in About this Mac when using MacbookPro10,2 SMBIOS with [RestrictEvents](https://github.com/acidanthera/RestrictEvents) kext.