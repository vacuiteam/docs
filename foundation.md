# Introduction

This document overviews the Vacui project, its development team's structure and
work principles. It is intended for:

- future development team members or newbies
- project contributors

# Definition

The Vacui project is a collection of modular development tools, components and
libraries. It has a codename VQ, which stands for "**V**acui **Q**uarter".
It is developed in multiple languages - Golang, C++ and C.

**Golang** is used in VacuiHW, OS development tools and the build orchestrator.
_Purpose_: Efficient code that is fast to write.

**C++** is used in the OS kernel, system modules and private SDKs.
_Purpose_: Memory stability.

**C** is used in the public SDK of VacuiOS. _Purpose_: High accessibility
in other programming languages, and ABI stability.

The project consists of the following major components:

- **VacuiHW** - A virtual hardware emulator.
- **VacuiOS** - A hybrid operating system that is intended to run on VacuiHW.

Future corresponding documents provide a comprehensive treatment of the
components above.

# Project Goals

- Establish a well-defined, stable and documented platform to create
  software for.

- Integrate social interaction and communication into the project
  as one of the foundational parts.

# Development Team

## Structure

**Founder** is a project's head maintainer who is **dywoq**. They review,
accept or cancel incoming changes in critical components' repositories,
shape and lead the project's development direction.

**Sub-teams** are responsible for maintaining their specific component. They are
needed to manage a complex source tree of Vacui.

## Work Principles

Work principles establish long-term planning and prevent early design
and architecture mistakes. Development team members shall consider them.
The work principles, which are shown below, are not mutually exclusive.

**Document It** - Document your component, its architecture and behavior
instead of dreaming it. It must be done before writing code. It reduces cost
of making changes in future. Ensure somebody else can implement a component ONLY
following a component's specification. If they do not, fix a specification.

**Make It Once** - If you program the same piece of code (such as string manipulation,
utility functions) over and over again in various components, you should make it
an external library. It prevents you from writing boilerplate functionality.

**Separate Its Concerns** - You do not mix component or library code with something
that obviously does not belong to it. It makes code more clear, focused and readable.

**Communication Is A Key** - Create a discussion inside our organization's repository
`vacuiteam/discussions`. If you do not understand something, ask a question. If a specific
feature affects somebody's components, interact with its sub-team. Communication is
not an enemy but a key to solving specific tasks and issues.

# Contacts

To join the development team, contact the founder writing to their email:
**dywoq <dywoq.contact@gmail.com>**. You will be asked questions that
test your knowledge of the operating system development's foundation,
overall programming concepts, and base software tools (e.g. Git).
The test is a live video meeting with cameras on (or, if you are unconformable,
you can disable your video camera). It is a talk between two engineers.
