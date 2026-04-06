Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[Open Source]], [[Linux From Scratch]]

---

# Base Distro
Arch
CachyOS (base on Arch): https://wiki.cachyos.org/


https://wiki.archlinux.org/title/Laptop_Mode_Tools

# Window Management
- MangoWC:
	- https://github.com/mangowm/mango
	- yt guide: https://www.youtube.com/watch?v=Q1Jgw_q0gWE&t=312s
- Niri:
	- https://github.com/niri-wm/awesome-niri
	- yt guide: https://www.youtube.com/watch?v=bjalAgAVIkc&t=529s

# Battery optimize
- https://wiki.archlinux.org/title/Power_management
- https://wiki.archlinux.org/title/Power_management/Suspend_and_hibernate

Tools:
- https://github.com/TheAlexDev23/power-options

## Undervoltage
- https://wiki.archlinux.org/title/Undervolting_CPU

# Boot time
- https://wiki.archlinux.org/title/Improving_performance/Boot_process
- https://medium.com/@therealcomtom/reducing-linux-booting-time-b5d0a061e05a

# Moderm
- https://wiki.archlinux.org/title/ThinkPad_mobile_Internet

# Virtual machine
- QEMU:
	- Intall: 
		- [Lab](https://github.com/daveprowse/virtualization/blob/main/kvm/kvm-install-debian-12/kvm-install-debian-12.md)  [Deep Dive-KVM Installation to Debian 12](https://www.youtube.com/watch?v=GgAQw08zJzs)
		- https://sysguides.com/install-kvm-on-linux/
		- https://www.youtube.com/watch?v=GgAQw08zJzs
		- https://christitus.com/vm-setup-in-linux/
	- https://christitus.com/windows-inside-linux/
	- https://sysguides.com/install-windows-11-on-kvm
	- Virtual IO
		- https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/
		- https://pve.proxmox.com/wiki/Windows_VirtIO_Drivers
		- Bug:
			- https://ostechnix.com/solved-cannot-access-storage-file-permission-denied-error-in-kvm-libvirt/
	Wiki:
	- https://www.qemu.org/
	- https://wiki.archlinux.org/title/QEMU

# Browser 
- Refer browser:
	- thorium: 
	- zen: https://github.com/zen-browser/desktop

- Enable GPU acceleration 
	- https://wiki.archlinux.org/title/Chromium#Force_GPU_acceleration
- Put Web running in RAM: [yt/link](https://www.youtube.com/watch?v=tGS6qkjv4oM&t=618s)
	- https://wiki.archlinux.org/title/Profile-sync-daemon (refer guide)
		https://wiki.archlinux.org/title/Chromium#Cache_in_tmpfs
		https://wiki.archlinux.org/title/Firefox/Profile_on_RAM

# AUR helper
- https://wiki.archlinux.org/title/AUR_helpers


# Default apps
- https://wiki.archlinux.org/title/Default_applications


# Network

# Share network

https://wiki.archlinux.org/title/Samba

**Avahi-daemon**: The  Avahi  mDNS/DNS-SD daemon implements Apple's Zeroconf architecture. The daemon registers local IP addresses and static services using mDNS/DNS-SD and provides two IPC APIs for local programs to make use of the mDNS record cache the avahi-daemon maintains. First there is the so called "simple protocol"  which is  used  exclusively by avahi-dnsconfd (a daemon which configures unicast DNS servers using server info published via mDNS) and nss-mdns (a libc NSS plugin, providing name resolution via mDNS). Finally there is the D-Bus interface which provides a rich object oriented interface to D-Bus enabled applications.
Upon startup avahi-daemon interprets its configuration file /etc/avahi/avahi-daemon.conf and reads XML fragments  from /etc/avahi/services/*.service  which may define static DNS-SD services. If you enable publish-resolv-conf-dns-servers in avahi-daemon.conf the file /etc/resolv.conf will be read, too.

`smbclient //truenas.local/folderShared/ -U vdung`

mount:
Package: gvfsd-smb
`gio mount smb://truenas.local/folderShared`
`mount at /run/user/1000/gvfs/smb-share:server=...`


# File manager
- https://wiki.archlinux.org/title/Lf

# Screenshot
flameshot: https://flameshot.org/docs/guide/faq/






# Optimization



---
# References
Official website:
Wikipedia:
Youtube: