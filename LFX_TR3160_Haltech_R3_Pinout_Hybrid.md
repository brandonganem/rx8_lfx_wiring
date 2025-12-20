# Haltech Nexus R3 Pinout - GM LFX + TR-3160 (Retrofitted to K24 Harness)

This pinout is designed to reuse as much of the existing K24 RX8 wiring harness as possible.

## Connector A (34 Pin)
| Pin | Function | Description | K24 Harness Wire | Changes Required |
| :--- | :--- | :--- | :--- | :--- |
| A01 | INJ 1 | Cylinder 1 Injector | Existing | None |
| A02 | INJ 2 | Cylinder 2 Injector | Existing | None |
| A03 | INJ 3 | Cylinder 3 Injector | Existing | None |
| A04 | INJ 4 | Cylinder 4 Injector | Existing | None |
| A05 | INJ 5 | Cylinder 5 Injector | **Was Killswitch** | **Repin / New Wire** |
| A06 | INJ 6 | Cylinder 6 Injector | **Was Unused** | **Add Wire** |
| A07 | INJ 7 | Unused | | |
| A08 | INJ 8 | Unused | | |
| A09 | DPO 1 | Brake Pedal Switch | Existing | None |
| A10 | GND | Battery Ground Out | Existing | None |
| A11 | GND | Battery Ground Out | Existing | None |
| A12 | DPO 2 | Clutch Pedal Switch | Existing | None |
| A13 | IGN SW | Ignition Switch Input | Existing | None |
| A14 | DPO 3 | Alternator Control | Existing | None (Verify LFX Alt Type) |
| A15 | DPO 4 | VVT Bank 1 Intake | **Was Unused** | **Add Wire** |
| A16 | DPO 5 | VVT Bank 1 Exhaust | **Was VTEC** | **Repurpose Wire** |
| A17 | DPO 6 | VVT Bank 2 Intake | **Was VTC** | **Repurpose Wire** |
| A18 | HBO 5 | Starter Relay | **Was Harness +12V** | **Repurpose (High Side)** |
| A19 | HBO 1 | DBW Motor + | Existing | None |
| A20 | HBO 2 | DBW Motor - | Existing | None |
| A21 | HBO 3 | VVT Bank 2 Exhaust | **Was VTC Power** | **Repurpose (Set as Low Side)** |
| A22 | HBO 4 | Reverse Lockout | **Was IGN Power** | **Repurpose (Set as Low Side)** |
| A23 | CAN 1 H | RX8 CAN High | Existing | None |
| A24 | CAN 1 L | RX8 CAN Low | Existing | None |
| A25 | HBO 6 | Unused | Was INJ Power | |
| A26 | +12V | 12V Low Current Out | Existing | None |
| A27 | IGN 1 | Cylinder 1 Coil | Existing | None |
| A28 | IGN 2 | Cylinder 2 Coil | Existing | None |
| A29 | IGN 3 | Cylinder 3 Coil | Existing | None |
| A30 | IGN 4 | Cylinder 4 Coil | Existing | None |
| A31 | IGN 5 | Cylinder 5 Coil | **Was Rev Switch** | **Repin / New Wire** |
| A32 | IGN 6 | Cylinder 6 Coil | **Was Unused** | **Add Wire** |
| A33 | IGN 7 | Unused | | |
| A34 | IGN 8 | Unused | | |

## Connector C (34 Pin)
| Pin | Function | Description | K24 Harness Wire | Changes Required |
| :--- | :--- | :--- | :--- | :--- |
| C01 | Trigger + | Crank Position Sensor | Existing | None |
| C02 | Trigger - | Crank Ground | Existing | None |
| C03 | Home + | Cam 1 (Bank 1 Intake) | **Was Exh Cam** | **Repurpose** |
| C04 | Home - | Cam Ground | Existing | None |
| C05 | SPI 1 | Cam 2 (Bank 1 Exhaust)| **Was Int Cam** | **Repurpose** |
| C06 | SPI 2 | Cam 3 (Bank 2 Intake) | **Was Oil Press** | **Repin (Move Oil Press)** |
| C07 | SPI 3 | Cam 4 (Bank 2 Exhaust)| **Was Flex Fuel** | **Repin (Move Flex)** |
| C08 | SPI 4 | VSS (Speed Sensor) | **Was Neutral Sw** | **Repurpose** |
| C09 | +8V | Sensor 8V | Existing | None |
| C10 | AVI 1 | MAP Sensor | Existing | None (If using ext MAP) |
| C11 | AVI 2 | Oil Temp | Existing | None |
| C12 | AVI 3 | IAT | Existing | None |
| C13 | AVI 4 | Oil Pressure | **Was Spare 2** | **Move Oil Press Here** |
| C14 | AVI 5 | TPS 1 (Throttle) | Existing | None |
| C15 | AVI 6 | TPS 2 (Throttle) | Existing | None |
| C16 | AVI 7 | Pedal Pos 1 | Existing | None |
| C17 | AVI 8 | Pedal Pos 2 | Existing | None |
| C18 | AVI 9 | ECT (Coolant) | Existing | None |
| C19 | SPI 5 | Trans Temp | **Was Trans Temp** | **Keep Existing** |
| C20 | SPI 6 | Flex Fuel | **Was Unused** | **Move Flex Here** |
| C21 | CAN 2 H | Haltech CAN | Existing | None |
| C22 | CAN 2 L | Haltech CAN | Existing | None |
| C23 | Knock 1 | Knock Bank 1 | Existing | None |
| C24 | Knock 2 | Knock Bank 2 | **Was Unused** | **Add Wire** |
| C25 | +5V | Sensor +5V | Existing | None |
| C26 | Sig Gnd | Signal Ground | Existing | None |
| C27 | AVI 10 | Fuel Pressure | Existing | None |
| C28 | AVI 11 | Reverse Switch Input | **Was ??** | **Move Rev Switch Here** |
| C29 | WB1 H+ | Wideband | Existing | None |
| C30 | WB1 Ip | Wideband | Existing | None |
| C31 | WB1 Vs | Wideband | Existing | None |
| C32 | WB1 Vs/Ip | Wideband | Existing | None |
| C33 | WB1 H- | Wideband | Existing | None |
| C34 | WB1 Rcal | Wideband | Existing | None |

## Connector E (4 Pin - High Current)
| Pin | Function | Description | K24 Harness Wire | Changes Required |
| :--- | :--- | :--- | :--- | :--- |
| E01 | HCO 1 | Ignition Coils Power | **Was Water Pump** | **Repurpose** |
| E02 | HCO 2 | Cooling Fan | Existing | None |
| E03 | HCO 3 | Injectors + VVT Power | **Was Starter** | **Repurpose** |
| E04 | HCO 4 | Fuel Pump | Existing | None |

## Summary of Major Moves
1.  **Injectors:** Added Inj 5 & 6 (A05, A06).
2.  **Coils:** Added Ign 5 & 6 (A31, A32).
3.  **VVT:** Repurposed VTEC/VTC wires and added new ones for 4x Solenoids.
4.  **Cams:** Took over SPI 2 & 3 (Oil Press/Flex) for Cam sensors.
5.  **Sensors:** Moved Oil Pressure to AVI 4 (C13) and Flex Fuel to SPI 6 (C20).
6.  **Reverse:** Moved Reverse Switch Input to AVI 11 (C28).
7.  **Power:** Repurposed Water Pump and Starter power feeds for Coils and Injectors.
8.  **Starter:** Added Starter Relay control on HBO 5 (A18).
