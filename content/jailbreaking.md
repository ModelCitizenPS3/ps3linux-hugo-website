+++
title = 'JAILBREAKING'
date = 2024-08-06T20:27:15-04:00
draft = false
layout = 'single'
+++

---

### *DISCLAIMER: For education only. If you brick your console, that's YOUR fault!*

This page contains an outline of the procedure I used to set up my Playstation 3 for booting Linux.

#### Downgrading the Playstation 3 to re-enable OtherOS (Linux)

1. [https://www.ps3toolset.com/bgtoolset](https://www.ps3toolset.com/bgtoolset)  
Navigate your Playstation 3's GameOS web browser to this miraculous website and behold the magic (thank you, bguerville)!  
Here is a good PS3 jailbreak tutorial video by Mr. Mario (if needed): [How to Jailbreak Your PS3 with PS3 Toolset](https://youtu.be/LIVu3Px3eXY)
2. [REBUG_CFW_4.84.2_REX_PS3UPDAT.PUP (Custom Firmware)](http://www.ps3linux.net/devel/ps3-filez/REBUG_CFW_4.84.2_REX_PS3UPDAT.PUP)  
After jailbreak, install this CFW which can be converted from CEX (retail) to DEX (debug).
3. [Convert Jailbroken PS3 from CEX to DEX with Rebug CFW](https://youtu.be/tmpexUf9eK0)  
Follow this tutorial by Mr. Mario to convert firmware from CEX (retail) to DEX (debug).  
Note: Procedure is easily reversible. See below.
4. [3.55DEXDOWNGRADERB4E_PS3UPDAT.PUP (Custom Firmware)](http://www.ps3linux.net/devel/ps3-filez/3.55DEXDOWNGRADERB4E_PS3UPDAT.PUP)  
Install this DEX Downgrader CFW which will allow you to next install Sony's 3.15 DEX firmware.
5. [SONY_PS3_FIRMWARE_3.15_DEX_PS3UPDAT.PUP (Official Firmware)](http://www.ps3linux.net/devel/ps3-filez/SONY_PS3_FIRMWARE_3.15_DEX_PS3UPDAT.PUP)  
This is Sony's DEX firmware 3.15 - the latest PS3 firmware with native support for OtherOS (Linux).  
Congratulations! Your Playstation 3 is now set up exactly like mine.and will support install of a Linux bootloader (kboot or petitboot).  
Note: At this point, don't forget to quick format the PS3's HDD (in System settings) and have it create a partition for OtherOS.
6. [PS3 Petitboot (OtherOS kexec Bootloader)](http://www.ps3linux.net/devel/ps3-filez/ps3-petitboot-09.11.30-cui_otheros.bld)  
PS3 Linux bootloaders may be installed to the console with a (vfat-formatted) USB drive or a burned CD/DVD.  
Note: Bootloader file must be in the proper directory (`/PS3/otheros`) and have the proper name (`otheros.bld`).  
Navigate to the PS3's Settings menu and select "Install OtherOS" (under "System" submenu) to install bootloader.

#### Converting PS3 DEX (Debug) Firmware Back to CEX (Retail)

* [REBUG_CFW_4.84.2_D-REX_PS3UPDAT.PUP (Custom Firmware)](http://www.ps3linux.net/devel/ps3-filez/REBUG_CFW_4.84.2_D-REX_PS3UPDAT.PUP)  
Install this firmware to convert your firmware from DEX back to CEX.
Follow this tutorial by ZoexModz if needed (apologies for the video's quality): [DEX to CEX & eid_root_key FIX](ttps://youtu.be/MyOmOz6P898)

