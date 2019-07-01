DSL (Damn Small Linux) is a lightweight Operating system compatible with Limbo PC Emulator. Below are the steps to set up a hard disk image for use with Limbo and install DSL linux. You can download the DSL Linux ISO from:
http://www.damnsmalllinux.org/download.html
  
## Considerations  
**Performance:**  
DSL Linux is one of the few lightweight Desktop OSes that is supported by limbo though it is still rather slow to your expectations of Desktop PC.  
  
**Security**  
The Kernel used by DSL Linux is old and considered insecure. Additionally its package managers are not receiving any security updates. Please use at your own discretion.  

**Guide**
There is an excellent guide at https://virtualbits.weebly.com you can follow.
​  
### Known Issues  
There is an issue with QEMU and the mouse acceleration under VNC. This causes the mouse to stop before reaching the end of the screen boundaries. On a terminal within DSL Linux type "xset m 1" or add the same line at the end of your .xinitrc at your home (dsl) directory. This should disable mouse acceleration.  