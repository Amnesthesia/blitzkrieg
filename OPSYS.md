# OPERATIVSYSTEMER:

## Trivia

* What's the first operating system considered a predecessor to UNIX and when was unix launched? Who wrote UNIX?

## Questions

### CPU & I/O
* Pros and cons of precise/imprecise interrupts?
* Explain the relation between system calls, commands and instructions
* Explain what happens in a hardware-driven interrupt?
* Why does a system call take much longer in a virtual machine than in a non-virtual environment?
* Explain the software layers in a typical I/O system and comment on what purpose each layer has
* Explain how the system architectures protection rings are used in hardware virtualization
* Assume a scheduling algorithm that favorizes processes that used a low amount of CPU time recently favorize I/O bound processes? Why will this algorithm in the long term prohibit CPU-bound processes from getting CPU-time?
* What two main groups of I/O devices exist in Unix/Linux systems? 
* Why is it useful to group I/O devices?

### Threads and processes
* What is a process?
* What's stored in a program's stack when it's running?
* What is a service/daemon?
* What is a mode switch/mode transition?
* What's the PSW/FLAG-register and what is it used for?
* What happens when you fork() ?

### File systems and memory
* How does the operating system find root dir in NTFS?
* What is the purpose of RAID disks? How are RAID disks organized? Explain RAID 1/5/10
* What is fragmentation and what types of fragmentations are we working with?
* How large files can we have in a filesystem based on inodes and triple-indirect addressing? (assuming 32-bits diskblock addresses and disk block size 4kb)
* Difference between the above and FAT32?
* What's the point of extending TLB to include ASID (Address Space Identified; introduced with Intel's EPT and AMDs RVI/NPT)
* Explain write aplication and wear levelling on SSD disks?
* What is MFT in the context of NTFS?
* What does internal and external fragmentation mean in relation to a file?
* Explain the difference between a hard and a soft link in a file system. What is the link counter in an inode used for?
* Assuming you have the metadata for a file. How do you get to the data blocks that file is dependent on in NTFS? EXT? FAT? 
* What does it mean that a system is adapted for SSD?
* Explain shortly how shadow page tables work

### Commands, Scripting & Programming logic

* Explain race conditions (spooling example etc)
* Explain critical sector
* Write bashscript (do X with command line arguments, filter list distinct)
* PowerShell list/grep/print
* Semaphore - explain when to wait & post (up/down)? (or mark spots in example code)
* Explain commands:
	- ps (ps -e, ps aux, ps axco)
	- ls (ls -ltr, ls -la, ls -l)
	- wc (wc -l)
	- grep (egrep, grep -e)
	- find
	- awk
	- exec
* Explain Assembly:
	- movl
	- leal
	- eax
	- edx
	- rbp
	- rax
	

### Security

* Explain what Covert Channel means.
* Explain how Windows Integrity Levels (Mandatory Integrity Control) works?
* What is a polymorphic virus? Explain how such a virus is programmed
* Explain the security model Bell-La Padula and Biba
* Explain how User Account Control (UAC) in Windows works
* List and comment on 4 different types of viruses
* What job does a Reference Monitor have in an operating system?

## Algorithms and Calculation
* Calculate average turnaround time for each scheduling algorithm (SRTN, Non-preemtive, priority scheduling, Round Robin with a time quantum of 30ms)
* Calculate Z pages, X bits in bitmap & Y page frames for M memory size
* How many sets exist in a 4-way set-associative cache of 128Kb size with 64 bytes cache lines?
* Affinity scheduling reduces amount of cache misses; does it reduce amount or TLB misses? Explain
* Draw and explain a 500Mhz crystal oscillator and explain how it causes clock interrupts of 2ns - 8.6 sec?
* Use Banker's algorithm to determine whether the state in a given table is safe (Deadlock)
* Explain what safety mechanism an OS typically uses to prevent a classical buffer overflow and return-to-libc attack
* Page Replacement:
	- Optimal
	- NRU
	- FIFO
	-	Second Chance
	- LRU

## Summary

### Topics

* CPU & I/O
	- Software layers
	- System calls (normal + virtualization; difference)
	- Scheduling algorithms
	- Hardware / Clock interrupts
	- Imprecise / precise interrupts
	- Oscillator
* Threads & Processes
	- Race conditions & Deadlock
		- Semaphores & Mutex
		- Banker's algorithm
		- Critical sector
* Filesystem & Memory
  - Hard/soft links
  - NTFS, FAT, EXT
		- MFT
	- RAID
	- Internal/External Fragmentation
	- Cache
  - TLB
	- Page tables
		- Shadow page tables
		- Calculate amount of pages
		- Calculate bitmap size
		- Page frames
		- Page replacement
			- Optimal
			- NRU
			- FIFO
			-	Second Chance
			- LRU
* Scripting & Programming logic
	- GNU/Linux commands:
		- ls
		- wc
		- grep/egrep
		- find
		- awk
		- exec
		- ps
	- PowerShell equivalents of above
	- Assembly
			- movl
			- leal
			- eax
			- edx
			- rbp
			- rax
* Security mechanisms:
	- Reference monitor
  - Bell-La Padula
  - Biba
  - UAC, User Account Control
	- Covert Channel
	- Protection rings

