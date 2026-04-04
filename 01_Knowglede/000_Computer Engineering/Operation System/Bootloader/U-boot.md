Tag: #SecondBrain 
Status: #open 
Related: [[Cross Compiler]], [[Linux]], [[Device tree]], [[Root File System (RFS)]]

---
**Das U-Boot** (often shortened to U-boot) is an [[Open Source]] [[Bootloader]] used in [[Embedded Engineering | embedded device]] to perform various low-level HW initialization tasks and boot the device's operation system kernel. 
It is available for a number of [[Computer architecture]]: ARM, RISC-V, x86, MIPS, ...

## Functionality:
U-Boot is both a first-stage and second-stage bootloader. It is loaded by the system's ROM (e.g. on-chip ROM of an ARM CPU) from a supported boot device, such as an SD card, SATA drive, NOR flash (e.g. using SPI or I2C), or NAND flash.

If there are size constraints, U-Boot may be split into two stages: the platform would load a small SPL (Secondary Program Loader), which is a stripped-down version of U-Boot, and the SPL would do some initial hardware configuration (e.g. DRAM initialization using CPU cache as RAM) and load the larger, fully featured version of U-Boot.
Regardless of whether the SPL is used, U-Boot performs both first-stage and second-stage booting.

>[!example]
>First-stage: configuring memory controllers and SDRAM.
>
>Second-stage: Performing multiple steps to load a modern operating system from a variety of devices that must be configured, presenting a menu for users to interact with and control the boot process, etc


![[BuildUboot.png]]


## U-boot Command
Uboot alway try to read the ''uEnv.txt'' from the boot source, if file is not founded, it will use the default values of the "'env'" variables.

boot default == run 'bootcmd'


U-boot transition to Linux need below information:
- address of Linux kernel image
- address of [[Device tree]]
- Information of logging HW (UART, or USB)
- location of [[Root File System (RFS)]]


Uboot Linux Image header

UImage = Uboot header + ZImage


U-boot --> Bootstrap loader

Uboot 
	bootm.c
		boot_jump_linux call --> kernel_entry(0, machid, r2); 
			kernel_entry is pointer at address of Linux kernel
			r2 is address of Flattened Device Tree blob (fdb)

Bootstrap loader
	head.S  (/arch/arm/boot/compressed/head.s)
		Start: --> call decompress_kernel()
	misc.c
		decompress_kernel() --> head.S

Linux Kernel
	head.S  (/arch/arm/kernel/head.S) --> head-common.S
	head-common.S  (/arch/arm/kernel/head-common.S) --> start_kernel(void)
	main.c 
		start_kernel(void) -- rest_init(void)
		rest_init(void) --> start thread "kernel_init" and "kthreadd" --> start scheduler



## Build and deployment U-boot

| File        | Description                                                                                                  |
| ----------- | ------------------------------------------------------------------------------------------------------------ |
| u-boot      | elf file format, use for debug.                                                                              |
| u-boot.bin  | Executable file run on the machine                                                                           |
| u- boot.img | .bin file with header                                                                                        |
| u-boot.srec | Executable file in Motorola S-record is a file format, use for over serial connection (same with hex format) |
| MLO         | Secondary Program Loader (SPL) - option                                                                      |

Boot from USB, SD card, or eMMC :
Create 2 partitions:
1. Type FAT32, mount as "boot"
2. Type ext4, mount as "rootfs"
### QEMU
#### QEMU for ARM architecture
**Environment for compiler:**
	`ARCH=arm`
	`CROSS_COMPILE=arm-none-eabi- or arm-linux-gnueabihf-`
**Build cmd**: `make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf-`

#### QEMU for aarch64 architecture
**Environment for compiler:**
	`ARCH=arm64`
	`CROSS_COMPILE=aarch64-linux-gnu-`
**Build cmd**: `make ARCH=arm CROSS_COMPILE=aarch64-linux-gnu-`

#### Deploy on machine:
List all machine support:
	cmd: `qemu-system-arm -M ?`
Virtual machine:
	cmd: `qemu-system-arm -M virt -nographic -no-reboot -bios <u-boot.bin>`
Other machine:
	https://lnxblog.github.io/2019/02/17/uboot-arm-qemu.html



Example boot to  binary echo hello world :) 
[https://lnxblog.github.io/2019/02/17/uboot-arm-qemu.html](https://lnxblog.github.io/2019/02/17/uboot-arm-qemu.html)[https://github.com/hhdang6637/embedded_linux_skeleton/blob/master/qemu_scripts/QEMU_command.txt](https://github.com/hhdang6637/embedded_linux_skeleton/blob/master/qemu_scripts/QEMU_command.txt)
[https://interrupt.memfault.com/blog/emulating-raspberry-pi-in-qemu](https://interrupt.memfault.com/blog/emulating-raspberry-pi-in-qemu)
[https://unix.stackexchange.com/questions/747464/testing-u-boot-on-qemu-arm64-virtual-machine](https://unix.stackexchange.com/questions/747464/testing-u-boot-on-qemu-arm64-virtual-machine)
[https://ubuntu.com/server/docs/boot-arm64-virtual-machines-on-qemu](https://ubuntu.com/server/docs/boot-arm64-virtual-machines-on-qemu)

Document: u-boot/doc/board/emulation/qemu-arm.rst


---
# Reference

Wikipedia: https://en.wikipedia.org/wiki/Das_U-Boot
Repository: https://source.denx.de/u-boot/u-boot

Documentation: https://docs.u-boot.org/en/latest/

![](https://www.youtube.com/watch?v=INWghYZH3hI&t=252s)