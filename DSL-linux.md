# DSL Linux Guide  
  
DSL (Damn Small Linux) is a lightweight Operating system compatible with Limbo PCEmulator. Below are the steps to set up a hard disk image for use with Limbo and install DSL linux.  
  
  
## Considerations  
**Performance:**  
DSL Linux is one of the few lightweight Desktop OSes that is supported by limbo though it is still rather slow to your expectations of Desktop PC.  
  
**Security**  
The Kernel used by DSL Linux is old and considered insecure. Additionally its package managers are not receiving any security updates. Please use at your own discretion.  
    
Recommended Limbo Configuration​  
* Arch: x86
* Machine: pc
* CPU: n720
* Mem: 128+
* VGA: std or Cirrus
* Network: User
* ​Network Card: ne2k_pci
* Disable ACPI: yes
  
## Recommended Guest Configuration  
Set the following within the virtual guest for better performance:    
Desktop Resolution: DSL Control Panel -> 800x600x16 or lower  
Desktop Manager:  
    Start Menu -> Desktop -> Icons -> xtDesk  
    Start Menu -> Desktop -> Menu -> no Icons  
​Open .xinitrc with an editor (ie nano, or vi) and comment the following lines to reduce the processes on startup:  
​    #dillo /user/share/doc/dsl/getting_started.html &>/dev/null &  
    #torsmo 2>/dev/null &  
​  
Instead of running from the live CD you can install dsl linux on a hard disk image. Installations steps on how to do a frugal install are here  
  
  
## Utilities
DSL Linux comes with an X window manager and busybox. You can also upgrade to GNU Utils by going to 'Start Menu' -> Apps -> Tools -> "Upgrade to GNU Utils".  
  
### Package Management  
There are 3 ways to download new packages to DSL:  
* dpkg
* apt-get
* myDSL Browser
* synaptic
  
### MyDSL Browser
You can find MyDSL Browser under 'Start menu' -> 'MyDSL' -> 'MyDSL Browser'. On the main window you browse the categories or you can search for software by name / description using the 'text search' button. Keep in mind software with extension uci install temporarily and you have to reinstall next time you reboot.  
  
### aptitude  
To use aptitude onDSL Linux first you have to enable it by going to 'Start Menu' -> Apps -> Tools -> Enable Apt  
  
### Synaptic  
Synaptic is a front end for apt-get. You can find it and install it under MyDSL Browser.  
Note: Don't install synaptic via apt-get it has unmet dependencies, use MyDSL Browser instead.  
  
### Useful Tools  
Make sure you have enabled/installed the above package managers.   
  
### GCC:  
To install gcc compiler go to MYDSL Browser and find and install package gcc1-with-libs.dsl  
  
### Java:  
​you can install via apt-get:  
sudo apt-get install jdk1.1-dev  
  
### Perl:  
version 5.8.0 is pre-installed no need to install again.  
  
### Python:  
​you can install via apt-get:  
sudo apt-get install python  
  
​  
### Known Issues  
There is an issue with QEMU and the mouse acceleration under VNC. This causes the mouse to stop before reaching the end of the screen boundaries. On a terminal within DSL Linux type "xset m 1" or add the same line at the end of your .xinitrc at your home (dsl) directory. This should disable mouse acceleration.  