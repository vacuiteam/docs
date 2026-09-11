# Victus

## Overview

Victus is a development tool that orchestrates building process in C/C++ components.

## Goals

- Provide a centralized way to build C/C++ components in **VacuiOS** to avoid
  fragmentation.

- Allow replacing compilers and linker through using toolchains, along with
  forcing specific toolchain.

## Modules

Modules are configuration files that use the **TOML** format (_v1.1.0_).
There are two types: **workspace** and **regular**.

### Configuration

A module consists of the general and type-specific information.

The general information consists of the following:

- `general.type` (`string`) - The module type. Allowed values: `"workspace"`, and `"regular"`.

Depending on the value of `general.type`, the corresponding variants of the type-specific
information are activated, which are shown in subsequent chapters.

#### Workspace

- `info.workspace.modules` (`string[]`) - The folder paths of modules in the current working directory.

#### Regular

- `info.regular.destination_path` (`string`) - The path to a destination file.
- `info.regular.objects_dir_path` (`string`) - The path to an objects directory path.
- `info.regular.dependencies` (`string[]`) - The dependencies list built first before the parent regular module.

## Toolchains

Toolchains are configuration files like modules that specify C and C++ compilers, a linker
and its additional flags used during compilation.

The toolchain consists of the following:

- `c_compiler` (`string`)
- `cxx_compiler` (`string`)
- `linker` (`string`)
- `additional_c_flags` (`string[]`)
- `additional_cxx_flags` (`string[]`)
- `additional_linker_flags` (`string[]`)
