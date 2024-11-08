Tags: #SecondBrain 
Status: #open, #unprocessed
Related: 

---
# Initial RAM based file system (Initramfs)

## About initramfs and creating initramfs

**What is initramfs ?**

 The word "initramfs" is made up of three words _"initial" "RAM_ _based" "file system"_

This is nothing but a file system hierarchy (which you just studied in the last lecture, all those directory structure), made to live in the RAM of the device by compressing it _(we use compression because RAM is precious, we cannot use whole RAM just to store the FS)_ and during booting, Linux mounts this file system as the initial file system.  That means you just need RAM to mount the FS and get going with the complete boot Process. 

**Does that mean usage of initramfs is compulsory? Used everywhere, every time ?**

 No, not necessarily. Using initramfs is optional.

**So, why do we need initramfs ?**

 Let’s understand this with an example. 

Let’s say you have a product and your product has USB interfaces, mass storage devices like SD card and let’s say you also have networking peripherals like Ethernet and also display. 

Now, to operate this wide range of peripherals, all the device drivers must be in place right?

That means all the drivers must be loaded in to the kernel space.

And along with the drivers, some peripherals may require the firmware binaries to operate. 

One idea is make sure that all those drivers are **“built in”** in to the kernel, that’s not a great idea because that makes your Linux kernel specific to your product and it will drastically increase the Linux kernel image size. 

Another good way is, you come up with the minimal file system, where you store all your drivers and firmware, and load that FS in to the RAM and ask the Linux to mount that file system during boot( Thanks to kernel boot arguments , you can use the kernel boot arguments to indicate kernel that your FS resides in RAM )

When the kernel mounts that file system from RAM, it loads all the required drivers for your product and all the peripherals of your product are ready to operate, because the drivers are in place. 

after That you can even get rid of this RAM based file system and use (switch to) some other advanced file system which resides on your other memory devices like eMMC/SD card or even you can mount from the network. 

**_So, basically initramfs embedded into the kernel and loaded at an early stage of the boot process_**, where it gives all the minimal requirements to boot the Linux kernel successfully on the board just from RAM without worrying about other peripherals. And what you should store in initramfs is left to your product requirements, you may store all the important drivers and firmware, you may keep your product specific scripts, early graphic display logos, etc. 

**How to keep initramfs in to RAM?**

 There are 2 ways, 

1) You can make initramfs “built in” in to the Linux Kernel during compilation ( i will show you later in this course) , so when the Linux starts booting , it will place the initramfs in the RAM and mounts as the initial root file system and continues.

2) You can load the initramfs from some other sources in to the RAM of your board and tell the Linux Kernel about it (that is , at  what RAM address initramfs is present ) via the kernel boot arguments.




---
# References
Official website:
Wikipedia:
Youtube: