Tags: #SecondBrain 
Status: #open
Related: [[Linux]]

---
## History & Organization:
The Yocto Project is a [Linux Foundation](https://en.wikipedia.org/wiki/Linux_Foundation) collaborative [open source](https://en.wikipedia.org/wiki/Open-source_software) project whose goal is to produce tools and processes that enable the creation of [Linux distributions](https://en.wikipedia.org/wiki/Linux_distribution) for [embedded and IoT software](https://en.wikipedia.org/wiki/Embedded_software) that are independent of the underlying architecture of the embedded hardware.
The project was announced by the Linux Foundation in 2010 and launched in March, 2011, in collaboration with 22 organizations, including [OpenEmbedded](https://en.wikipedia.org/wiki/OpenEmbedded).
From <[https://en.wikipedia.org/wiki/Yocto_Project](https://en.wikipedia.org/wiki/Yocto_Project)>


2003 - OpenEmbedded ([https://en.wikipedia.org/wiki/OpenEmbedded](https://en.wikipedia.org/wiki/OpenEmbedded)).
2004 - OpenedHand (company) work with Nokia to create the N770 WebPad using fork of OpenEmbedd. That fork called [Poky]([https://en.wikipedia.org/wiki/Pocky](https://en.wikipedia.org/wiki/Pocky)) Linux.
2008 - Intel buy out OpenedHand.
2010 - Intel and Linux Foundation create the Yocto Project based on Poky Linux.


Allow us to create a (your own) distro linux
	Collection of tools and methods enabling
	Base on technology from the OpenEmbedded project

Yocto quite small (only metadata)

**Layer:**
- BSP: defines as a MACHINE, related board-specific packages
	Contains `/conf/machine/[MACHINE].conf`
- Distribution: defines as a DISTRO, such of Poky and Angstrom
	Contain` /conf/distro/[DISTRO].conf`
- Software: everything else
	Contain neither `/conf/machine/[MACHINE].conf` or `/conf/distro/[DISTRO].conf`
	Libraries: e.g. qt5
	Language: e.g. Java
	Tools: e.g. virtualization or selinux
**Recipes:** file `*.bb`


Get yocto (Clone)7
 cmd$ . oe-init-build-env build-qemu --> (/conf)






open source projects that use Yocto:
webOS
Automotive grade linux
[[Linaro]]: https://www.linaro.org/





---
# References
Official website: 
https://www.yoctoproject.org/
https://docs.yoctoproject.org/what-i-wish-id-known.html

Wikipedia:
Youtube:
https://www.youtube.com/@TheYoctoProject

![](https://www.youtube.com/watch?v=8M8U1EgnUVw&t=55s)


![](https://www.youtube.com/watch?v=kZFiqBAnFpw)

![](https://www.youtube.com/watch?v=7JVmOM7bjaQ&t=4490s)