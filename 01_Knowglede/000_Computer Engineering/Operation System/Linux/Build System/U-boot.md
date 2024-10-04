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





---
# Reference

Wikipedia: https://en.wikipedia.org/wiki/Das_U-Boot
Repository: https://source.denx.de/u-boot/u-boot

Documentation: https://docs.u-boot.org/en/latest/

![](https://www.youtube.com/watch?v=INWghYZH3hI&t=252s)