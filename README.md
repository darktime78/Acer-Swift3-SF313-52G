# Acer-Swift3-SF313-52G
For Fun  
## Configuration  
Hardware  | Model
---  | :--
Processor | Intel(R) Core i7-1065G7
Graphics | Intel(R) Iris(R) Plus Graphics G7 + Nvidia Geforce MX350 (Disable)
SSD |	Intel(R) 660p 1Tb 
RAM |	16GB LPDDR4X 3200MHz
Wifi + Bluetooth | Intel(R) Wifi 6 AX201 
Audio  |	Conexant CX8400
LCD | IPS（13.5 Inches 3:2 2k)
## System version - Ventura 13.6.1
- For other versions, please replace `AirportItlwm.kext` by yourself
- Please add `IntelBluetoothInjector.kext` for versions below Monterey, [Reference for details](https://openintelwireless.github.io/IntelBluetoothFirmware/FAQ.html#what-additional-steps-should-i-do-to-make-bluetooth -work-on-macos-monterey)
## Bios settings
* Main->Ctrl＋s->SATA Mode->AHCI
* Main->Fast Boot->Disabled
* Main->Security->Set Supervisor Password->Change TPM (TCM) State->Disable (otherwise you will sleep until the battery runs out with black screen) Trusted Platform Module (TPM)
### Optional
- Set DVMT Pre-Allocated to 04 (128M) or 05 (160M). The inability to enter the BIOS after changing to 05 in the picture may be due to other problems. After resetting the NVRAM, it is normal.
- Disable CFG Lock
- Disable Low Power S0 (for Sleep)
- Turn on HIDPI
## Known issues
- The built-in microphone is Intel Smart Sound Technology and cannot be driven
- The HDMI driver has been removed from the official driver. HDMI on the body cannot be used and a type-c adapter is required.
