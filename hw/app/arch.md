# Hardware Architecture

## Overview

The architecture of **Vacui VirtualHW** relies on **control and storage units**.

Control units manage the processor's state and hardware itself. They can disable and reboot
system, prevent a guest program from accessing specific memory, change the current ring mode etc.
Despite having these permissions, they are formally restricted from doing these operations
to ensure the stability of the hardware.

Storage units consists of data managed by control units, but owned by a guest program.
They are needed to contain persistent and critical data.

## Control Units

- **Ring Control Unit (RCU)** manages the processor's ring mode.
- **Memory Control Unit (MCU)** restricts programs, running in the user ring, from accessing
  kernel memory.
- **System Call Control Unit (SCCU)** captures an occurred system call and calls a system call
  handler of a guest program.

## Storage Units

- **Drive Storage Unit (DSU)** contains a raw stream of bytes. It is used by a guest program
  to manage a filesystem.
