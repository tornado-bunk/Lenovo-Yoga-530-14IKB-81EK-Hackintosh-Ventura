
# Lenovo Yoga 530-14IKB-81EK Hackintosh Ventura

macOS Ventura on Lenovo Yoga 530-14IKB-81EK with OpenCore 1.0.7
<img src="https://github.com/tornado-bunk/Lenovo-Yoga-530-14IKB-81EK-Hackintosh-Ventura/blob/main/VenturaYoga.png" alt="look">

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

## Please note that:
- You should add Serial Number, UUID, MLB and ROM details to Config -> PlatformInfo -> Generic if you want to get iServices working.

## Experimental: macOS 26 Tahoe
- There is an **experimental branch** for macOS 26 Tahoe.
- **Status:** It boots successfully, but most features (Wi-Fi, etc.) are still missing, unstable and untested.

## Credits
- [Dortania](https://dortania.github.io/OpenCore-Install-Guide/) for the legendary OpenCore Install Guide.
- [techgenius1](https://github.com/techgenius1/Yoga530-14IKB-Hackintosh-OpenCore) for the README structure and configuration ideas for the Yoga 530.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and the essential kexts (Lilu, VirtualSMC, WhateverGreen).
- [lvs1974](https://github.com/acidanthera/CpuTscSync) for **CpuTscSync**, the lifesaver that fixed the TSC sync issues on the i5-8250U.
- All the **Hackintosh Community** for sharing the knowledge that made this build possible.
