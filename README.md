# HP 15-EF2127WM

# Hackintosh Configuration

This repository contains a personal OpenCore EFI configuration for a Hackintosh build based on the HP 15-EF2127WM laptop.

August 9, 2026.

## Hardware Summary

- Laptop: HP 15-EF2127WM
- CPU: AMD Ryzen 5 5500U with Radeon Graphics
- Cores/Threads: 6 cores / 12 threads
- GPU: AMD Radeon Graphics (Renoir)
- RAM: 8 GB DDR4 (2 x 4 GB, Samsung)
- Wi-Fi/Bluetooth: Realtek RTL8822CE 802.11ac PCIe Wireless adapter
- Storage: ADATA SX8200PNP NVMe SSD
- Display: 15.6-inch 1728x1080 eDP panel
- SMBIOS: MacBookPro16,3

## Project Purpose

This EFI is set up for running macOS with OpenCore on the hardware listed above. It includes the standard ACPI patches, kexts, and boot configuration needed for this specific AMD Renoir-based system.

## OpenCore Layout

- EFI/BOOT/BOOTx64.efi
- EFI/OC/OpenCore.efi
- EFI/OC/config.plist
- EFI/OC/ACPI/
- EFI/OC/Kexts/
- EFI/OC/Drivers/
- EFI/OC/Resources/
- EFI/OC/Tools/

## Included ACPI

The config includes several SSDTs for power management and compatibility, including:

- SSDT-PLUG-ALT.aml
- SSDT-HPET.aml
- SSDT-USBX.aml
- SSDT-RTCAWAC.aml
- SSDT-EC.aml
- SSDT-PNLF.aml

## Kernel Extensions

The setup uses a standard AMD/Apple-friendly stack with:

- Lilu.kext
- VirtualSMC.kext
- ForgedInvariant.kext
- AppleALC.kext
- AirportBrcmFixup.kext
- USBToolBox.kext
- UTBDefault.kext
- UTBMap.kext
- RealtekCardReader.kext
- RealtekCardReaderFriend.kext
- RTLBluetoothFirmware.kext
- rtw88.kext
- RtWlanU.kext
- RtWlanU1827.kext
- RestrictEvents.kext
- NVMeFix.kext
- SMCBatteryManager.kext
- SMCProcessor.kext
- Various AMD power and sensor kexts

## Notes

- This configuration is tailored to the hardware detected in the provided system dump.
- OpenCore is configured with common AMD Renoir compatibility settings.
- Wi-Fi support is handled through Realtek-based kexts.
- Use this repository as a starting point and validate all settings against your own hardware and macOS installation.

## Important Warning

This is a personal EFI configuration for a Hackintosh system. It should be used carefully and only after understanding the relevant OpenCore and macOS compatibility requirements.

## Credits

- OpenCore team
- Acidanthera
- Community Hackintosh developers and maintainers

## License

This project is provided as-is for personal use and experimentation.
