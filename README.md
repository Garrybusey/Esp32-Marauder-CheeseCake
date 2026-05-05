# Esp32-Marauder-CheeseCake

A beginner-friendly **ESP32 handheld PCB learning project** inspired by the physical style of ESP32 Marauder boards and dolphin/Flipper-Zero-like handheld multi-tools.

The goal of this repo is **PCB development practice**: learning KiCad, schematic design, board layout, footprints, routing, basic power design, and preparing manufacturing files. The intended use case is **authorized defensive cybersecurity utility / wireless diagnostics**, not attacking networks or bypassing access systems.

> Status: planning / starter repository. No finished Gerbers yet.

## Project goals

- Design a handheld ESP32-based PCB from scratch in KiCad.
- Support an ESP32 Wi-Fi/Bluetooth module or dev-board style mounting.
- Add a small OLED screen and physical navigation buttons.
- Add safe utility features such as battery monitoring, GPIO breakout, IR header, microSD option, NFC header, and optional RF module headers.
- Keep V1 realistic for a beginner: simple, buildable, and easy to debug.
- Keep the design focused on legal, authorized, defensive use.

## Current V1 hardware concept

Recommended V1 board scope:

- ESP32-WROOM-style module footprint.
- Optional 2.54 mm header footprint for a DevKit-style ESP32 board.
- 1.3 inch I2C OLED display header/footprint.
- 5 tactile buttons: up, down, left, right, OK.
- USB-C power input.
- USB-UART bridge for programming classic ESP32 modules.
- MCP73831 LiPo charger.
- AP2112K 3.3 V regulator.
- JST-PH 2-pin LiPo battery connector.
- Battery voltage sense divider.
- Optional IR TX/RX section.
- Optional microSD section.
- Optional CC1101 sub-GHz module header.
- Optional PN532 NFC module header.
- GPIO/debug expansion header.

## Important antenna note

If using an ESP32 module with a built-in PCB antenna, do **not** design your own Wi-Fi antenna. Place the module at the edge of the PCB and keep the antenna area clear of copper, traces, battery, display metal, and tall components.

If using an ESP32 module with u.FL/IPEX antenna output, use a short controlled-impedance RF trace and keep the antenna connector close to the module.

## Repository structure

```text
Esp32-Marauder-CheeseCake/
├── README.md
├── SAFETY.md
├── LICENSE
├── docs/
│   ├── 01_project_context.md
│   ├── 02_kicad_beginner_setup.md
│   ├── 03_pcb_floorplan.md
│   ├── 04_routing_rules.md
│   ├── 05_manufacturing_notes.md
│   ├── planning/
│   │   └── ESP32_Handheld_PCB_KiCad_Planning_Workbook.xlsx
│   └── references/
│       └── related_projects.md
├── hardware/
│   ├── bom/components.csv
│   ├── pinout/pin_map.csv
│   ├── checklists/
│   │   ├── schematic_checklist.md
│   │   ├── layout_checklist.md
│   │   └── bringup_test_plan.md
│   ├── fabrication/pick_and_place_example.csv
│   └── kicad/START_HERE.md
├── firmware/
│   └── README.md
└── enclosure/
    └── enclosure_notes.md
```

## Suggested board size

For a first handheld PCB:

```text
Width: 60 mm
Height: 100 mm
Layers: 2-layer V1, 4-layer optional later
Thickness: 1.6 mm
Copper: 1 oz
Finish: HASL for low cost, ENIG if budget allows
```

## KiCad workflow

1. Start a blank KiCad project.
2. Draw the schematic first.
3. Assign footprints.
4. Update PCB from schematic.
5. Draw the PCB outline on `Edge.Cuts`.
6. Place ESP32 antenna at the top edge.
7. Place OLED and buttons for handheld ergonomics.
8. Route power first, then signals.
9. Add GND pours on both layers.
10. Run ERC and DRC.
11. Export Gerbers, drill files, BOM, and pick-and-place files.

## Defensive / authorized use only

This repo is not for building tools that attack networks, capture credentials, jam signals, clone access cards, or bypass devices. Only test your own devices, your own lab, or systems where you have explicit written permission.

