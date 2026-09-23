# RCU

## Overview

**RCU (Ring Control Unit)** is a part of `Vacui VirtualHW`. It manages the processor's ring mode.

**MMIO Ports Block range**: `0x07000000` ... `0x7003FFF`.

## Goals

- Providing a guest program with the functionality to inspect the current processor's ring mode.

- Providing a guest program with the functionality to enter various modification states
  to prevent switching the processor mode during critical operations.

## Ring Modes

RCU supports the following processor's ring modes (support for Ring 1 and Ring 2 is excluded): 
**Ring 0** and **Ring 3**.  
