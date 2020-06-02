# Ryzentosh @ ASUS PRIME X570-PRO

OpenCore config for Zen2 and ASUS Prime X570-PRO based installations.

## What does not work

* Internal Audio (I am using the external USB card, so, I don't care about it)
* Sleep

## Hardware

* CPU: AMD Ryzen 3700X
* Motherboard: ASUS PRIME X570-PRO
* Memory: Crucial Ballistix 2x16GB BL2K16G30C15U4W
* GPU: XFX AMD Radeon 5700XT (reference)
* Ethernet: Intel I211-AT
* Audio: Focusrite Scarlett 4i4 3rdgen
* NVME: Samsung 970 Evo Plus 500GB
* SATA: Samsung 860 Evo 1TB
* SATA: Samsung 850 Evo 1TB

## Tips and tricks

### Audio stuttering and crackling

* Switch PCIe slot with PCIe Gen.4 GPU to the 3.0 mode. It helps a lot

### macOS fails to load

* If macOS loading hangs, please check that you have `npci=0x2000` in `NVRAM/boot-args` section.

## ACPI

* https://github.com/radianttap/EFI-ASRock-X570-ITX-iMacPro1-1

## Software

* OpenCore 
  * URL: https://github.com/acidanthera/OpenCorePkg
  * Version: `0.5.7`
  * Removed:
    * `Drivers/HiiDatabase.efi`
    * `Drivers/NvmExpressDxe.efi`
    * `Drivers/XhciDxe.efi`
    * `Tools/*`

* AppleSupportPkg
  * URL: https://github.com/acidanthera/AppleSupportPkg
  * Version: `2.1.6`
  * Removed:
    * `Drivers/AudioDxe.efi`

* Lilu
  * URL: https://github.com/acidanthera/Lilu
  * Version: `1.4.3`

* VirtualSMC
  * URL: https://github.com/acidanthera/VirtualSMC
  * Version: `1.1.2`
  * Removed:
    * `Kexts/SMCBatteryManager.kext`
    * `Kexts/SMCLightSensor.kext`
    * `Tools/*`

* WhateverGreen
  * URL: https://github.com/acidanthera/WhateverGreen
  * Version: `1.3.8`
  * Removed:
    * `ACPI/SSDT-PNLF.aml`

* SMCAMDProcessor
  * URL: https://github.com/trulyspinach/SMCAMDProcessor
  * Version: `0.6`

* HoRNDIS
  * URL: https://github.com/jwise/HoRNDIS/releases
  * Version: `9.2`

* SmallTree Intel 82576
  * URL: unknown
  * Version: unknown

* RadeonBoost
  * URL: https://egpu.io/forums/mac-setup/radeonboost-something-for-you-guys-to-try/
  * Version: `1.3`

