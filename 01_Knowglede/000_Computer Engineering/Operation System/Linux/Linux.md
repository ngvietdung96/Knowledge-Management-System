Tags: #MapOfContents 
Status: #open
Related: [[Operation System]]

---
# References
Official website:
Wikipedia:
Youtube:
# Embedded Linux

![](https://www.youtube.com/watch?v=BdKyq56Cijo&list=TLPQMTcxMTIwMjMhfXAoVbzHAw&index=3)

# Boot
[[U-boot]]

# [[Root File System (RFS)]]
https://wiki.linuxfoundation.org/lsb/fhs-30
https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard#cite_note-2

# Command

Writing an SD Card Image Using Linux Command Line Tools:

Show list of Disks on current machine:
```
sudo fdisk -l
```

If the Linux image file you have downloaded ends with an `.xz` file extension, run:
```
xzcat ~/Downloads/<image-file.xz> | sudo dd of=<drive address> bs=1M
```
Else, run:
```
sudo dd if=~/Downloads/<image-file> of=<drive address> bs=32M
```


[How to add directory to path in Linux](https://linuxize.com/post/how-to-add-directory-to-path-in-linux/)

# Source 

![# How Do Linux Kernel Drivers Work? - Learning Resource](https://www.youtube.com/watch?v=juGNPLdjLH4)

![](https://www.youtube.com/watch?v=pj0a91vlcGo)
