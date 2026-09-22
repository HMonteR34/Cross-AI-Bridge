---
name: firmware-development
description: Use this skill for firmware development, board bring-up, driver implementation, RTOS integration, debugging, porting across hardware platforms, and especially security hardening. Trigger on embedded C/C++, bare-metal, Zephyr, FreeRTOS, ARM/RISC-V, secure boot, drivers, bootloader, OTA, or security best practices.
---

# Firmware Development & Porting with Security

## Overview
This skill delivers workflows, checklists, templates, and best practices for reliable embedded firmware development and porting. Emphasis on security by design, portability, and production readiness for MCUs, SoCs, and IoT/edge devices.

## Core Principles
- Hardware abstraction for portability.
- Security by design (secure boot, crypto, isolation).
- Follow MISRA/CERT, use version control, rigorous testing.
- Validate on real hardware.

## Development Workflow
1. Setup toolchain, CMake, linker scripts, memory map.
2. Implement drivers with error handling and power mgmt.
3. Integrate RTOS and handle concurrency/interrupts.
4. Add debugging (JTAG, SWO) and fault handlers.
5. Develop secure bootloader with DFU/OTA.
6. Unit/integration/HIL testing.

## Porting Guide
1. Assess hardware differences (peripherals, memory, security features).
2. Refactor to HAL/BSP.
3. Update startup, clocks, drivers, interrupts.
4. Adapt build system.
5. Full validation and performance testing.

## Security Hardening (Key Focus)
See references/security-checklist.md for details.
- Enable secure boot and root of trust.
- Use HSM/TEE for keys/crypto.
- Protect against buffer overflows, injection, side-channels.
- Secure updates with signing/encryption.
- Least privilege, compartmentalization, zero-trust.

## Tools
- GCC/toolchains for ARM/RISC-V.
- OpenOCD/GDB/J-Link.
- pyOCD/dfu-util for flashing.
- Static analyzers, fuzzers.

Add templates to assets/. Use references/ for MCU-specific guides. Integrate with docx/pdf skills for reports.

## Live-project note (2026-09-22)
This package is still generic MCU/RTOS. The user's active target is locked Google TV on Amlogic (Onn 4K Pro). Grok evaluation: treat OTA capture, UART, AVB, and productmode as the real workflow until a specialized skill exists. See `shared-memory/grok-evaluation-2026-09-22.md`.
