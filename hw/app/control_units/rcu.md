# RCU

## Overview

RCU (stands for **R**ing **C**ontrol **U**nit) is a part of **Vacui VirtualHW**.
It has the following responsibilities:

- managing the processor's ring mode
- providing the control units with functionality to manage the ring mode.

It has no dependencies, since other control units rely on it.

## Services

RCU exposes the following services:

- switching the processor's ring mode
- inspecting the current processor's ring mode

These services are not provided explicitly to a guest program except control units.
