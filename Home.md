### **Welcome to the Limbo PC Emulator wiki!**    

Limbo Emulator is a port of QEMU (Quick Emulator) and dependent libraries for Android Devices.  
  
Limbo Emulator can currently emulate lightweight Operating Systems for Intel based x86 PC like DSL Linux, Debian, Freedos and Others.  

Limbo Emulator is Open Source Software, you can find a copy of our source code in Github here. Although you can download compiled apk files from this site or from the Android market via other unofficial channels, we recommend downloading a copy of the original source files from our repository and compiling it yourself. You can redistribute binaries and source code as long as you abide to the license: [GPLv2.0](https://github.com/limboemu/limbo/blob/master/COPYING)  


***


Latest Release
Limbo PC Emulator ver 4.0.0

Release Notes:

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


***


Download APK here  
Screenshots: here  
Instructions & OS Guides here  
Other Compatible OSes: here  