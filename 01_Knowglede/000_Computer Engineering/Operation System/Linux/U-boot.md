Tag: #SecondBrain 
Status: #open 
Related:

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


## U-boot Command
Uboot alway try to read the ''uEnv.txt'' from the boot source, if file is not founded, it will use the default values of the "'env'" variables.

boot default == run 'bootcmd'

























---
# Reference

Wikipedia: https://en.wikipedia.org/wiki/Das_U-Boot
Repository: https://source.denx.de/u-boot/u-boot

Documentation: https://docs.u-boot.org/en/latest/

![](https://www.youtube.com/watch?v=INWghYZH3hI&t=252s)