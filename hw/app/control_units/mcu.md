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
