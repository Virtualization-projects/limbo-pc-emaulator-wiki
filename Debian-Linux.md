# Debian Linux  
  
Debian Sarge is recommended since it's based on a Kernel 2.4 which is not very demanding on resources:  
You can download the ISO business card cdrom or try to do a netinst CD installation  
You can find all the images below:  
https://www.debian.org/releases/sarge/debian-installer  
  
​  
## Net Install  
Netinst (Net Installation)  
You can create a new Hard Disk image and install it on your device directly on do the prework on your Desktop computer. If you choose the later you will need QEMU.  
    
**For windows:**  
Download Qemu Manager or QEMU for windows  
  
**For Linux:**  
Download with:  
> apt-get install qemu-system-arm  
​  
Start qemu on your desktop with these settings:
* Arch: x86
* Machine: PC
* Memory: 256
* CD: debian-31r8-i386-netinst.iso
* HDA: debian-31.qcow2 (create a new disk with qcow2 as the format with a size of 20 GB)
* vga: cirrus (Cirrus Logic)
* net: User
* Nic: ne2k-pci
  ​
Hit Start.  
  
**When Prompted:**  
Keyboard: choose US Keyboard and English (others may not be supported by Limbo)
Language: English
Disk: Use recommended settings for new users
Grub Install: Choose Yes on the Master Boot Record
Follow instructions and complete download and installation.
When asked to finish installation and reboot (press continue)
After reboot complete the steps for post installation.  
  
When configuring apt-get choose to edit the sources manually (file /etc/apt/sources.list)  
  
Make sure the following lines are present:  
> deb http://archive.debian.org/debian/ sarge main non-free contrib  
> deb http://archive.debian.org/debian-security/ sarge/updates main non-free contrib  
  
NOTE: remove all other lines (ie oldstable)

Make sure you work all the way through the rest of the configuration process.
When you asked for packages DO NOT install the Desktop Environment (we'll do that later).
Don't select any manual packages either just choose OK and press enter.

You can skip the Mail configuration.
Choose the Finish Configuring Base packages.
​You're done


**Business Card ISO**
If you want to run debian from a Business card ISO:  
Download here. Web site: https://www.debian.org/releases/sarge/debian-installer  
  
Move the iso image to your external sd card on your device.  
Create new VM from Limbo  
Open the ISO as CDROM  
tap on "Start"  
  
**Desktop Manager**
If you want to install a desktop manager like icewm otherwise skip below
Desktop (optional)
icewm installation guide:
> apt-get update
> apt-get install icewm
> apt-get install x-window-system
  
Follow the instructions on the screen and choose default values.  
Use auto probing when available.  
Make sure that mouse is detected as ImPS2  
  
Now you can start the desktop by typing:
> startx

Note: You can install other windows managers also:
> apt-get install fluxbox
> apt-get install xfce4​
> apt-get install gnome

If you don't want the graphical login in the beginning then type:
> apt-get remove xfce4 xdm gdm  

The above will just uninstall the login managers not the desktop managers

To uninstall a desktop manager:
> apt-get remove icewm*
> apt-get remove fluxbox*
> apt-get remove xfce*
> apt-get remove gnome*
​  
## Preinstalled Hard Disk Images
If you want to you can download a ready made hard disk image [here](http://virtualboxes.org/images/debian/)(Choose Debian 3.1).