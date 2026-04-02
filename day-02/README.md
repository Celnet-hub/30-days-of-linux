# Day 02 - [Understanding the Linux Architecture - Part 2]

## Objective

Today's objective is simple. Expand on the kernel. Since the kernel is the core component of the Linux operating system. Understand the components/subsystems of the Kernel would give me a better understanding how many the OS handles CPU, memory, etc behind the scenes.

---

## What I Learned

There are 5 subsystems that makes up the Linux Kernel:
- Process Scheduler
- The Memory Management Unit (MMU)
- The VFS (Virtual File System)
- The Networking Subsystem
- The Inter-Process Communication (IPC) Unit

---

## What I Practiced

- To see how the kernel handles processes:
    - `top`: to view processor's activities.
    - `htop`: same as top but more colorful.

- In terms of Memory management:
    - `free -h`: The quickest way to see total, used, and available memory. The -h makes it "human-readable" (GB instead of bytes). this shows how the kernel partitions the RAM.
    - `vmstat 1`: Provides a running report of virtual memory, paging, and CPU activity every 1 second.

- To understand how the Kernel maps different hardware into a single folder struture:
    - `df -h`: Shows your "Disk Free" space, but more importantly, it shows all the different filesystems the VFS is currently managing.

    - `lsblk`: Lists all block devices (hard drives, USBs). It shows the physical layout before the VFS "abstracts" it.

    - `mount`: Shows exactly which physical device is "hooked" into which folder in your system.


---

## Key Takeaways

- The kernel is a resource manager that manages resources required for apps to operate 
- In Linux, everythin is a file