Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[Operation System]], [[MMU]]

---
### Physical and logical addresses


### process model
An MMU is commonly deployed to support “process model”. This is a way to organize tasks in an operating system and is the one used by most “heavyweight” operating systems, In the world of embedded systems, this means Linux. Most desktop operating systems also employ process model. 

The idea is simple: each task (OS term is processes or running programs) uses memory from address zero upwards, as if it were running by itself on the CPU. The MMU maps the addresses onto a specific area of real, physical memory. Each time there is a context switch – i.e. a different process takes control – the MMU mapping is changed.

This simplifies the development of each process and provides a high level of safety and security as each process cannot access the memory that “belongs” to other processes. The downside of this approach is that each context switch includes an additional overhead: MMU remapping. If you want to use Linux, you need to have an MMU.

### thread model
Most RTOS products on the market are thread model. This means that all the tasks’ (now called threads) code and data occupy the same address space, along with that of the RTOS itself, as illustrated in **Figure 1** .

![](https://www.embedded.com/wp-content/uploads/media-1204226-mentor-mmu-fig-1-300.jpg)

_**Figure 1: Multitasking using a thread model**_

Theoretically, but hopefully not in practice, **one thread can access and/or corrupt the code and data of another thread or of the RTOS**. Obviously, this possibility is only of passing interest if the code is properly debugged and from a trustworthy source. The big **benefit** of thread model is that the **context switch is fast**, as only the CPU registers need to be saved and restored.

Source: https://www.embedded.com/using-a-memory-management-unit/

### Thread protected model
Some RTOS products (including [Nucleus RTOS](https://www.mentor.com/embedded-software/nucleus/)) have an option to use the MMU in a simple, but useful, way. This mode of operation may be called “lightweight process model” or “thread-protected mode”. This approach does not remap any memory, but it protects memory that does not belong to the current task [by making it invisible]. 
If a task attempts to access memory outside of its designated area, a trap occurs and this is usually an indication of a fault in the code. This slightly increases the context switch time, as the MMU needs to be set up, but this is a lower overhead than a full remapping required for process model

_**![](https://www.embedded.com/wp-content/uploads/media-1204228-mentor-mmu-fig-3-300.jpg)
Figure 3: Memory management using a thread protected mode with Task 2 in control

**_

---
# References
Official website:
Wikipedia:
Youtube:

Source: https://www.embedded.com/using-a-memory-management-unit/
Source: https://blogs.sw.siemens.com/embedded-software/2019/09/16/do-you-need-a-memory-management-unit/