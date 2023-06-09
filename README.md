## Overview of our OS and the x86 architecture

### What is the x86 architecture, exactly?
> An instruction set architecture family based on the Intel 8086 CPU is referred to as "x86."

Since its debut in 1981 for the IBM PC, the x86 architecture has been the most widely used instruction set architecture. Numerous pieces of software, including operating systems (OS), run on x86-based hardware, including DOS, Windows, Linux, BSD, Solaris, and Mac OS X.


I will create an operating system for the x86-32 architecture rather than the x86-64. My operating system should work with modern hardware because of backward compatibility (but use caution if you want to test it on a real machine).

### My Operating System:
My objective is to create a relatively straightforward UNIX-based operating system in C++, not simply a "proof-of-concept". The OS must have the ability to boot, launch a userland shell, and support extensions.

The operating system will run on 32 bits, be designed for the x86 architecture, and be compatible with some, if not most hardware.


**Specifications:**

* Code in C++
* x86, 32 bit architecture
* Boot with Grub
* Kind of modular system for drivers
* Kind of UNIX style
* Multitasking
* ELF executable in userland
* Modules (accessible in userland using /dev/...) :
|  * IDE disks
|  * DOS partitions
|  * Clock
|  * EXT2 (read only)
|  * Boch VBE
* Userland :
|  * API Posix
|  * LibC
|  * Can run a shell or some executables (e.g., lua)
