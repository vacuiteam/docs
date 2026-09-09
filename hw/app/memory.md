# Hardware Memory Layout

| **Purpose**         | **Physical Range**            | **Size**      | **Description**                                   |
| ------------------- | ----------------------------- | ------------- | ------------------------------------------------- |
| Conventional Memory | `0x00000000` ... `0x06FFFFFF` | `112 MiB - 1` | Reserved for the guest program                    |
| Hardware MMIO Ports | `0x07000000` ... `0x07FFFFFF` | `16MiB - 1`   | Reserved for the hardware control units' services |

The memory regions set their permission flags, which the hardware (**Vacui VirtualHW**)
and a guest program must respect. The flags are **R** (Read), **W** (Write) and **E** (Execute).

| **Subject**         | **Hardware permissions** | **Guest program permissions** |
| ------------------- | ------------------------ | ----------------------------- |
| Conventional Memory | R, E                     | R, W, E                       |
| Hardware MMIO Ports | R, W                     | R, W                          |
