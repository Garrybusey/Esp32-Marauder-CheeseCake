# Routing Rules

## Beginner-safe PCB rules

```text
Minimum track width: 0.20 mm
Minimum clearance: 0.20 mm
Via diameter: 0.80 mm
Via drill: 0.40 mm
Signal traces: 0.20–0.30 mm
Power traces: 0.50–1.00 mm
Battery/USB traces: 0.75–1.20 mm
```

These are conservative and should work with common low-cost PCB manufacturers.

## Recommended routing order

1. Place components properly first.
2. Route USB/power input.
3. Route 3.3 V rail.
4. Route ESP32 programming pins.
5. Route OLED I2C.
6. Route buttons.
7. Route SPI headers.
8. Route optional modules.
9. Add GND pours on top and bottom.
10. Add GND stitching vias.

## Ground plane

In PCB Editor:

```text
Add Filled Zone → Net: GND → Layer: F.Cu
Add Filled Zone → Net: GND → Layer: B.Cu
Press B to refill zones
```

Do not pour copper inside the ESP32 antenna keepout.

## Power advice

ESP32 current spikes can cause brownouts. Use:

- 10 uF near ESP32 3.3 V input,
- 0.1 uF near ESP32 3.3 V input,
- 47 uF bulk capacitor on 3.3 V rail if space allows,
- wide 3.3 V and GND routing.

