Tag: #MapOfContents 
Status: #open 
Related: [[Microcontroller]]

---
# UEFI/GPT and BIOS/MBR
# Partition Table
- Old - MRB support volumes is limit to 2TB.
- New - GPT (GUID Partition Table) support volumes much larger than 2TB (up to 9.4 ZB)

# Firmware Interface
## UEFI (Unified Extensible Firmware Interface)
- https://uefi.org/specifications
- https://www.tianocore.org/: 
	- Community supporting an open source implementation of the UEFI.
	- Document training: https://github.com/tianocore/tianocore.github.io/wiki
- Collection book of UEFI: https://github.com/vincentjzimmer/Documents
	- 2011-vol15-iss-1-intel-technology-journal.pdf


# Window bootloader
- Document: Microsoft start up phase [link](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/windows-boot-issues-troubleshooting)

## Open Source Window bootloader
- https://reactos.org/ AND https://github.com/reactos/reactos
- NT family of operating systems (NT4, 2000, XP, 2003, Vista, 7).
## Secure Boot (window)
- Doc: [link](https://learn.microsoft.com/en-us/windows/security/operating-system-security/system-security/secure-the-windows-10-boot-process)


# Embedded linux
[[U-boot]]
[[Buildroot]]


![](https://www.youtube.com/watch?v=Jcan8YfLfLs)



# USB flashing
[USB Flashing Format (UF2)](https://github.com/microsoft/uf2)

# Ventoy
https://github.com/ventoy/Ventoy
Ventoy is an open source tool to create bootable USB drive for ISO/WIM/IMG/VHD(x)/EFI files.  
With Ventoy, you don't need to format the disk over and over, just copy the image files to the USB drive and boot them. You can copy many image files at a time and Ventoy will give you a boot menu to select them.