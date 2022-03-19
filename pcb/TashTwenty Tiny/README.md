# TashTwenty Tiny

This is a dual PCB design, using mostly through hole components (with the exeption of the SD connector). It's designed this way to be period correct and easy to build for people who don't like soldering SMT components

This folder contains the source KiKad files for the main board. Please check the DB19_IDC20 subfolder for the DB19 to IDC20 adapter. 

### BOM (main board)
Here is the BOM for the main board. Part number are what was tested on prototypes board but you may find alternatives easily, especially resistors and sockets

| Reference(s)          | Value      | Quantity | Notes                                  | Part number           |
|-----------------------|------------|----------|----------------------------------------|-----------------------|
| C1, C2                | 2.2uF      | 2        | radial electrolytic capacitors 4x1.5mm | Jamicon SHR2R2M1HC07M |
| C3, C4                | 100nF      | 2        | ceramic capacitor 5.08mm               | Weltron 453358        |
| D1                    | Green      | 1        | 5mm green LED                          | Kingbright L-53SGD    |
| D2                    | Yellow+Red | 1        | 5mm dual color common cathode LED      | Kingbright L-59EYW    |
| J1                    | SD Card    | 1        | SD Card connector                      | TE 2041021-1          |
| J2                    | IDC20      | 1        | IDC 2x10 Header                        | BLK 10120560          |
| Q1                    | BC337      | 1        | NPN BJT Transistor                     | BC337                 |
| R10, R11              | 330Ω       | 2        | standard 0.25W carbon film resistor    | TRU TC-CFR0W4J0331    |
| R1, R3, R5, R8        | 1200Ω      | 4        | standard 0.25W carbon film resistor    | TRU TC-CFR0W4J0122    |
| R2, R4, R6            | 2200Ω      | 3        | standard 0.25W carbon film resistor    | TRU TC-CFR0W4J0222    |
| R7, R9, R12, R13, R14 | 10kΩ       | 5        | standard 0.25W carbon film resistor    | TRU TC-CFR0W4J0103    |
| U1                    | PIC16F1825 | 1        | PIC 8-bit Microcontroller (DIP-14)     | PIC16F1825-I/P        |
| U2                    | 74ACT08    | 1        | Quad TTL 2-Input AND Gate              | SN74ACT08N            |
| U3                    | 3.3V LDO   | 1        |                                        | MCP1700-3302E/TO      |

Optional

| Reference(s)          | Value      | Quantity | Notes                                  | Part number         |
|-----------------------|------------|----------|----------------------------------------|---------------------|
| J1                    | -          | 1        | 1x2 header + jumper or wire            | -                   |
| U1, U2				| socket     | 2        | DIP-14 socket                          | TRU 14-LC-TT        |
| Case   				| ABS        | 1        | Instrument Case, ABS 2.6x2.6"          | HM 1593K(TBU|GY|BK) |

Using sockets is recommended because it will allow you to reclaim the gates and microcontroler if your board is broken.
J1 is reserver for future use, you may want to use a wire for it. (or a resistor leg)

### BOM (adapter board)

| Reference(s)          | Value      | Quantity | Notes                                  | Part number        |
|-----------------------|------------|----------|----------------------------------------|--------------------|
| J1                    | IDC20      | 1        | IDC 2x10 Header                        | BLK 10120560       |
| J2                    | DB19       | 1        | DB19 wire male connector               | Good luck.         |


### BOM (external links)
Here is a mouser link (without the case):
- https://www.mouser.fr/ProjectManager/ProjectDetail.aspx?AccessID=6e66469657

### Building

Building is straightworfard. It's recommended to start with the SD Card connector, then components, and headers + sockets last.
