Date: 2023-11-20, 08:27
Tags: #idea
Status: #open
Related: [[Bootloader]], [[Texas Instruments (TI)]], [[U-boot]], [[Linux]]

---
# How Do Embedded Processor Start

When you first flip the switch or push the button, after the first electrons start flowing and crystals start vibrating, before any Linux dmesg lines appear on any screen, there is a fundamental chicken and egg question we must answer before the CPUs in our Beaglebone or Raspberry Pi can start executing our code. How do embedded processors find and run the code they need to begin executing code? 
Join Bryan as he goes through each stage of the bootup process for an AM62 and the constraints we must work around when we first start configuring the clocks, starting the power controllers, initializing DDR, loading the firmware, and everything else we need before we can start the Linux kernel and securely wakeup our embedded system. 
At the end of this session you will be familiar with the role of each bootloader and each step of how Texas Instruments’ AM62 family of SoCs loads, verifies, and uses each bootloader stage as the CPUs work their way to the Linux prompt and running your embedded applications.



---
# References
![](https://www.youtube.com/watch?v=UvFG76qM6co)