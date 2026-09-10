# RCU

## Overview

**Description**: The RCU (stands for **R**ing **C**ontrol **U**nit) is a part
of **Vacui VirtualHW**. It is responsible for managing the processor's ring mode.

**MMIO Ports Block range**: `0x07000000` ... `0x7003FFF`.

## Goals

- Providing functionality to inspect the current processor's ring mode.

- Providing functionality to enter readonly modification state to prevent
  accidental processor mode switches during critical operations.

## Ring Modes

At the moment, the RCU supports a pair of ring modes excluding **Ring 1** and **Ring 2**:
**Ring 0** (kernel and drivers) and **Ring 3** (user). This choice corresponds
to the IA32 processor architecture.

## Functionality

As mentioned in the **"Goals"** chapter, the RCU has the following functionality:

- Inspection of the RCU's information consisting of the current processor's ring mode
  and modification state.

- Switching the modification state and processor's ring mode.
