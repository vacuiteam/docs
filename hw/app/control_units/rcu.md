# RCU

## Overview

**Description**: The RCU (stands for **R**ing **C**ontrol **U**nit) is a part
of **Vacui VirtualHW**. It is responsible for managing the processor's ring mode.

**MMIO Ports Block range**: `0x07000000` ... `0x7003FFF`.

## Goals

- Providing functionality to inspect the current processor's ring mode.

- Providing functionality to enable temporary lock flag that is needed to
  prevent the processor's ring mode from being switched during critical
  operations.

## Ring Modes

At the moment, the RCU supports a pair of ring modes excluding **Ring 1**
and **Ring 2** - **Ring 0** and **Ring 3**. This choice corresponds to the
IA32 processor architecture.
