# RCU

## Overview

_Description_: **Ring Control Unit (RCU)** is a part of **Vacui VirtualHW**
managing the processor's ring mode.

_Dependencies_: None

_Responsibilities_:

- Providing control units with functionality to view and modify the
  processor's ring mode.

## Supported ring modes

RCU implements switching between ring modes, which are supported by the processor
(which is **IA32**). Although support of Ring 1 and Ring 2 are removed:

- **Ring 0** (Kernel and Drivers)
- **Ring 3** (User Software)
