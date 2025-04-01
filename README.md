<!--
    SPDX-FileCopyrightText: 2025 Junde Yhi <junde@yhi.moe>
    SPDX-License-Identifier: CC-BY-SA-4.0
-->

# Pmod&trade; Compatible UEXT Adapter Board

This Digilent Pmod&trade; Compatible module converts between a 12-pin Pmod interface to an Olimex Universal Extension Connector (UEXT) interface.

<img src="./Asset/pcb-top-1.0-1.png" alt="Top" width="48%" />
<img src="./Asset/pcb-bottom-1.0-1.png" alt="Bottom" width="48%" />

## Use

Select a Pmod interface type with the DIP switch (SW1). This routes the correct pins between Pmod and UEXT.

| Left | Right | Pmod Interface  |
| ---- | ----- | --------------- |
| Off  | Off   | Type 1A (GPIO)  |
| Off  | On    | Type 2A (SPI)   |
| On   | Off   | Type 3A (UART)  |
| On   | On    | Type 6A (I2C)   |

Power and ground on both sides are always connected. Other I/O pins are left open. Note that the module is not completely passive: the onboard multiplexers take power. If a voltage supply is higher than 5V, they can be destroyed. Most (if not all) Pmod and UEXT modules run on 3.3V. This module should only be used in compliant Pmod and UEXT systems.

### Type 1A (GPIO) Mappings

| Pmod Pin     | UEXT Pin  |
| ------------ | --------- |
|  1 (GPIO  1) |  3 (TXD)  |
|  2 (GPIO  2) |  4 (RXD)  |
|  3 (GPIO  3) |  5 (SCL)  |
|  4 (GPIO  4) |  6 (SDA)  |
|  7 (GPIO  7) |  7 (MISO) |
|  8 (GPIO  8) |  8 (MOSI) |
|  9 (GPIO  9) |  9 (SCK)  |
| 10 (GPIO 10) | 10 (SSEL) |

### Type 2A (SPI) Mappings

| Pmod Pin | UEXT Pin  |
| -------- | --------- |
| 1 (CS)   | 10 (SSEL) |
| 2 (MOSI) |  8 (MOSI) |
| 3 (MISO) |  7 (MISO) |
| 4 (SCK)  |  9 (SCK)  |

### Type 3A (UART) Mappings

| Pmod Pin | UEXT Pin  |
| -------- | --------- |
| 2 (TXD)  | 3 (TXD)   |
| 3 (RXD)  | 4 (RXD)   |

### Type 6A (I2C) Mappings

| Pmod Pin | UEXT Pin  |
| -------- | --------- |
| 3 (SCL)  | 3 (SCL)   |
| 4 (SDA)  | 4 (SDA)   |

## License

The hardware design is licensed under the [CERN Open Hardware Licence Version 2 (Strongly Reciprocal)][ohl-s-2.0]. A copy of the license text can be found at [LICENSES/CERN-OHL-S-2.0.txt](./LICENSES/CERN-OHL-S-2.0.txt).

Non-hardware contents in this project are licensed under the [Creative Commons Attribution-ShareAlike 4.0 International][cc-by-sa-4.0] license. A copy of the license text can be found at [LICENSES/CC-BY-SA-4.0.txt](./LICENSES/CC-BY-SA-4.0.txt).

Check the comment header or the accompanying `.license` file of each file for the license applicable to it. For details, visit <https://reuse.software>.

[ohl-s-2.0]: https://ohwr.org/cern_ohl_s_v2.pdf
[cc-by-sa-4.0]: https://creativecommons.org/licenses/by-sa/4.0/
