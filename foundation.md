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

## Work Principles

Work principles establish long-term planning and prevent early designing and architectural
mistakes. Development team members shall consider them. The work principles, which are
shown below, are not mutually exclusive.

1. **Document It** - Document your component, its architecture and procedures
   instead of dreaming about it. It reduces cost of making changes in future.

2. **Make It Once** - If you program the same piece of code (such as string manipulation,
   utility functions) over and over again in various components, you should make it
   an external library. It prevents you from writing boilerplate.

3. **Separate Its Concerns** - You do not mix component or library code with something
   that obviously does not belong to it. It makes code more clear, focused and readable.

4. **Communication Is A Key** - Create a discussion inside our organization's repository
   `vacuiteam/discussions`. If you do not understand something, ask a question. If a specific
   feature affects somebody's components, interact with sub-teams. Communication is
   not an enemy but a key to solving specific task and issue.
