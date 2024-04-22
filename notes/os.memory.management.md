---
id: ijfryhtekkngvig2hbmk5hy
title: Memory Management
desc: ''
updated: 1713819658986
created: 1713816786099
---


## Components used by OS for managing memory

### Physical Memory ([[os.memory.ram]])

Physical memory is the actual hardware component installed in the system. 

### Virtual Memory

Memory management technique that allows the system to run larger applications or execute more programs than the available physical RAM would allow.

It is a conceptual layer on top of physical memory.

It is typically larger than the available physical [[os.memory.ram]]. The illusion of a larger address space is what makes it “virtual.” How is this possible? Read on to find. 

#### Virtual Address Space

Addresses of virtual memory locations -> also bigger than the physical address space.

### Page table

Page tables store mappings between virtual addresses and physical addresses. These are also stored in [[os.memory.ram]], more specifically in [[os.memory.ram.kernel]].

### Pagefile (Swap space)

Space or file on disk (not RAM).

## Processes involved in managing memory

### Swapping

Swapping involves moving parts of a process’s memory between RAM (physical memory) and disk (usually a swap file or partition) at [[execution.lifecycle.runtime]].


## Managing memory - Lifecycle of an address space

- The OS assigns virtual memory for the [[os.memory.ram.user.stack]] when a [[execution.process.thread]] is created.
- Physical memory is assigned to that virtual memory on demand using the [[#page-table]].
- The OS identifies “swappable” pages (memory chunks) based on their usage patterns. Basically, any memory chunk not being used that frequently or actively.
- These pages are swapped in and out as needed.

Swapping allows the OS to free up RAM for other processes but doing it frequently can degrade system performance - so there is a sweet spot to reach for the OS.
