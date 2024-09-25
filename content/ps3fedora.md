+++
title = 'PS3 FEDORA'
date = 2024-08-06T22:18:44-04:00
draft = false
layout = 'single'
+++

---

### Fedora 12 (ppc) on Playstation 3

The latest Fedora release that is compatible/installable on the Playstation 3 is Fedora 12 (ppc). There are several good reasons to choose Fedora 12 as your PS3 Linux distro. For one thing, the online software repositories are still up (archived) and accessible. Obviously they are no longer receiving updates, but the volume/variety of applications they provide is impressive. This also includes the RPM Fusion repos. Furthermore, the programming tools and libraries for the PS3's Cell architecture were developed by Sony/IBM to install and run on RPM based distributions (such as Fedora or RHEL) and I have personally confirmed that these tools do install and function properly in Fedora 12 with minimal issues/complications.

#### Fedora 12 (ppc) Install ISOs

* [Fedora-12-ppc-DVD.iso](https://dl.fedoraproject.org/pub/archive/fedora/linux/releases/12/Fedora/ppc/iso/Fedora-12-ppc-DVD.iso)  
* [Fedora-12-ppc-netinst.iso](https://dl.fedoraproject.org/pub/archive/fedora/linux/releases/12/Fedora/ppc/iso/Fedora-12-ppc-netinst.iso)

#### My PS3 Fedora Youtube Videos

* [Playstation 3 Fedora Server Install (OtherOS) Diskless](https://youtu.be/D9LcyRV84LI)  
Video of me installing Fedora 12 (ppc) on my Playstation 3 over the network via an NFS share  
* [Four Servers I Run on my Playstation 3 (in Linux)](https://youtu.be/CveuUwIIcGQ)  
Showcasing some of the services my Playstation 3 provides on my home network - includes SSH, NFS, VNC, and HTTP

#### Some Scripts I Wrote for Fedora 12 on PS3 (post-install)

* [ps3-goodrepos](http://www.ps3linux.net/devel/ps3-filez/ps3-goodrepos.tar.bz2)  
Script to configure yum repos and run update after fresh Fedora 12 installation on Playstatiion 3  
* [ps3-cellsdk-install](http://www.ps3linux.net/devel/ps3-filez/ps3-cellsdk-install.tar.bz2)  
Script to configure yum to access the [Cell Software Development Kit (SDK) yum repos](http://www.ps3linux.net/devel/cellsdk-repos) (hosted here by me)

