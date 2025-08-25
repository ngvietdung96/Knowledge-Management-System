Date: 2023-12-06, 07:32
Tags: #idea
Status: #open
Related: [[Operation System]], [[UNIX]], [[RISC-V]]

---
# xv6 Kernel
A study OS build for learning and understand basic concept about kernel. 
Run on RISC emulation.

**Introduction:**
![](https://www.youtube.com/watch?v=ktkAlbcoz7o)

UNIX Operation system
Education - MIT
Implementation
	RISCV
	Multicore
	~6000 line of code

https://www.youtube.com/watch?v=fWUJKH0RNFE
## Shell Program of xv6 Operation System
https://www.youtube.com/watch?v=ubt-UjcQUYg&list=PLbtzT1TYeoMhF4hcpEiCsOeN13zqrzBJq


https://github.com/mit-pdos/xv6-riscv
![](https://www.youtube.com/watch?v=KkenLT8S9Hs&list=PLP29wDx6QmW4Mw8mgvP87Zk33LRcKA9bl)

Entry.S mention in *linker file*.

Machine mode
Supervisor mode
User mode

OS
time slide interrupt


## Build xv6

Issue Compile Error :
MakeFile: Compile CFLAG with `-Werror`
Compiler will be failed, because of "mp.c" file will do "magic thing on array pointer" 
`[-Werror=array-bounds]`

Mitigation:
Remove CFLAG `-Werror` or add flag `-Wno-array-bounds`

### xv6-riscv
Compiler require speccial prefix:
`# riscv64-unknown-elf-` or `riscv64-linux-gnu-`
`# perhaps in /opt/riscv/bin`
`# TOOLPREFIX =`

Compile: need to build `riscv64-unknow-elf-` in source [https://github.com/riscv/riscv-gnu-toolchain](https://github.com/riscv/riscv-gnu-toolchain)

Default program build in `/opt/riscv/bin`

QEMU: need package "qemu-system-riscv64" (debian is "qemu-system-misc")
BUILD: with parameter
CMD: `make TOOLPREFIX=/opt/riscv/bin/riscv64-unknow-elf-`
--> `riscv64-unknow-elf-`
[https://github.com/riscv-collab/riscv-gnu-toolchain](https://github.com/riscv-collab/riscv-gnu-toolchain) --> build the compiler for riscv64


---
# References
Official website: https://pdos.csail.mit.edu/6.1810/2023/xv6.html
Wikipedia:
Youtube: 
	About of Channel: https://www.youtube.com/@hhp3
	He is in Department of Computer Science at Portland State University.
Book: [[book-XV6-riscv-rev3.pdf]]