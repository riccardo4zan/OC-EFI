# OpenCore EFI

Guide: https://dortania.github.io/OpenCore-Install-Guide/

# Hardware configuration
* i5 6500
* ASUS H170M-PLUS
* RX 570 4G (Sapphire ITX) 
* 16GB DDR4 

# BIOS Settings
Starting from the default configuration on BIOS version 3805, no changes to defualt settings

# EFI
- SIMBIOS: iMac 17,1 
- OC Version: 0.6.4 (Updated 8/12/2020)

# Working:
* Ethernet 1GB
* Audio
* Sleep
* All USB ports
* Power Management

# TODO:
- [ ] Disable OC boot picker (https://www.reddit.com/r/hackintosh/comments/gerpxg/how_to_turn_off_picker_on_opencore/)
- [ ] FileVault (https://dortania.github.io/OpenCore-Post-Install/universal/security.html#filevault)
- [ ] iServices (Serial not valid) (https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html)

__________

# Kexts:
* Apple ALC (https://github.com/acidanthera/applealc/releases)
* IntelMausi (https://github.com/acidanthera/IntelMausi/releases)
* Lilu (https://github.com/acidanthera/lilu/releases)
* VirtualSMC + SMCProcessor + SMCSuperIO (https://github.com/acidanthera/virtualsmc/releases)
* WhateverGreen (https://github.com/acidanthera/whatevergreen/releases)
* USBInjectAll (https://bitbucket.org/RehabMan/os-x-usb-inject-all/src/master/)

# Credits
* Opencore: https://github.com/acidanthera/OpenCorePkg

* GibMacOS https://github.com/corpnewt/gibMacOS
* ProperTree https://github.com/corpnewt/ProperTree
* GenSMBIOS https://github.com/corpnewt/GenSMBIOS
* SSDT Time https://github.com/corpnewt/SSDTTime
