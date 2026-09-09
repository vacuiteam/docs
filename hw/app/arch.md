# Hardware Architecture

## Overview

The architecture of **Vacui VirtualHW** relies on **control and storage units**.

Control units manage the processor's state and hardware itself. They can disable and reboot
system, prevent a guest program from accessing specific memory, change the current ring mode etc.
Despite having these permissions, they are formally restricted from doing these operations
to ensure the stability of the hardware.

Storage units consists of data managed by a control unit (SCU), but actually owned
by a guest program. They contain persistent and critical data (e.g. a filesystem).

## Control Units

- **Ring Control Unit (RCU)** manages the processor's ring mode.
- **Memory Control Unit (MCU)** restricts programs, running in the user ring, from accessing
  kernel memory.
- **System Call Control Unit (SCCU)** captures an occurred system call and calls a system call
  handler of a guest program.
- **Interrupt Manager Control Unit (IMCU)** generates an interrupt (e.g. a timer interrupt) on request
  and calls its corresponding handler.
- **Storage Control Unit (SCU)** provides a guest program with centralized functionality to manage memory
  in storage units.

## Storage Units

- **Drive Storage Unit (DSU)** consist of raw bytes. Generally, It is used by a guest program
  to manage a filesystem.
