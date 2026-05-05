# Project Context

## What this project is

**Esp32-Marauder-CheeseCake** is a beginner PCB development project for building a small ESP32 handheld board. The concept is inspired by the physical idea of ESP32 Marauder-style boards and dolphin/Flipper-Zero-like handheld multi-tools, but the project focus is **defensive diagnostics and PCB learning**.

## Why this exists

The creator is new to KiCad and PCB design. This repo is meant to document the process clearly:

- planning the board,
- choosing components,
- making a schematic,
- assigning footprints,
- laying out a handheld PCB,
- routing traces,
- exporting manufacturing files,
- testing the assembled board.

## Target V1 outcome

A working first PCB that can:

- power an ESP32 safely,
- be programmed through USB-UART,
- display a menu on an OLED,
- read button presses,
- run from a LiPo battery,
- expose headers for optional modules.

V1 success does not require every advanced module to be soldered directly onto the board.

## Design philosophy

Keep V1 simple:

- Use modules and headers for advanced RF/NFC parts.
- Avoid bare RF chip routing until later revisions.
- Use 0603 passives instead of tiny 0402 parts.
- Use a 2-layer PCB first.
- Prioritize debugging and learning over miniaturization.

