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
* Main->Ctrl+s->SATA Mode->AHCI
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

## Firmware BIOS without OS
1. Downloaded the latest v1.08 BIOS archive file from Official Acer site. It's an EXE file (BIOS_Acer_1.08_A_A.exe) that can be extracted via 7z. 
2. Copy the BIOS file __BiosEc.fd__ to an empty and with FAT16/32 formatted usb stick.
2. Unplug the AC adapter.
3. Plug in the USB flash disk.
4. Press and hold <Fn> and <Esc>, and then plug in the AC adapter while still holding <Fn> and <Esc>.
5. Press the Power button. You can now stop holding <Fn> and <Esc>.
6. The BIOS flash should now begin, the fan will spin up and the power led should change its state.
7. After everything is done, the notebook will shut down.

## Modify BIOS settings
Modifications are risky, please proceed with caution
The test is normal on 1.08. There is no guarantee that other versions will not have problems.
1. First open WDFInst.exe, then open H2OUVE-W-GUIx64.exe

2. Click File->Load runtime

3. Click the green Variable on the left

4. Perform the following modifications
* Disable CFG Lock
![CFGLock](https://github.com/darktime78/Acer-Swift3-SF313-52G/blob/main/images/CFG_Lock.png)  

* DVMT Pre-Allocated
![DVMT](https://github.com/darktime78/Acer-Swift3-SF313-52G/blob/main/images/DVMT.png)  

* Disable Low Power S0 (Enable S3)
![S0](https://github.com/darktime78/Acer-Swift3-SF313-52G/blob/main/images/Low_Power_S0.png)  

5. Click File->Save and restart system
  
