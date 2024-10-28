+++
title = 'JAILBREAKING'
date = 2024-08-06T20:27:15-04:00
draft = false
layout = 'single'
+++

## DISCLAIMER: *For education only. If you brick your console, that's YOUR fault!*

---

![Black Beauty](/pics/ps3-black-bg-320.jpg)

This page contains all the files I used in the process of setting up my Playstation 3 to boot and run Linux. It also contains an outline of the steps I followed to complete the procedure. Links to important websites (like Bguerville's magical [ps3toolset](https://www.ps3toolset.com/bgtoolset) - THANK YOU, BGUERVILLE; GREAT WORK!) and some helpful Youtube tutorials are provided as well.

So, currently there are two methods of preparing (hacking) a Playstation 3 for the purpose of running Linux. Probably the more popular method (as it applies to a larger number of consoles) is to install a custom firmware (like REBUG) that supports partitioning the PS3's HDD and launching the bootloader (petitboot) from a custom menu of hacks. This method is sometimes referred to as OtherOS++ and will work on any Playstation 3 capable of flashing custom firmware (CFW). The other method to configure a PS3 for Linux involves using a custom firmware to perform a "downgrade" of the console's system software such that an official Sony firmware of release number 3.15 or lower may be installed. Sony's firmware 3.15 is the last official firmware that natively supported booting OtherOS (Linux) and contained options in the settings menu for paritioning the PS3's HDD, installing a bootloader (kboot or petitboot), and dual booting between Sony's GameOS and OtherOS. For this method to work, you must have a Playstation 3 old enough to flash a firmware of release 3.15 or lower. My PS3 (a CECHP-01) happens to be old enough to flash an OtherOS firmware so that is the method I used on my console, and it is also the procedure that I here describe (see below).

#### Downloads - Some Firmwares and a Bootloader (for Downgrading and Linux Prep)

* [REBUG_CRC67E4A95C_FWv4.84.2_REX_PS3UPDAT.PU](/ps3-filez/REBUG_CRC67E4A95C_FWv4.84.2_REX_PS3UPDAT.PU)  
MD5 - 0835d81e3c581f3bdfdfbe86fca5e192  
Rebug custom firmware (CFW) 4.84.2 REX - Supports conversion from CEX (retail) to DEX (debug)
* [3.55DEXDOWNGRADERB4E.PUP](/ps3-filez/3.55DEXDOWNGRADERB4E.PUP)  
MD5 - efa62388ee8d2592727ddbdce9b4bec8  
DEX downgrader CFW - Installs on DEX PS3s, permits flashing with obsoleted (downgraded) firmwares
* [DEX_CRC7CCB04C0_FWv3.15_PS3UPDAT.PUP](/ps3-filez/DEX_CRC7CCB04C0_FWv3.15_PS3UPDAT.PUP)  
MD5 - DEX_CRC7CCB04C0_FWv3.15_PS3UPDAT.PUP  
Official (Sony) firmware 3.15 (DEX) - Natively supports dual booting between GameOS and OtherOS (Linux)  
This is the firmware I use on my console for all of my PS3 Linux exploits & endeavors. I love this firmware.
* [ps3-petitboot-09.11.30-cui.bld](/ps3-filez/ps3-petitboot-09.11.30-cui.bld)  
MD5 - 7969b377ac5727c8e602d6de0716f0b4  
PS3 Petitboot - A kexec-based PowerPC Linux bootloader. Works like GRUB (on x86 machines)
* [REBUG_CRC63F00899_FWv4.84.2_D-REX_PS3UPDAT.PUP](/ps3-filez/REBUG_CRC63F00899_FWv4.84.2_D-REX_PS3UPDAT.PUP)  
MD5 - 9211252d41841461c6299bfad48fa7f1  
Rebug custom firmware (CFW) 4.84.2 D-REX - Supports conversion from DEX (debug) back to CEX (retail)

#### Downgrading the Playstation 3 to Re-Enable OtherOS (Linux)

1. ***Jailbreak Your Console***  
Navigate your PS3's GameOS web browser to Bguerville's ps3toolset site:  
[https://www.ps3toolset.com/bgtoolset](https://www.ps3toolset.com/bgtoolset).  
Follow this video by Mr. Mario to perpetrate your jailbreak:  
[How to Jailbreak Your PS3 with PS3 Toolset](https://youtu.be/LIVu3Px3eXY).
2. ***Install REBUG_CRC67E4A95C_FWv4.84.2_REX_PS3UPDAT.PUP Custom Firmware***  
After jailbreak, reboot the console and perform a firmware "upgrade" using REBUG custom firmware (see above for download).
3. ***Perform Firmware Conversion from CEX (retail) to DEX (debug)***  
Follow this video by Mr. Mario (if needed) to perform CEX to DEX conversion:  
[How to Convert a Jailbroke PS3 from CEX to DEX with REBUG](https://youtu.be/tmpexUf9eK0)  
Note: This step is a bit scary for noobs. Bear in mind that this conversion is totally reversible (see below).
4. ***Install 3.55DEXDOWNGRADERB4E.PUP Custom Firmware***  
Perform a firmware update using custom firmware 3.55DEXDOWNGRADERB4E.PUP (see downloads above).  
This DEX "downgrader" is pre-configured to permit flashing with Sony's official (DEX) firmware 3.15 in the next step.
5. ***Install Official Sony Firmware DEX_CRC7CCB04C0_FWv3.15_PS3UPDAT.PUP***  
Finally, flash firmware DEX_CRC7CCB04C0_FWv3.15_PS3UPDAT.PUP to the PS3 using the usual update procedure.  
After install, your PS3 will be setup just like mine, and you will have re-enabled support for OtherOS on your console... goodie gum-drops!
6. ***Format the PS3's HDD and Create a Partition for OtherOS***  
Look in the system menu (under Settings) and select the option to perform a quick format of the PS3's hard drive.  
You will be given options for if (and how) you would like to partition the drive for OtherOS.  
Personally, I chose to give GameOS 10% of HDD space and designated the remaining storage available for Linux (OtherOS).
7. ***Install PS3 Petitboot (your PowerPC Linux Bootloader)***  
Copy ps3-petitboot-09.11.30-cui.bld to the correct directory (`/PS3/otheros`) on a fat32-formatted USB drive and rename the file as `otheros.bld`.  
With the USB drive in the PS3, select "Install OtherOS" from the System menu (under Settings) and your Linux bootloader will install.
8. ***Reboot Your Playstation 3 into OtherOS***  
Select "Default System" in your System menu (under Settings) and switch it from PS3 to OtherOS.  
After reboot, your PS3 will load the petitboot bootloader menu; you can now go about installing a PS3-compatible Linux distro.  
My strong suggestion would be to try out Fedora 12, a stupendous operating system for the PS3.  
Follow this video by me (the Model Citizen) demonstrating a network (diskless) Fedora 12 install on my own PS3:  
[PS3 Fedora Server Install (OtherOS) Diskless](https://youtu.be/D9LcyRV84LI)

#### To Convert Firmware Type from DEX (debug) Back to CEX (retail)

1. ***Install REBUG_CRC63F00899_FWv4.84.2_D-REX_PS3UPDAT.PUP Custom Firmware***  
Update system firmware with this REBUG DEX custom firmware, which can be converted from DEX back to CEX.
2. ***Execute Firmware Conversion***  
Follow this video by ZoexModz to perform DEX to CEX conversion:  
[DEX to CEX & eid_root_key Fix](https://youtu.be/MyOmOz6P898)

---

