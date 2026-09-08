# Introduction

This specification is a foundational document of the Vacui project.
It is intended for:

- future development team members or newbies
- project contributors

# Definition

The Vacui is a collection of modular development tools, components and
libraries. It has a codename VQ, which stands for "**V**acui **Q**uarter".
It is developed in multiple languages - Golang, C++ and C. Below, you
can see purpose of the languages:

- **Golang** - It is needed to program virtual hardware emulator, build
  orchestrators and OS development tools. Here, efficient code, which
  is also fast to write, matters.

- **C++** - It is used in the operating system kernel, and internal SDKs,
  where safety and memory stability are high priority.

- **C** - It is used in public OS user-land libraries, where ABI stability
  and accessibility by other languages are critically important.

The project consists of the following components:

- **VacuiHW** - A virtual hardware emulator.

- **VacuiOS** - A hybrid operating system that is intended to run on VacuiHW.

Future corresponding documents provide a comprehensive treatment of the
components above.

# Development Team

## Structure

- **Founder** - The project founder (dywoq). They are project's head maintainer.
  The founder reviews, accepts or cancels incoming changes in critical components'
  repositories.

- **Sub-teams**: To manage a complex source tree, the development team is divided into
  sub-teams. A sub-team is responsible for maintaining a specific component (e.g. a kernel,
  boot loader, libraries, specific tool etc.). If needed, sub-team members can communicate
  with other sub-teams, if a specific feature or bug fix affects other components.
