# KiCad Beginner Setup

## 1. Create a blank project

Open KiCad:

```text
File → New Project → New Project
```

Recommended name:

```text
Esp32-Marauder-CheeseCake
```

## 2. Main KiCad files

```text
.kicad_sch = schematic/circuit drawing
.kicad_pcb = PCB layout
.kicad_pro = project settings
```

## 3. Start with the schematic

Open **Schematic Editor** first.

Useful shortcuts:

```text
A = Add symbol
W = Wire
L = Net label
R = Rotate
M = Move
Delete = Delete
```

## 4. Add symbols in blocks

Recommended schematic order:

1. ESP32 module.
2. USB-C power.
3. USB-UART programmer.
4. 3.3 V regulator.
5. LiPo charger.
6. OLED connector.
7. Buttons.
8. Battery sense divider.
9. Optional headers.

## 5. Use labels, not giant wires

Example:

```text
ESP32 GPIO21 → label SDA
OLED SDA pin → label SDA
```

KiCad treats equal labels as connected.

## 6. Assign footprints

After the schematic is mostly done:

```text
Tools → Assign Footprints
```

Recommended common footprints:

```text
ESP32 module: RF_Module:ESP32-WROOM-32
Resistor: Resistor_SMD:R_0603_1608Metric
Capacitor: Capacitor_SMD:C_0603_1608Metric
Button: Button_Switch_SMD:SW_SPST_TL3342
Battery: Connector_JST:JST_PH_B2B-PH-K_1x02_P2.00mm_Vertical
OLED header: Connector_PinHeader_2.54mm:PinHeader_1x04_P2.54mm_Vertical
CC1101 header: Connector_PinHeader_2.54mm:PinHeader_2x04_P2.54mm_Vertical
```

## 7. Update PCB from schematic

In KiCad:

```text
Tools → Update PCB from Schematic
```

Then arrange footprints in PCB Editor.

