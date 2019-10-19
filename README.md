# Gigabyte Designaire Z390 - for macOS Catalina 10.15 (19A602)

### General Information
This EFI uses Clover v2.5k-5097. This is a vanilla install. All kexts and drivers are kept in the EFI folder.

## Before You Boot:
### Make necessary changes to the `config.plist`

1. Ensure that you visit the SMBIOS in Clover Configurator pane and add your own Serial Numbers. They have been removed from this config.plist. 
    - You may do this by visiting the SMBIOS tab and clicking the dropdown underneath "Check Coverage" to the right of the page, and selecting "iMac19,1". This will auto-generate all the information you need. If you're doing it manually, you'll see the values have been replaced with the text `[REPLACE_ME]`.
    
### Double-check your BIOS settings

1. Please ensure that youhave `Chipset` > `Internal Graphics` **disabled**. I know everyone elese says to enable it, but it seems as though Catlina doesn't like it.

### Misc. Recommendations
- Install Catalina using AFPS and *not* using MacOS Extended Journaled
- Add `-v` to boot arguments to boot via verbose mode until you're positive you have a good setup, instead of showing the logo. 
    - This can be done by pressing the `Space` button on your keyboard in the Clover boot menu while (make sure you have the installation drive selected), and then selecteding `-v` in the middle of the argiments list. Then, go up to the top and click `boot <VOLUME_NAME> with selected options`.
- A custom theme has been applied. You may wish to revert to the standard theme or apply your own.

---
## My Hardware:
- Gigabyte Designare Z390
- Intel Core i9 9900K
- AMD Radeon VII 16 GB
- Fenvi T919 Bluetooth/WiFi Card
- Samsung EVO 860s and 850s

---

## Working (incomplete list, only the things I care about)
1. Bluetooth / WiFi (Fenvi T919 PCI/E card -- the embedded one is diabled)
2. Audio (except the rear IO's 3.5mm jack... the front one works somehow)
3. NVRAM Emulation
4. Shutdown / Restart / Sleep (including bluetooth-on-wake)
5. USB 3.0 / 3.1 (including charging and hotswapping)
6. Thunderbolt 3 (including charging and hotswapping)

## Changes
**10/18/2019**
- Fixed Shutdown and Sleep / Bluetooth-on-wakeup by adding EmuVariableUefi to the list of drivers

**10/19/2019**
- Updated to CLover 2.5-5097 from 5095.
- Removed two unused themes.