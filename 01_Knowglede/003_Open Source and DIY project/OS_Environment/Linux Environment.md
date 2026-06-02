Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[Open Source]], [[Linux From Scratch]]

---
Reference:
- Arch wiki
- CachyOS wiki
- Gentoo wiki
- Void linux
# Base Distro
- Arch
	- CachyOS (base on Arch): https://wiki.cachyos.org/
- Void linux: https://voidlinux.org/
- Gentoo linux: 
General
https://wiki.archlinux.org/title/Laptop_Mode_Tools
## Arch
 - CachyOS (base on Arch): https://wiki.cachyos.org/
	- CachyOS recommend: [General system tweaks](https://wiki.cachyos.org/configuration/general_system_tweaks)
> [!bug] unknow: Bellow make suppend crash
> To enable RCU Lazy, add the following parameter to your kernel [cmdline](https://wiki.cachyos.org/configuration/boot_manager_configuration/) parameters list:
> `rcutree.enable_rcu_lazy=1`
- Arch recommend: https://wiki.archlinux.org/title/Laptop_Mode_Tools

# [[Bootloader]]
- Limine bootloader: https://github.com/limine-bootloader/limine
- Grub: 
## Boot time
- https://wiki.archlinux.org/title/Improving_performance/Boot_process
- https://medium.com/@therealcomtom/reducing-linux-booting-time-b5d0a061e05a

# Desktop Environment
## Display Manager
- https://wiki.archlinux.org/title/Display_manager
- Text UI:
	- Ly: https://codeberg.org/fairyglade/ly
	- Lidm: https://github.com/javalsai/lidm
- Graphical:
	- ???
## Window Management
- X.org
	- i3wm:
		- xrandr (manage monitor)
		- rofi
	
- Wayland:
	- https://wiki.gentoo.org/wiki/List_of_software_for_Wayland
	- https://github.com/rcalixte/awesome-wayland
	- Sway:
	- MangoWC:
		- https://github.com/mangowm/mango
		- yt guide: https://www.youtube.com/watch?v=Q1Jgw_q0gWE&t=312s
	- Niri:
		- https://github.com/niri-wm/awesome-niri
		- yt guide: https://www.youtube.com/watch?v=bjalAgAVIkc&t=529s
## Clipboard
- https://wiki.archlinux.org/title/Clipboard
- https://ejmastnak.com/tutorials/arch/copy-paste/

## Fish vs Zfs
- https://fishshell.com/docs/current/language.html


# Virtual machine
- QEMU:
	- Good document (CachyOS): 
		- https://wiki.cachyos.org/virtualization/qemu_and_vmm_setup/
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
	- Chromium:
	- thorium: 
	- zen: https://github.com/zen-browser/desktop
- Enable GPU acceleration 
	- https://wiki.archlinux.org/title/Chromium#Force_GPU_acceleration
- Put Web running in RAM: [yt/link](https://www.youtube.com/watch?v=tGS6qkjv4oM&t=618s)
	- https://wiki.archlinux.org/title/Profile-sync-daemon (refer guide)
		https://wiki.archlinux.org/title/Chromium#Cache_in_tmpfs
		https://wiki.archlinux.org/title/Firefox/Profile_on_RAM
# File manager
- https://wiki.archlinux.org/title/Lf
# Screenshot
flameshot: https://flameshot.org/docs/guide/faq/

# Package manager
## AUR helper
- https://wiki.archlinux.org/title/AUR_helpers
## Default apps
- https://wiki.archlinux.org/title/Default_applications


# Network

## Share network

https://wiki.archlinux.org/title/Samba

**Avahi-daemon**: The  Avahi  mDNS/DNS-SD daemon implements Apple's Zeroconf architecture. The daemon registers local IP addresses and static services using mDNS/DNS-SD and provides two IPC APIs for local programs to make use of the mDNS record cache the avahi-daemon maintains. First there is the so called "simple protocol"  which is  used  exclusively by avahi-dnsconfd (a daemon which configures unicast DNS servers using server info published via mDNS) and nss-mdns (a libc NSS plugin, providing name resolution via mDNS). Finally there is the D-Bus interface which provides a rich object oriented interface to D-Bus enabled applications.
Upon startup avahi-daemon interprets its configuration file /etc/avahi/avahi-daemon.conf and reads XML fragments  from /etc/avahi/services/*.service  which may define static DNS-SD services. If you enable publish-resolv-conf-dns-servers in avahi-daemon.conf the file /etc/resolv.conf will be read, too.

`smbclient //truenas.local/folderShared/ -U vdung`

Mount:
- package: mount.cifs
	- https://linuxvox.com/blog/mount-smb-share-on-linux/
	- `sudo mount.cifs //smb-server/address /mount-folder/ -o username=your-user,password=your-pass`

- package: gvfsd-smb
	- `gio mount smb://truenas.local/folderShared`
	- `mount at /run/user/1000/gvfs/smb-share:server=...`




# Optimization



---
# References
Official website:
Wikipedia:
Youtube: