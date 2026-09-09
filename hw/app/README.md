# Introduction

**Vacui HW Application** is a sub-component of **Vacui HW**. It is a virtual hardware emulator
program running provided guest code (it can be anything, not only **VacuiOS**). The emulator
relies on [Unicorn Engine](https://www.unicorn-engine.org) to execute the guest code.
The virtual hardware has a code name - **Vacui VirtualHW**.

_WANRING_: Since it is virtual, some physical hardware details may be missing
in the documentation.

# Goals

- Provide a guest program with base services to manage and control
  the hardware and processor in a centralized way.

- Make **Vacui VirtualHW** flexible and convenient enough so it can be used not
  only by the sub-components of **VacuiOS**.

# Documents

## General

- [Hardware Memory Layout](./memory.md)
- [Hardware Configuration](./config.md)
- [Hardware Architecture](./arch.md)
