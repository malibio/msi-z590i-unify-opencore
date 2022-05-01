# msi-z590i-unify-opencore
This repository contains the EFI content I used to run the latest OpenCore boot loader.  I'll add more details below, but for now - if you know what you're doing - feel free to play with the EFI folder

# Hardware
Items that could affect your config.plist (if different from yours, you might need to do a bit of reading and/or troubleshooting ):
- MSI Z590i Unify Motherboard (obviously)
- Intel 11700K CPU
- XFX Speedster SWFT 210 Radeon RX 6600 (though thinking of upgrading)
- WD Black SN750 High Performance NVMe M.2 Internal
- WLAN: BCM94360NG (bought it Amazon - look it up)

Items SHOULD not require config adjustment:
- Corsair Vengeance LPX 32GB (2 x 16GB)
- Arctic Liquid Freezer II 120
- Corsair SF600 PC Power Supply
- Phanteks Enthoo Evolv Shift 2 Mini-ITX Case

# Working
- macOS Monterey 12.3.1
- Wifi and Bluetooth (via BCM94360NG Wireless Card)
- Audio via DisplayPort (didn't test the audio jacks)
- USB: all ports available with my case
- Thunderbolt 3/4 including Hot-plug (from my test it works, but I don't really have a TB4 device to test with)
- Ethernet: works at 1Gbps speed (have not tested with 2.5Gbps because my router doesn't go as fast)
- Airdrop
- Sleep/Wake (via power button)
- Shutdown
- Restart

# Not working
- Sidecar (this is due to 11th Gen CPU's iGPU is not supported by Apple)

# BIOS Settings
- More to follow

# Installation instructions
- Download the entire EFI folder found in this repo.
- Use the OpenCore install guide WRT to [create a macOS installer USB stick](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/mac-install.html).
- Download [MountEFI](https://github.com/corpnewt/MountEFI), then mount your USB installer's EFI partition to copy the downloaded EFI folder there (yes, you'll end up with an EFI folder within the EFI drive).
- Reboot to your installer USB stick, then follow instructions.
- Once macOS installation completed, mount the EFI drive of your main installion hard disk drive to copy the EFI folder.
- Follow this [guide](https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#platforminfo) to change the SMBIOS info in your config file

