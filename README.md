# Brave Origin Unlocker

A TypeScript-based utility for managing Brave Origin's local application state on Windows and macOS, built with Deno.

## Overview

Brave Origin Unlocker is a utility that interacts with Brave Origin's local `Local State` JSON configuration file.

It is designed to modify browser configuration data related to purchase validation and SKU information.

The project includes platform detection, configuration management, and additional monitoring functionality.

## Features

- **Cross-platform support:** Windows and macOS detection.
- **Local State management:** Reads and modifies browser configuration data.
- **SKU configuration:** Updates locally stored SKU information.
- **Configuration monitoring:** Includes background monitoring functionality.
- **Automatic startup:** Includes optional startup integration.
- **Deno-powered:** Written in TypeScript and executed using Deno.
- **Standalone builds:** Supports compilation for supported platforms.

## Requirements

- [Deno](https://deno.com/)
- Windows or macOS
- Brave Origin installed
- Appropriate filesystem permissions

## Installation

### 1. Install Deno

Download and install Deno from:

https://deno.com/

Verify the installation:

```bash
deno --version
```

### 2. Clone the repository

```bash
git clone https://github.com/debraj-80/brave-origin-unlocker.git

cd brave-origin-unlocker
```

### 3. Inspect the project

Before running the utility, review its source code, Deno permissions, filesystem operations, and startup behavior.

## Available Deno Tasks

The project provides predefined tasks in `deno.json`.

Inspect available tasks with:

```bash
deno task
```

### Compilation

The project includes compilation tasks for the following targets:

| Target | Task |
|---|---|
| Windows x64 | `compile-win` |
| macOS Apple Silicon | `compile-mac-arm` |
| macOS Intel | `compile-mac-x64` |

Compiled outputs are configured to be placed in the `dist/` directory.

## Project Structure

```text
brave-origin-unlocker/
│
├── unlock.ts
├── deno.json
├── README.md
├── .gitignore
└── dist/
    └── Generated binaries
```

The `dist/` directory is generated during compilation and may not be present in a fresh clone.

## Security Considerations

This utility modifies browser configuration files and may interact with Windows startup mechanisms.

Please consider the following before using or reviewing the project:

- Back up browser configuration files before making changes.
- Review filesystem permissions granted to Deno.
- Understand any background monitoring or startup registration.
- Inspect generated executables independently of the source code.
- Do not run unfamiliar binaries with Administrator privileges.
- Keep Windows Defender and other security protections enabled.

**Important:** Changes to local purchase-validation or SKU data do not establish legitimate purchase authorization. This project does not guarantee that server-side license validation will accept modified local state.

## Disclaimer

This project is provided for educational and software research purposes.

Users are responsible for understanding the code, its effects on local browser data, and any applicable software licensing terms.

The author makes no guarantee of compatibility, reliability, or suitability for a particular environment.

---

**Built with TypeScript and Deno.**
