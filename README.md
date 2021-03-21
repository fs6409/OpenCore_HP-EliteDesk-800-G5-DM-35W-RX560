# OpenCore_HP-EliteDesk-800-G5-DM-35W-RX560
Here a the files and guides I used for the installation of macOS Big Sur on HP EliteDesk 800 G5 Desktop Mini With Rx560 GPU

## Description
Product Name : HP EliteDesk 800 G5 Desktop Mini

Product No. : 6AU16AV

Product Desc. : BU IDS EliteDesk 800 35W G5 GPU DM

- CPU : Intel Core i7-8700T or i5-8500T
- GPU : Intel Graphics UHD630 (Dual DisplayPort)
- GPU : AMD RX560 (DisplayPort)
- Memory : 2 Slots DDR4-2400 64GB(32GB x 2)
- Storage : PCIe NVMe 2 TB, PCI-E Gen3 x 4, KIOXIA(Toshiba) KXG60PNV2T04 
- Ethernet : Intel I219LM Gigabit Network Connection LOM
- Wireless LAN : DW1560 or DW1820

## Known Issues
- I'm using a USB DAC to audio out, if you want to use the Internal Speaker and 2 audio out front ports you will do 
  additional kext hack.
- With DW1560 or DW1820, unlock whit Apple Watch does not work.

## Installation

### BIOS Settings
- Disable Fast Boot
- Enable USB boot
- UEFI Boot order, make sure your USB device is first to boot
- Secure Boot : Legacy Support Disable and Secure Boot Disable
- Set Video Memory to 64 MB

### Installation
Create a USB Key with Big Sur following the Dortaina OpenCore guide

## Post Installation
### Add OpenCore to Boot disk
The Dortania Post-Install guide demonstrates how to install OpenCore to the boot drive


### config.plist
**ACPI Section**

- Already fixed real-time clock power loss (005) (RTC ERROR)

**Please regenerate a new SystemSerialNumber, MLB Number and a new SystemUUID**
