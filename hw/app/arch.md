# Hardware Architecture

## Overview

The architecture of **Vacui VirtualHW** relies on **control and storage units**.

Control units manage the processor's state and hardware itself. They can disable and reboot
system, prevent a guest program from accessing specific memory, change the current ring mode etc.
Despite having these permissions, they are restricted from doing these operations in most cases 
to ensure the hardware stability.

Storage units consists of data managed by a control unit (SCU), but actually owned
by a guest program. They contain persistent and critical data (e.g. a filesystem)
as raw bytes.

## Control Units

- **Ring Control Unit (RCU)** manages the processor's ring mode.
- **Memory Control Unit (MCU)** restricts programs, running in the user ring, from accessing
  kernel memory.
- **System Call Control Unit (SCCU)** captures an occurred system call and calls a system call
  handler of a guest program.
- **Interrupt Manager Control Unit (IMCU)** generates an interrupt (e.g. a timer interrupt) on request
  and calls its corresponding handler, set by a guest program.
- **Storage Control Unit (SCU)** provides a guest program with centralized functionality to manage data
  in storage units.

All control units are given a 16KiB block in the **MMIO Ports** region, which is shown in
[hardware memory layout document](./memory.md). A guest program writes specific values to the ports
within the block (e.g. to prepare a control unit before doing specific operations). The block
has a unique starting physical address, followed by the base address of the **MMIO Ports** region.

## Storage Units

- **Drive Storage Unit (DSU)** is used by a guest program to manage a filesystem.
