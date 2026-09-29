# MCU

## Overview

**MCU (Memory Control Unit)** is a part of `Vacui VirtualHW`. It controls and manages
guest code's memory access.

**MMIO Ports Block range**: `0x7004000` ... `0x7007FFF`.

## Goals

- Providing a guest program with functionality to set the memory protection mechanisms
  up in the kernel mode.

## Memory Protection

As mentioned in the **"Goals"** chapter, MCU provides general memory protection mechanisms
(such as paging, virtual memory). Unlike in the classic IA32 architecture, the procedure
of setting the mechanisms up is different, since the control registers are not involved.

## Paging

Paging is a general memory protection mechanism that splits memory into pages and stores
their meta information in the page directories and tables.

- **Pages** are identical, fixed-size blocks of data.

- **Page Directories** are linear arrays of physical address that point to the page tables.

- **Page Tables** are linear arrays of physical address that consists of meta information
  belonging to pages.
