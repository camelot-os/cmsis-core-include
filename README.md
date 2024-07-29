<!--
SPDX-FileCopyrightText: 2024 Ledger SAS

SPDX-License-Identifier: Apache-2.0
-->

# CMSIS headers extract for outpost-os embedded repositories

## Introduction

This repository hold snapshoted versions of ARM CMSIS official headers so that they can be used into
any ARM-based repositories.

By now, we use this repository in order the CMSIS mono-repo complexity while only using cmxx-related headers.

This repository aim to disappear as soon as ARM as delivered a clean multi-repo based CMSIS header sets.

## Usage

This repository can be used easily with Meson build system, so that the CMSIS include directory is
automatically added, allowing the usage of `#include <cmsis/header.h>` directly in the caller's repository
sources.

## Versioning

This repository is versionned using the CMSIS upstream version used, allonside local potential evolutions of
the meson glue, with the following syntax: *vx.y.z-t* where:

   * vx.y.z matches the CMSIS headerset version used
   * -t matches local updates on local files
