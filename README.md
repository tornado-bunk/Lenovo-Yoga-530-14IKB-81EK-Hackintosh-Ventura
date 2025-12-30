
# Lenovo Yoga 530-14IKB-81EK Hackintosh Tahoe

macOS Tahoe on Lenovo Yoga 530-14IKB-81EK with OpenCore 1.0.7
<img src="https://github.com/tornado-bunk/Lenovo-Yoga-530-14IKB-81EK-Hackintosh-Ventura/blob/experimental/tahoe/TahoeYoga.png" alt="look">

## Configuration

| Specifications      | Detail                                      |
| ------------------- | ------------------------------------------- |
| Computer model      | Lenovo Yoga 530-14IKB-81EK		         |
| Processor           | Intel Core i5-8250U Processor               |
| Memory              | 8GB DDR4 2666MHz	                          |
| Integrated Graphics | Intel UHD Graphics 620                      |
| Sound Card          | Realtek ALC236 (layout-id:99)               |
| Wireless Card       | Intel Wireless 3165                         |
| Touchpad            | Synaptics I2C Touchpad                      |

## What's not working:

- [ ] Fingerprint
- [ ] Pen
- [ ] Wifi
- [ ] Bluetooth
- [ ] Almost everything

## Please note that:
- You should add Serial Number, UUID, MLB and ROM details to Config -> PlatformInfo -> Generic if you want to get iServices working.

## Experimental: macOS 26 Tahoe
- This is an **experimental branch** for macOS 26 Tahoe.
- **Status:** It boots successfully, but most features (Wi-Fi, etc.) are still missing, unstable and untested.

### Branch Specifics (Tahoe vs Ventura)
- **Wi-Fi:** Switched to `itlwm.kext` instead of `AirportItlwm`.
  - *Note:* You MUST use the [HeliPort](https://github.com/OpenIntelWireless/HeliPort) app to manage connections.
- **Audio:** `AppleALC` has been removed; testing `VoodooHDA` injection for this kernel version. 
- **Booter:** Enabled `FixupAppleEfiImages` quirk to ensure compatibility with the Tahoe bootloader. 

### Kexts Currently DISABLED (Testing Phase)
To isolate boot issues on macOS 26, the following kexts are temporarily set to `false` in the config: 
- **Battery & Sensors:** `SMCBatteryManager`, `SMCLightSensor`, `SMCProcessor`, `SMCSuperIO`. 
- **Bluetooth:** Full Intel Bluetooth suite (`BlueToolFixup`, `IntelBTPatcher`, `IntelBluetoothFirmware`). 
- **Yoga Features:** `YogaSMC` and `BrightnessKeys`. 
- **USB Mapping:** `USBToolBox` and `UTBDefault`.

## Credits
- [Dortania](https://dortania.github.io/OpenCore-Install-Guide/) for the legendary OpenCore Install Guide.
- [techgenius1](https://github.com/techgenius1/Yoga530-14IKB-Hackintosh-OpenCore) for the README structure and configuration ideas for the Yoga 530.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and the essential kexts (Lilu, VirtualSMC, WhateverGreen).
- [lvs1974](https://github.com/acidanthera/CpuTscSync) for **CpuTscSync**, the lifesaver that fixed the TSC sync issues on the i5-8250U.
- All the **Hackintosh Community** for sharing the knowledge that made this build possible.

