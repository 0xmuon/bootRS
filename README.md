# bootRS

#### A bootloader built in rust as a side project.
The bootRS project is organized as a Rust workspace containing multiple specialized crates that work together to provide bootloader functionality for both BIOS and UEFI systems.
```
I havn't pushed the test repo as some codes have open endpoints.(will update soon!)
```

#### Memory Configuration Architecture
The bootloader's memory management operates through a configuration-driven approach where kernels specify their memory requirements at compile time through the BootloaderConfig struct.

#### Physical Memory Discovery
The bootloader discovers available physical memory through platform-specific mechanisms and translates this information into a unified MemoryRegions structure.

#### Virtual Memory Setup
The bootloader establishes virtual memory mappings based on the kernel's configuration, setting up page tables and creating the virtual address space layout.

#### Boot Information Transfer
The bootloader passes comprehensive memory information to the kernel through the BootInfo struct, providing all necessary details for kernel memory management initialization.

Here's an overview:
![image](https://github.com/user-attachments/assets/c81418ef-d687-48c3-8c10-057d034f5c60)


## Reference:

https://os.phil-opp.com/

https://github.com/rust-osdev/uefi-rs
