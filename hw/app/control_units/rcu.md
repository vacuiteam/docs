# RCU

## Overview

The RCU (stands for **R**ing **C**ontrol **U**nit) is a part of 
**Vacui VirtualHW**. It has the following responsibilities:

- managing the processor's ring mode
- providing the control units with functionality to manage the ring mode.

It has no dependencies, since other control units rely on it.

## Services

The RCU does not check who requests its services, because it does
not expose them to a guest program except the control units, 
therefore, additional checks are meaningless.

- The RCU has the following services: **switching the processor's ring mode**
  and **inspecting the current processor's ring mode**.
