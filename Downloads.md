# Current Release: 4.1.0  
Source Code  
Source Code can be found here: https://github.com/limboemu/limbo  
  
  
Release Notes  
  
* Support for compiling with QEMU 4.0.0 see README.developers for instructions
* VNC is now using a Unix domain socket for local connection
* QMP is now using a Unix domain socket for local connection
* Support for allowing QMP external connections
* Updated download and guide links to github repo
* Added software updates option in settings screen
* Moved legacy file manager option to settings screen
* SDL interface is now default
  
  
***

Known Issues:  
Mouse acceleration issues in QEMU VNC (see guide for disabling it)  
Emulated audio is slow  

  
If you want to follow the guides and setup your OS images you should also install QEMU for Windows and Linux:  
  
Qemu with GTK (GUI) for Windows Make sure you download a version with GTK if you want a GUI.  
Qemu Manager (GUI) for Windows  
  
If you have Ubuntu or if you run a Debian based linux distro install from the command line with:   
> sudo apt-get install qemu  
  
Make sure you read the quickstart guide before you do anything else: [here](https://github.com/limboemu/limbo/wiki/Quickstart)  
  
***

## Downloads  
** If you're upgrading to version 4 from version 2 or 3 you have to **uninstall** and do a **fresh install**. Make sure you **export** your virtual machines before you uninstall and then **re-import** them.

﻿Download Limbo 4.1.0 for **ARM devices** (most phones and tablets)  
  ​
  
Limbo ARM Emulator  
[limbo-android-arm-ARM.4.1.0.apk](https://drive.google.com/uc?export=download&id=1xJjY38z7qDha8m0pjgYf-UKb9Wjd7Azx)

Limbo SPARC Emulator   
[limbo-android-sparc-ARM.4.1.0.apk](https://drive.google.com/uc?export=download&id=1QjnTtrRwAJreAnOlB8Bc-9xrF4k1KyF9)  

Limbo PPC Emulator  
[limbo-android-ppc-ARM.4.1.0.apk](https://drive.google.com/uc?export=download&id=13qoS7PTowiR5VLKnyEpUMjdzPON60xj1)  

Limbo x86 PC Emulator  
[limbo-android-x86-ARM.4.1.0.apk](https://drive.google.com/uc?export=download&id=1NImRzuSi5CWYNW5qijJj5YXph1BxKyP3)  

***

Download Limbo 4.1.0 for **Intel CPU devices** (Zenfone 2, Yoga Tablet 2)  
  
  
Limbo x86 PC Emulator  
[limbo-android-x86-X86.4.1.0.apk](https://drive.google.com/uc?export=download&id=11x3Vkl2EaSbk0QiQheP1jNHINgIlh5ld)  

Limbo ARM Emulator  
[limbo-android-arm-X86.4.1.0.apk](https://drive.google.com/uc?export=download&id=1ONJszj16lHZx29m3osR-tTIJtR3Cn7mx)  
  
Limbo SPARC Emulator  
[limbo-android-sparc-X86.4.1.0.apk](https://drive.google.com/uc?export=download&id=1uqBmmnvN2be-O4_kTqiLHCsKMZntM6Dv)  
  
Limbo PPC Emulator  
[limbo-android-ppc-X86.4.1.0.apk](https://drive.google.com/uc?export=download&id=1cqj9w_xQqIs44G_i9OHDR3fQzcbpOg8r)

***

﻿Download Limbo 4.0.0 for **ARM devices** (most phones and tablets)  
  ​
  
Limbo ARM Emulator  
[limbo-android-arm-ARM.4.0.0.apk](https://drive.google.com/uc?export=download&id=1XID78k8hxEQzJqoT5LmMflm6-RDXJoR7)
  
Limbo SPARC Emulator   
[limbo-android-sparc-ARM.4.0.0.apk](https://drive.google.com/uc?export=download&id=1uRj8_g5UJlKMHv2YM24Jo0Wb9UWyhKgv)  
  
Limbo PPC Emulator  
[limbo-android-ppc-ARM.4.0.0.apk](https://drive.google.com/uc?export=download&id=1yHCOonMbvSIhYAMAaiE0KhHjpMdCJu8L)  
  
Limbo x86 PC Emulator  
[limbo-android-x86-ARM.4.0.0.apk](https://drive.google.com/uc?export=download&id=1mF1mZbuf1DHMmUoThFLHPEg8UEcPWeLW)  
  
***

Download Limbo 4.0.0 for **Intel CPU devices** (Zenfone 2, Yoga Tablet 2)  
  
  
Limbo x86 PC Emulator  
[limbo-android-x86-X86.4.0.0.apk](https://drive.google.com/uc?export=download&id=1WxCrFCdF7i2eRbsZUYp8Qi0oIBP5Qaa6)  
  
Limbo ARM Emulator  
[limbo-android-arm-X86.4.0.0.apk](https://drive.google.com/uc?export=download&id=1xOWDfcDb7UniFhwoCgvnYT7Z0K02-5-n)  
  
Limbo SPARC Emulator  
[limbo-android-sparc-X86.4.0.0.apk](https://drive.google.com/uc?export=download&id=1XrmbGmk3kExbM5MAZQ1T8XRM56KZmWKR)  
  
Limbo PPC Emulator  
[limbo-android-ppc-X86.4.0.0.apk](https://drive.google.com/uc?export=download&id=1FcaB45nlKxIBxrNCaQ3AwbRVrhoUu4ld)
  
***  

## Tools
The following android apps are recommended:  
[Juice SSH](https://play.google.com/store/apps/details?id=com.sonelli.juicessh) To connect to your vm with forward port  
[Hacker's Keyboard](https://play.google.com/store/apps/details?id=org.pocketworkstation.pckeyboard) Fully qwerty keyboard  
[Turbo Download Manager](https://play.google.com/store/apps/details?id=com.okythoos.android.tdmpro) Download fast large  ISOs and virtual hard disks.  
[ZArchiver](https://play.google.com/store/apps/details?id=ru.zdevs.zarchiver)  File Extractor for use with compressed images.  
[ES File Explorer](https://play.google.com/store/apps/details?id=com.estrongs.android.pop)  File Manager with FTP client for sharing files with the virtual machines    
  
  