# Circuit Drawing Guide

[Open the schematic image](images/schematic/diy_atx_psu.svg).

| Position | Circuit |
|---|---|
| Left | J1 ATX supply, with the original fan M1 shown inside |
| Upper right | F1–F3 and the 12 V, 5 V and 3.3 V terminals |
| Centre | U1 ZK-4KX and the adjustable terminals |
| Lower centre | R1/D1 standby indicator and R2/D2 power-good indicator |
| Lower right | J8 12 V socket and J9 5 V LED strip |
| Bottom | SW1 PS_ON switch and the COM return to black terminal J5 |

Follow the drawn wires from the supply to each load and its return. A dot marks a junction; crossing wires without a dot are not connected. The adjustable negative terminal J7 returns to the module's OUT− pin rather than joining the external COM bus directly.

J1 groups equivalent signals from the conventional motherboard-side 24-pin ATX map. The pin numbers are retained in the KiCad symbol and listed in the [wire and pin table](wiring-and-protection.md). This is a signal map, not a physical view of the connector or PSU board pads.

F1–F3 are the three fixed-output fuses. The adjustable positive terminal connects directly to OUT+, with no separate external fuse. Fuse-selection calculations are in the report. R1 and R2 are the 1 kΩ LED resistors. The original PSU fan is shown within J1 because its internal wiring is not part of the external distribution drawing.

The source and module are represented by their external signals. See the [circuit discussion](design-review.md) for the return paths, PWR_OK loading and branch protection.
