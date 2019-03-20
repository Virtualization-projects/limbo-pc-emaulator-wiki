Current Release: 4.0.0  
Source Code  
Source Code can be found here: https://github.com/limboemu/limbo  
  
  
Release Notes  
  
* Enabled SDL scaling with linear algorithm
* Fixed loading native libraries for 64 bit hosts
* VNC and SDL 1-1 screen mode is now centered
* Emulated SD Drive is now available only for ARM
* Desktop Mode is now global setting
* Fixed issue with VNC 24bit color on Samsung phones showing black screen
* Standardized VNC port for better compatibility with external clients
* Added Calibration Fix for VNC Mouse
* Mouse, Keyboard, MTTCG, and KVM are now Machine option (not global)
* New option Disable TSC for OSes that hang or kernel panic (set by default)
* Some machine options have changed default values (ie network is disable by default)
* New expand/collapse user interface for main screen.
* Formatted display path for disk image files
* Enabled fallback file manager for Android devices that don't support Android Storage Framework (no SD Card support)
* Shared folder is now configurable (SD Card still not supported)
* Added reconnect option for VNC
* VNC client resize automatically when VM resolution changes
* Added/Rearranged some additional CPU and Machine specs across emulators
* Added internal log viewer
* Fixed issue with virtual disk files containing percent symbol
* QEMU monitor is now resized automatically
* Fixed issue with crashing and/or corrupting vm states after pause is complete
* Fixed emulated SD card for ARM emulator
* Maximum number of virtual CPUs is now 8
* Maximum machine RAM is now 2GB
* Logging now starts capturing output early
* Log File is now saved internally with "Copy To" option
* Limbo generated files are now all saved under internal private storage,
* Virtual disks images can still be loaded from external storage or SD Card
* Added description for emulated mouse usb-tablet (this fixes VNC mouse issues)
* Mouse usb-tablet is not supported by all Guest OSes
* Added icons for Legacy file manager
* Added icons for Drives dialog box
* Reduced message errors for QMP client
* Early support for double tap/hold touchpad mode
* Early support for x86 guest MTTCG (qemu 3.1.0)
* New build environemnt read README.developers for changes to makefiles
* Reduced JNI internal configuration files and makefiles
* Default build sdk version is now api 26, minimum api continues to be 21
  
  
Known Issues:  
Mouse acceleration issues in QEMU VNC (see guide for disabling it)  
Emulated audio is slow  

Work in progress  
N/A  
  
  
If you want to follow the guides and setup your OS images you should also install Qemu for Windows and Linux:  
  
Qemu with GTK (GUI) for Windows Make sure you download a version with GTK if you want a GUI.  
Qemu Manager (GUI) for Windows  
  
If you have Ubuntu or if you run a Debian based linux distro install from the command line with:   
sudo apt-get install qemu  
  
Make sure you read the quickstart guide before you do anything else: here  
  
﻿Download Limbo 4.0.0 for ARM devices (most phones and tablets)  
  ​
Limbo ARM Emulator
limbo-android-arm-ARM.4.0.0.apk
  
Limbo SPARC Emulator  
limbo-android-sparc-ARM.4.0.0.apk  
  
Limbo PPC Emulator  
limbo-android-ppc-ARM.4.0.0.apk  
  
Limbo x86 PC Emulator  
limbo-android-x86-ARM.4.0.0.apk  
  
Download Limbo 4.0.0 for Intel CPU devices (Zenfone 2, Yoga Tablet 2)  
  
Limbo x86 PC Emulator  
limbo-android-x86-X86.4.0.0.apk  
  
Limbo ARM Emulator  
limbo-android-arm-X86.4.0.0.apk  
  
Limbo SPARC Emulator  
limbo-android-sparc-X86.4.0.0.apk  
  
Limbo PPC Emulator  
limbo-android-ppc-X86.4.0.0.apk  
  