# Victus

## Overview

Victus is a development tool that orchestrates building process in C/C++ components.
It relies on **Make** to handle compilation of C/C++ source files and linking.
Modules that use Victus apply the **TOML configuration** format (_v1.1.0_ version).

## Goals

- Provide a centralized way to build C/C++ components in **VacuiOS** to avoid
  writing boilerplate configurations.

- Allow replacing compilers and linker through using toolchains, along with
  forcing specific toolchain.
