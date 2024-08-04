Tags: #SecondBrain 
Status: #open, #unprocessed
Related: 

---

https://pages.cs.wisc.edu/~remzi/Classes/537/Fall2021/


  

|  |  |  |  |  |  |
| ---- | ---- | ---- | ---- | ---- | ---- |
| **Intro** | **Virtualization** |  | **Concurrency** | **Persistence** | **Security** |
| [Preface](https://pages.cs.wisc.edu/~remzi/OSTEP/preface.pdf) | 3 _[Dialogue](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-virtualization.pdf)_ | 12 _[Dialogue](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-vm.pdf)_ | 25 _[Dialogue](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-concurrency.pdf)_ | 35 _[Dialogue](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-persistence.pdf)_ | 52 [_Dialogue_](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-security.pdf) |
| [TOC](https://pages.cs.wisc.edu/~remzi/OSTEP/toc.pdf) | 4 [Processes](https://pages.cs.wisc.edu/~remzi/OSTEP/cpu-intro.pdf) | 13 [Address Spaces](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-intro.pdf) [code](https://github.com/remzi-arpacidusseau/ostep-code/tree/master/vm-intro) | 26 [Concurrency and Threads](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-intro.pdf) [code](https://github.com/remzi-arpacidusseau/ostep-code/tree/master/threads-intro) | 36 [I/O Devices](https://pages.cs.wisc.edu/~remzi/OSTEP/file-devices.pdf) | 53 [_Intro Security_](https://pages.cs.wisc.edu/~remzi/OSTEP/security-intro.pdf) |
| 1 _[Dialogue](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-threeeasy.pdf)_ | 5 [Process API](https://pages.cs.wisc.edu/~remzi/OSTEP/cpu-api.pdf) [code](https://github.com/remzi-arpacidusseau/ostep-code/tree/master/cpu-api) | 14 [Memory API](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-api.pdf) | 27 [Thread API](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-api.pdf) [code](https://github.com/remzi-arpacidusseau/ostep-code/tree/master/threads-api) | 37 [Hard Disk Drives](https://pages.cs.wisc.edu/~remzi/OSTEP/file-disks.pdf) | 54 [_Authentication_](https://pages.cs.wisc.edu/~remzi/OSTEP/security-authentication.pdf) |
| 2 [Introduction](https://pages.cs.wisc.edu/~remzi/OSTEP/intro.pdf) [code](https://github.com/remzi-arpacidusseau/ostep-code/tree/master/intro) | 6 [Direct Execution](https://pages.cs.wisc.edu/~remzi/OSTEP/cpu-mechanisms.pdf) | 15 [Address Translation](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-mechanism.pdf) | 28 [Locks](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-locks.pdf) [code](https://github.com/remzi-arpacidusseau/ostep-code/tree/master/threads-locks) | 38 [Redundant Disk Arrays (RAID)](https://pages.cs.wisc.edu/~remzi/OSTEP/file-raid.pdf) | 55 [_Access Control_](https://pages.cs.wisc.edu/~remzi/OSTEP/security-access.pdf) |
|  | 7 [CPU Scheduling](https://pages.cs.wisc.edu/~remzi/OSTEP/cpu-sched.pdf) | 16 [Segmentation](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-segmentation.pdf) | 29 [Locked Data Structures](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-locks-usage.pdf) | 39 [Files and Directories](https://pages.cs.wisc.edu/~remzi/OSTEP/file-intro.pdf) | 56 [_Cryptography_](https://pages.cs.wisc.edu/~remzi/OSTEP/security-crypto.pdf) |
|  | 8 [Multi-level Feedback](https://pages.cs.wisc.edu/~remzi/OSTEP/cpu-sched-mlfq.pdf) | 17 [Free Space Management](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-freespace.pdf) | 30 [Condition Variables](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-cv.pdf) [code](https://github.com/remzi-arpacidusseau/ostep-code/tree/master/threads-cv) | 40 [File System Implementation](https://pages.cs.wisc.edu/~remzi/OSTEP/file-implementation.pdf) | 57 [_Distributed_](https://pages.cs.wisc.edu/~remzi/OSTEP/security-distributed.pdf) |
|  | 9 [Lottery Scheduling](https://pages.cs.wisc.edu/~remzi/OSTEP/cpu-sched-lottery.pdf) [code](https://github.com/remzi-arpacidusseau/ostep-code/tree/master/cpu-sched-lottery) | 18 [Introduction to Paging](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-paging.pdf) | 31 [Semaphores](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-sema.pdf) [code](https://github.com/remzi-arpacidusseau/ostep-code/tree/master/threads-sema) | 41 [Fast File System (FFS)](https://pages.cs.wisc.edu/~remzi/OSTEP/file-ffs.pdf) |  |
|  | 10 [Multi-CPU Scheduling](https://pages.cs.wisc.edu/~remzi/OSTEP/cpu-sched-multi.pdf) | 19 [Translation Lookaside Buffers](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-tlbs.pdf) | 32 [Concurrency Bugs](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-bugs.pdf) | 42 [FSCK and Journaling](https://pages.cs.wisc.edu/~remzi/OSTEP/file-journaling.pdf) | **Appendices** |
|  | 11 _[Summary](https://pages.cs.wisc.edu/~remzi/OSTEP/cpu-dialogue.pdf)_ | 20 [Advanced Page Tables](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-smalltables.pdf) | 33 [Event-based Concurrency](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-events.pdf) | 43 [Log-structured File System (LFS)](https://pages.cs.wisc.edu/~remzi/OSTEP/file-lfs.pdf) | [_Dialogue_](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-vmm.pdf) |
|  |  | 21 [Swapping: Mechanisms](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-beyondphys.pdf) | 34 _[Summary](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-dialogue.pdf)_ | 44 [Flash-based SSDs](https://pages.cs.wisc.edu/~remzi/OSTEP/file-ssd.pdf) | [Virtual Machines](https://pages.cs.wisc.edu/~remzi/OSTEP/vmm-intro.pdf) |
|  |  | 22 [Swapping: Policies](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-beyondphys-policy.pdf) |  | 45 [Data Integrity and Protection](https://pages.cs.wisc.edu/~remzi/OSTEP/file-integrity.pdf) | [_Dialogue_](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-monitors.pdf) |
|  |  | 23 [Complete VM Systems](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-complete.pdf) |  | 46 _[Summary](https://pages.cs.wisc.edu/~remzi/OSTEP/file-dialogue.pdf)_ | [Monitors](https://pages.cs.wisc.edu/~remzi/OSTEP/threads-monitors.pdf) |
|  |  | 24 _[Summary](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-dialogue.pdf)_ |  | 47 _[Dialogue](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-distribution.pdf)_ | [_Dialogue_](https://pages.cs.wisc.edu/~remzi/OSTEP/dialogue-labs.pdf) |
|  |  |  |  | 48 [Distributed Systems](https://pages.cs.wisc.edu/~remzi/OSTEP/dist-intro.pdf) | [Lab Tutorial](https://pages.cs.wisc.edu/~remzi/OSTEP/lab-tutorial.pdf) |
|  |  |  |  | 49 [Network File System (NFS)](https://pages.cs.wisc.edu/~remzi/OSTEP/dist-nfs.pdf) | [Systems Labs](https://pages.cs.wisc.edu/~remzi/OSTEP/lab-projects-systems.pdf) |
|  |  |  |  | 50 [Andrew File System (AFS)](https://pages.cs.wisc.edu/~remzi/OSTEP/dist-afs.pdf) | [xv6 Labs](https://pages.cs.wisc.edu/~remzi/OSTEP/lab-projects-xv6.pdf) |
|  |  |  |  | 51 _[Summary](https://pages.cs.wisc.edu/~remzi/OSTEP/dist-dialogue.pdf)_ |  |

why OS
- security
- reliability - 
- file
- program management
- how computer work



Virtualization:
- Goals:
	- Efficiency
	- Security (isolate)

virtualization CPU:
- General ideal: time sharing
- Mechanisms: low-level how
- Policies: rule to decide which process to run


**Reboot is powerful**
if an program/system run continueoustly 3 year, a lot of thing happen and can be hard to debug, test.
Reboot is bring the program/system to start point where it was testing many time in its lifetime.



---
# References
Official website:
Wikipedia:
Youtube: