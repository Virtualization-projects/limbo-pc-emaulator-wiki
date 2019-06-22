# KVM support for Limbo
This is a guide for making Limbo running guest OSes in nearly native speed leveraging KVM.

# Step 1
## x86 KVM Android kernel
Limbo fully supports KVM for Android-x86 OS. Android-x86 project is a port of Android for x86 devices like PCs and Laptops. ISOs and other downloads can be found in https://osdn.net/projects/android-x86/releases/65697.
Android-x86 version 5.1 already contains support for KVM so you can download the ISO, burn it in a CD, and use it to boot your PC computer. If you don't want to install it in your hard disk you can instead run the live CD option selecting it  from the menu. You can now move to step 2.

## ARM Android kernel
Limbo is currently NOT tested under KVM for Android ARM devices. This is a short guide to help you compile KVM support for your Android ARM device kernel and share your findings. Keep in mind the example below is specific for Samsung Galaxy S8 your device might need different options. Additionally, you will need to flash the resulting boot image into your device and perhaps you also need to disable the secure boot depending on your Android ARM device. Proceed only if you know what you're doing and at your own risk.

### Samsung Galaxy S8
You will need an Ubuntu OS and the Android NDK toolchain to compile the kernel with KVM support. 
The Android NDK toolchain can be found in https://developer.android.com/ndk/downloads.
If newer NDK versions error during compilation make sure you are using the correct version. To download archived versions go to https://developer.android.com/ndk/downloads/older_releases.

Go to Samsung Open Source center: http://opensource.samsung.com/
and search for:
s8 or g950F
There might be multiple archives, make sure you download the correct one for your device.
Download the zip file and extract it somewhere in your home directory.

Open the defconfig file exynos8895-dreamlte_defconfig and add these options with a text editor:
```
CONFIG_VIRTUALIZATION=y 
CONFIG_KVM=y 
```

These options might also be needed
```
CONFIG_KVM_MMIO=y 
CONFIG_KVM_ARM_HOST=y 
```

Now you can start building the kernel from the command line.
Make sure you're under the top level folder and type these commands:
```
export ARCH=arm64 
export CROSS_COMPILE=PATH_TO_NDK/android-ndk-NDK_VERSION/toolchains/aarch64-linux-android-TOOLCHAIN_VERSION/prebuilt/linux-x86_64/bin/aarch64-linux-android- 
make clean 
make mrproper 
make exynos8895-dreamlte_defconfig 
make menuconfig 
make 
```

# Step 2
Once Android boots up open the android terminal and make sure you have the device file /dev/kvm exists and has appropriate file permissions:
```
ls /dev/kvm
chmod 666 /dev/kvm
```

# Step 3
Now install the appropriate Limbo emulator supporting your host Architecture. The host and the guest architecture should be the same for example if you have a PC with Android-x86 and want to boot DSL Linux you will need to install the Limbo x86 PC Emulator for x86 devices.

# Step 4
Finally you can create a virtual machine inside Limbo and enable the KVM option under the "CPU/Board" section. Load a compatible ISO for x86 like DSL Linux and complete the configuration for your virtual machine. Start your VM. If all goes well you should be able to have a running in nearly native speed.