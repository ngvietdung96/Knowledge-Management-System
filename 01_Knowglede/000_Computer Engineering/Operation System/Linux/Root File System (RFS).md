
# About RFS

In this lecture let’s discuss about the Root File System(RFS) and its directory structure. 

Later videos in this course will show you how you can create your own root file system by using **busybox and buildroot** and we can also test it on the hardware. 

Now the root file system, as the name indicates, it’s a file system which Linux mounts to the "/" (root)

File system is nothing but a collection of files organized in standard folder structure. 

Yes!!! There is a standard for the Linux file system. That is called **_"File system Hierarchy Standard"_**

You  may have to check this document if you are interested. 

[https://wiki.Linuxfoundation.org/lsb/fhs-30](https://wiki.linuxfoundation.org/lsb/fhs-30)
[https://en.wikipedia.org/wiki/File system_Hierarchy_Standard#cite_note-2](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard#cite_note-2)

In a typical file system you will find the below folder structure, even though all these folders are not required for Linux to boot and mount the file system successfully. 
Now, let’s understand what the purpose of each folder is and what exactly it contains. 

The official documentation of the FHS says this about the directories present in the "/"
[http://refspecs.Linuxfoundation.org/FHS_3.0/fhs/ch03s02.html](http://refspecs.linuxfoundation.org/FHS_3.0/fhs/ch03s02.html)


|**Directory**|**Description**|
|:--|:--|
|bin|Essential command binaries|
|boot|Static files of the boot loader|
|dev|Device files|
|etc|Host-specific system configuration|
|lib|Essential shared libraries and kernel modules|
|media|Mount point for removable media|
|mnt|Mount point for mounting a file system temporarily|
|opt|Add-on application software packages|
|run|Data relevant to running processes|
|sbin|Essential system binaries|
|srv|Data for services provided by this system|
|tmp|Temporary files|
|usr|Secondary hierarchy|
|var|Variable data|

## bin/ :

This directory contains **binaries** of Linux commands which are used by both the system admins and users.

You don’t need privileges from your System admin to execute these commands neither you need root access. Remember that this folder will not contain binaries for all the Linux commands. There is a restriction on what types of commands have to be placed in this directory, because these binaries can be executed by the common user. 

Below are some the commands you will find it in the **bin/** directory. 

|**Command**|**Description**|
|:--|:--|
|cat|Utility to concatenate files to standard output|
|chgrp|Utility to change file group ownership|
|chmod|Utility to change file access permissions|
|chown|Utility to change file owner and group|
|cp|Utility to copy files and directories|
|date|Utility to print or set the system data and time|
|dd|Utility to convert and copy a file|
|df|Utility to report file system disk space usage|
|dmesg|Utility to print or control the kernel message buffer|
|echo|Utility to display a line of text|
|false|Utility to do nothing, unsuccessfully|
|hostname|Utility to show or set the system's host name|
|kill|Utility to send signals to processes|
|ln|Utility to make links between files|
|login|Utility to begin a session on the system|
|ls|Utility to list directory contents|
|mkdir|Utility to make directories|
|mknod|Utility to make block or character special files|
|more|Utility to page through text|
|mount|Utility to mount a file system|
|mv|Utility to move/rename files|
|ps|Utility to report process status|
|pwd|Utility to print name of current working directory|

_you can see that commands related to "repairing", "recovering", "restoring", "network configuration" ,”modules install remove”  are not found in this directory._ 
## boot/:

This directory contains the boot related files, which are required to boot the Linux. This directory may be read by the boot loader to read the boot images like Linux kernel image, dtb, vmLinux, initramfs, etc. 

So this directory may be accessed by boot loader even before the kernel boots and mounts the file system. 

## dev/:

This is the place where you can find the **"device files”.**
You may be heard or read this statement **_"in unix/Linux devices are treated like file access" ._**
Yes, if you want to access any i/o, networking devices, memory devices, serial devices, parallel devices, input output devices such as keyboard, mouse, display, everything will be treated like a file.
So, this directory will have the file entry for every device

For example: the i2c devices may have a file entries like this 
**/dev/i2c-0 ,**
**/dev/i2c-1,**

The user Space application can use this device files to access those devices .
The ram may have a device file entry like **/dev/ram0**

The 2 partitions of the SD card may have entries like this:
**/dev/mmcblk0p1**
**/dev/mmcblkop2.**

The serial devices may have entries like this:
**/dev/ttyS0,**
**/dev/ttyS1,**
**/dev/ttyO0** 

It’s the responsibility of the respective drivers to populate this directory with the device files 

## etc/ :
This is the place where all the start-up scripts, networking scripts, scripts to start and stop networking protocols like NFS, networking configuration files,  different run level scripts will be stored. 

1) Contains run level scripts, which will be used during different run levels
2) Contains start-up and shutdown scripts
3) Contains various scripts related to services like start/stop networking, start/stop NFS, etc 
4) Contains various configuration files, like passwd, hostinfo, etc. 
5) Contains various network configuration files

## lib/ :
The major contents of this directory are 
1) The dynamically loadable kernel modules.  ( later you will see, when we compile the kernel modules and when we run “modules install” command , all the kernel modules will go and sit in this directory under the sub directory "modules" .)
2) To store the Essential shared libraries (_.so_.*) for dynamic linking.

for example, 'C' shared library(libc), math library, python libray, etc,

## media/ :
This is the mount point for the removable media like your USB flash drive, SD cards, camera, cell phone memory, etc .
For example, when i connect my SD card to the PC, there will be 2 device files will be created for each partition **1) /dev/sdb1 and 2) /dev/sdb2**
and theses 2 device files are automatically mounted under the **/media** directory. So that i can access those 2 partitions just like folders. 

Some examples:-
/media/cdrom for CD-ROM  
/media/your usb flash driver name

### mnt/ :
This is the place where you can mount the temporary file system. 
The system admins can use a Linux commands to temporarily mount and un-mount the file system, if they want to transfer any file. 

### opt/ :
"opt" stands for "optional"
This directory will be used when you install any software packages for your Linux distribution. 

For example if i run the command apt-get install **some packages name** then the package will be installed in this directory. 

### sbin/ :

The commands which come in the category of system administration will be stored in this directory, which is used by your sys admins for the purpose of networking configurations, repairing, restoring and recovering .

may be **sbin** stands for "**System Admin's bin**" ??

It also has root only command and need privileges to execute those commands. 

These are the commands which  you will find in **sbin/**

|**Command** |**Description** | 
|:--|:--|
|fastboot|Reboot the system without checking the disks (optional)|
|fasthalt|Stop the system without checking the disks (optional)|
|fdisk|Partition table manipulator (optional)|
|fsck|File system check and repair utility (optional)|
|fsck.* |File system check and repair utility for a specific file system (optional)|
|getty|The getty program (optional)|
|halt|Command to stop the system (optional)|
|ifconfig|Configure a network interface (optional)|
|init|Initial process (optional)|
|mkfs|Command to build a file system (optional)|
|mkfs.* |Command to build a specific file system (optional)|
|mkswap|Command to set up a swap area (optional)|
|reboot|Command to reboot the system (optional)|
|route|IP routing table utility (optional)|
|swapon|Enable paging and swapping (optional)|
|swapoff|Disable paging and swapping (optional)|
|update|Daemon to periodically flush file system buffers (optional)|

### home/:

The **/home** directory contains a home folder for each user.
Each user only has write access to their own home folder and must obtain elevated permissions (become the root user) to modify other files on the system.
This directory will be used to store personal data of the user . 

In a single user mode you may have folder like this 
/home/ramesh

In a multiple user mode, you may have folder dedicated to each user. 
/home/ramesh,  /home/suresh, /home/ram etc. 

### srv/ :
**SRV stands for "Service"**
The **/srv** directory contains **“data for services provided by the system**.” If you are using the Apache HTTP server to serve a website, you’d likely store your website’s files in a directory inside the /srv directory.

### tmp/ :
Applications store temporary files in the /tmp directory.

### usr/ :
According to FHS, it’s a "secondary hierarchy", the **usr/** directory may contain the below sub directories 

|**Directory**|**Description**|
|:--|:--|
|bin |Most user commands|
|include |Header files included by C programs|
|lib |Libraries|
|local |Local hierarchy (empty after main installation)|
|sbin |Non-vital system binaries|
|share |Architecture-independent data|

**/usr/bin** contains binary of the commands for user programs

For example, if you have firefox on your system then just check it must be available under **"/usr/bin"** not under **/bin**. Because it is a binary related to user installed programs, similarly, **"zip"** command also you will find it under **/usr/bin.** 

**/usr/sbin** contains, again privileged commands which may be used by the system admins, but these commands are for system administration purposes. 

**/usr/include** will hold the header files which will be included from the C programs you write.

**/usb/lib** will again hold the shared libraries, linker/loader files , which enable your **/usb/bin** and /**usr/sbin** commands to execute. 

For more information you may check this official link:
http://refspecs.linuxfoundation.org/FHS_3.0/fhs/ch03.html