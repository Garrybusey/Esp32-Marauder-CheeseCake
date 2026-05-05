# Safety, Legal, and Ethics

This project is intended for **learning PCB design** and building a **defensive/authorized wireless diagnostics handheld**.

## Allowed project direction

Safe/defensive features:

- Wi-Fi SSID visibility for your own lab environment.
- BLE visibility for your own lab devices.
- OLED-based hardware menu.
- Battery monitoring.
- GPIO diagnostics.
- IR remote testing for your own devices.
- NFC reading for your own test tags.
- Sub-GHz packet tests only between your own boards/modules on legal ISM frequencies.

## Not allowed in this repo

Do not add or request:

- Deauthentication attacks.
- Evil portal / fake login collection.
- Password or credential capture.
- Beacon spam meant to disrupt others.
- RF jamming.
- Access-card cloning or bypass.
- Unauthorized RF replay.
- Interference with networks/devices you do not own.

## Regulatory reminder

Radio rules depend on country/region. Sub-GHz transmission, NFC/RFID behavior, antenna choice, output power, duty cycle, and product distribution may require compliance work such as FCC, ISED, CE/RED, or other testing.

Before distributing or selling hardware:

- Confirm legal frequency bands.
- Confirm output power limits.
- Confirm antenna restrictions.
- Use certified modules where possible.
- Do pre-compliance EMC/RF testing.
- Do not ship offensive firmware.

