# Limbo Quickstart  
​  
This is a quickstart guide that explains most of Limbo features and frontend functionality.  
  
  
Limbo is a Emulator for Android device powered by QEMU and depend libraries. It allows you to run Desktop PC operating systems with emulated peripheral devices. It is compatible with small lightweight operating system. To see a list of compatible OSes click under Guides from the top menu.  

Large operating systems might not work at all or be very slow so it is recommended to always use a SD card to run your guest operating system. The reason is that large operating systems use a lot of memory and might be stressing your device storage. So Make Sure you use an External SD Card to run your virtual Hard Disk and CD ROM images from.  
  
## Features  
Limbo provides following emulation Capabilities via its front end:  
  
* CPU (x86,x86 64bit, ARM, Sparc, PowerPC)  
* Memory (up to 2GB)  
* Hard Drives (IDE/SCSI up to 4)  
* CDRom (IDE, 3 hard drives if used)  
* Floppy Drives (up to 2)  
* SD Card (only image files, does NOT support external SD Card)  
* VGA (standard, SVGA cirrus, SVGA VM Ware)  
* Audio (choppy only suport under SDL interface)  
* Network (functional under User mode, TAP not supported)  
  ​
  
By now you should have installed Limbo if not click [here](https://github.com/limboemu/limbo/wiki/Downloads) to download and install.  
  
## GUI (Graphical User Interface)  
Limbo provides a VNC interface and a native SDL interface to render the graphics. The main differences between the two interfaces are outlined below.  
  
### VNC Interface:  
Slow UI Interaction  
Runs Limbo in a Service mode  
Guest OS is running even in the background  
Mouse acceleration issue with screen boundaries  
  
### SDL Interface  
Faster UI interaction  
Limbo is run only on the foreground  
Pauses when in the background  


## Architecture Configuration  
  
The following architecture machines are supported:  
  
**Intel x86 32 and 64 bit  **
This is the most common architecture that people use to get Linux and other operating systems.  
  
**ARM 32 and 64bit  **
You can run Linux operatings systems for ARM CPUs like Debian Linux for ARM for boards like Raspberry Pi.    
​
Sparc  
You can boot and run many older operating system like Oracle Solaris.  
  
PowerPC  
Some people have been successful in running Debian Linux for Power PC  
  
## Network Configuration  
Limbo supports 2 modes for providing network and internet capabilities to the Guest machine:  
  
### User:
This mode supports NAT and provides internal ip address. Event though the guest OS is under a internal network, you should always operate Limbo under a network that you trust.  
  
### TAP (not supported currently)
Mode provides a bridge to the external network (Wifi) with a separate ip address from your phone. This mode is only available for rooted Android devices with a TAP device already configured. If you can't setup a TAP device or don't have a rooted you should use the User mode above.  
  
**Notes:**
Currently Limbo doesn't read the DNS  settings of your phone though you can configure the DNS address for the Guest OS from the Limbo Console under the box "DNS Address". As default it's set to the Google public DNS server: 8.8.8.8.  
  
## VGA Configuration
Limbo provides VGA emulation via QEMU under the following VGA modes:  
  
**std (standard)**  
Standard VGA.  
  
**Cirrus (Cirrus Logic)**  
Super VGA  
  
**VM Ware**  
Super VGA.  
   
**Note:**  
For most OSes It is recommended to use standard vga (std) for better performance and compatibility with your guest OS. Try reducing the Display Resolution within the VM for better results. You may wish to switch to a 1-1 display mode to remove any scaling effects. To do that tap the monitor icon from the top menu and choose "Display Mode" / "Normal (One-To-One)".  
  
Limbo Emulator can run faster under VNC Mode if you change to a 256 color mode. To do that tap the monitor icon from the top menu and choose "Color Mode" / "256 colors (1bpp).  
  
## Peripherals  
### Keyboard:
You can use any kind of Android soft keyboard from the market.  
Recommended: Hacker's Keyboard  
Also Physical Hardware keyboards (slide phones or external Bluetooth keyboards might be supported (not tested fully))  

**Note:**  
Only US Keyboard layout is currently supported though you may try using another layout by entering the following option in the advanced paramaters (Limbo bottom main screen). For example for German enter:  
-k de  
  
### Mouse:
Trackpad mode is supported (Double tap to enable).  
Touch screen mode is not fully supported but you can try choosing "usb table" mouse under the User Interface section in Limbo, start the VM, then from within the VM tap on the mouse icon and choose "Desktop Mode". Make sure that the VM resolution can fit in your screen, if not reduce the VM resolution.  
  
## Hard Drives/CD ROM  
You can attach up to 4 hard disk images to Limbo as IDE. You can also attach a CD ROM iso image if you wish though it will use one of the 4 slots reserved for the hard disks.  
  
Image formats supported:  
* img (raw)
* qcow/qcow2 (QEMU disk format)
* vdi (Virtual Box disk format)
* ​vmdk (VM Ware disk format)
* ​vpc (Virtual PC disk format)
* vhd/vhdx (Hyper V disk format)
  
**Note:**   
If you use an older versions of Limbo Emulator and want to pause the VM and resume it you need to convert any preexisting images to qcow2 format. You can do this using the qemu-img binary in Linux, Windows, or Mac from the terminal like so:  
qemu-img convert -f raw -O qcow2 oldimage.img newimage.qcow2  
  
In any case it is recommended to use the qcow2 since it's natively supported by QEMU. You can also create new HD virtual images from within Limbo Emulator: tap on a Hard Drive drop down list (enable it from the left check box if you use newest versions of Limbo) and choose new, then select the size of the hard disk and choose its directory.  
  
## Advanced Configuration  
* Disable ACPI (some Guest OSes don't work well with ACPI)
* Disable HPET
* Disable FD Boot Check
* Higher Priority (Some time might provide faster performance)
* Reverse Display (Only for DSL interface, currently not supported)
  
## Sound Configuration  
Only for SDL Interface and very choppy (Currently not supported)  
  
Sound Cards emulated:  
* sb16
* adlib
* es1370
* ac97
  
**Note:**  
Playing MP3 files and other encoders within the virtual machine might not run well at all. Playback of wav files have better performance. Other sounds by the Desktop OS you're running might considerably reduce the performance so it's best to disable this option.  
  
## VM State  
You can save the Virtual Machine state to a file and resume later. This is a great feature so your virtual machine doesn't have to boot again from the start.  
  
**Note:**  
Saving the VM state doesn't work with certain hard disk images or the "Shared Folder" option. The best choice is to use qcow2 images which are fully supported.  
  