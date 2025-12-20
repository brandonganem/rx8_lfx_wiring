# Haltech Nexus R3 Pinout - GM LFX + TR-3160 (Retrofitted to K24 Harness)

This pinout is designed to reuse as much of the existing K24 RX8 wiring harness as possible.

## Wiring Standards
*   **Wire Type:** TXL Automotive Wire (Thin Wall Cross-Linked Polyethylene).
*   **Wire Colors:** Colors listed below are standard aftermarket/Haltech conventions for the *ECU side* of the harness (the new wires you are running).
    *   **IMPORTANT:** You are splicing into an OE GM Engine Harness. The wire colors on the **GM Pigtails** will likely **NOT MATCH** the colors listed below.
    *   **Action:** Always match the **Pin Position** on the GM connector, not the color.
*   **Wire Sizes:**
    *   **Power (High Current):** 12-14 AWG (HCOs).
    *   **Power (Med Current):** 16-18 AWG (DBW, Solenoids).
    *   **Signals / Sensors:** 20-22 AWG.
    *   **Shielded:** Crank/Cam/Knock sensors use shielded cable (2-core or 3-core).

## Connector A (34 Pin)
| Pin | Function | Description | Wire Size (TXL) | Wire Color (Ref) | K24 Harness Wire | Changes Required |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| A01 | INJ 1 | Cylinder 1 Injector | 20 AWG | Blue / Red | Existing | None |
| A02 | INJ 2 | Cylinder 2 Injector | 20 AWG | Blue / Yellow | Existing | None |
| A03 | INJ 3 | Cylinder 3 Injector | 20 AWG | Blue / Green | Existing | None |
| A04 | INJ 4 | Cylinder 4 Injector | 20 AWG | Blue / Orange | Existing | None |
| A05 | INJ 5 | Cylinder 5 Injector | 20 AWG | Blue / Black | **Was Killswitch** | **Repin / New Wire** |
| A06 | INJ 6 | Cylinder 6 Injector | 20 AWG | Blue / Purple | **Was Unused** | **Add Wire** |
| A07 | INJ 7 | Kill Switch Input | 20 AWG | White / Blue | **Unused** | **Digital Input** |
| A08 | INJ 8 | Spare Connector Pin 1 | 20 AWG | White / Green | **Unused** | **Aux Out / Switch In** |
| A09 | DPO 1 | Brake Pedal Switch | 20 AWG | Violet / Red | Existing | None |
| A10 | GND | Battery Ground Out | 14 AWG | Black | Existing | None |
| A11 | GND | Battery Ground Out | 14 AWG | Black | Existing | None |
| A12 | DPO 2 | Clutch Pedal Switch | 20 AWG | Violet / Blue | Existing | None |
| A13 | IGN SW | Ignition Switch Input | 20 AWG | Pink / White | Existing | None |
| A14 | DPO 3 | Alternator Control | 20 AWG | Violet / Green | Existing | None (Verify LFX Alt Type) |
| A15 | DPO 4 | VVT Bank 1 Intake | 20 AWG | Violet / Yellow | **Was Unused** | **Add Wire** |
| A16 | DPO 5 | VVT Bank 1 Exhaust | 20 AWG | Violet / Orange | **Was VTEC** | **Repurpose Wire** |
| A17 | DPO 6 | VVT Bank 2 Intake | 20 AWG | Violet / White | **Was VTC** | **Repurpose Wire** |
| A18 | HBO 5 | Starter Relay | 18 AWG | Gray / Red | **Was Harness +12V** | **Repurpose (High Side)** |
| A19 | HBO 1 | DBW Motor + | 18 AWG | Orange / Red | Existing | None |
| A20 | HBO 2 | DBW Motor - | 18 AWG | Orange / Blue | Existing | None |
| A21 | HBO 3 | VVT Bank 2 Exhaust | 20 AWG | Gray / Yellow | **Was VTC Power** | **Repurpose (Set as Low Side)** |
| A22 | HBO 4 | Spare Connector Pin 2 | 18 AWG | Gray / Green | **Was IGN Power** | **Available** |
| A23 | CAN 1 H | RX8 CAN High | 22 AWG (Twisted) | Yellow | Existing | None |
| A24 | CAN 1 L | RX8 CAN Low | 22 AWG (Twisted) | Green | Existing | None |
| A25 | HBO 6 | Spare Connector Pin 3 | 18 AWG | Gray / Black | Was INJ Power | |
| A26 | +12V | 12V Low Current Out | 20 AWG | Red / White | Existing | None |
| A27 | IGN 1 | Cylinder 1 Coil | 20 AWG | Yellow / Red | Existing | None |
| A28 | IGN 2 | Cylinder 2 Coil | 20 AWG | Yellow / Yellow | Existing | None |
| A29 | IGN 3 | Cylinder 3 Coil | 20 AWG | Yellow / Green | Existing | None |
| A30 | IGN 4 | Cylinder 4 Coil | 20 AWG | Yellow / Orange | Existing | None |
| A31 | IGN 5 | Cylinder 5 Coil | 20 AWG | Yellow / Black | **Was Rev Switch** | **Repin / New Wire** |
| A32 | IGN 6 | Cylinder 6 Coil | 20 AWG | Yellow / Purple | **Was Unused** | **Add Wire** |
| A33 | IGN 7 | Reverse Switch Input | 20 AWG | Yellow / Blue | **Was Unused** | **Digital Input (0-12V)** |
| A34 | IGN 8 | Reverse Lockout | 20 AWG | Yellow / White | **Was Unused** | **Low Side Output (Solenoid)** |

## Connector C (34 Pin)
| Pin | Function | Description | Wire Size (TXL) | Wire Color (Ref) | K24 Harness Wire | Changes Required |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| C01 | Trigger + | Crank Position Sensor | 22 AWG Shielded | Yellow | Existing | None |
| C02 | Trigger - | Crank Ground | 22 AWG Shielded | Blue | Existing | None |
| C03 | Home + | Cam 1 (Bank 1 Intake) | 22 AWG Shielded | Yellow | **Was Exh Cam** | **Repurpose** |
| C04 | Home - | Cam Ground | 22 AWG Shielded | Blue | Existing | None |
| C05 | SPI 1 | Cam 2 (Bank 1 Exhaust)| 22 AWG | White / Red | **Was Int Cam** | **Repurpose** |
| C06 | SPI 2 | Cam 3 (Bank 2 Intake) | 22 AWG | White / Blue | **Was Oil Press** | **Repin (Move Oil Press)** |
| C07 | SPI 3 | Cam 4 (Bank 2 Exhaust)| 22 AWG | White / Green | **Was Flex Fuel** | **Repin (Move Flex)** |
| C08 | SPI 4 | Flex Fuel | 22 AWG | White / Yellow | **Was Neutral Sw** | **Repurpose (Use CAN Speed)** |
| C09 | +8V | Unused | N/A | N/A | Existing | **Cap / Depin** |
| C10 | AVI 1 | MAP Sensor | 22 AWG | Orange / White | Existing | **Keep External MAP** |
| C11 | AVI 2 | Combo Oil Temp | 22 AWG | Orange / Black | Existing | None |
| C12 | AVI 3 | IAT | 22 AWG | Orange / Red | Existing | None |
| C13 | AVI 4 | Oil Pressure (Stock) | 22 AWG | Orange / Blue | **Was Spare 2** | **Move Oil Press Here** |
| C14 | AVI 5 | TPS 1 (Throttle) | 22 AWG | Orange / Green | Existing | None |
| C15 | AVI 6 | TPS 2 (Throttle) | 22 AWG | Orange / Yellow | Existing | None |
| C16 | AVI 7 | Pedal Pos 1 | 22 AWG | Orange / Purple | Existing | None |
| C17 | AVI 8 | Pedal Pos 2 | 22 AWG | Orange / Gray | Existing | None |
| C18 | AVI 9 | ECT (Coolant) | 22 AWG | Orange / Brown | Existing | None |
| C19 | SPI 5 | Combo Oil Pressure | 22 AWG | White / Orange | **Was Trans Temp** | **Repurpose (0-5V)** |
| C20 | SPI 6 | Coolant Pressure | 22 AWG | White / Purple | **Was Unused** | **Add Sensor (0-5V)** |
| C21 | CAN 2 H | Haltech CAN | 22 AWG (Twisted) | White | Existing | None |
| C22 | CAN 2 L | Haltech CAN | 22 AWG (Twisted) | Blue | Existing | None |
| C23 | Knock 1 | Knock Bank 1 | 22 AWG Shielded | White | Existing | None |
| C24 | Knock 2 | Knock Bank 2 | 22 AWG Shielded | White | **Was Unused** | **Add Wire** |
| C25 | +5V | Sensor +5V | 20 AWG | Orange | Existing | None |
| C26 | Sig Gnd | Signal Ground | 20 AWG | Black / White | Existing | None |
| C27 | AVI 10 | Fuel Pressure | 22 AWG | Green / Red | Existing | None |
| C28 | AVI 11 | Trans Temp | 22 AWG | Green / Blue | **Was Rev Switch** | **Move Trans Temp Here** |
| C29 | WB1 H+ | Wideband | Haltech Cable | Red | Existing | None |
| C30 | WB1 Ip | Wideband | Haltech Cable | White | Existing | None |
| C31 | WB1 Vs | Wideband | Haltech Cable | Black | Existing | None |
| C32 | WB1 Vs/Ip | Wideband | Haltech Cable | Gray | Existing | None |
| C33 | WB1 H- | Wideband | Haltech Cable | Yellow | Existing | None |
| C34 | WB1 Rcal | Wideband | Haltech Cable | Green | Existing | None |

## Connector E (4 Pin - High Current)
| Pin | Function | Description | Wire Size (TXL) | Wire Color (Ref) | K24 Harness Wire | Changes Required |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| E01 | HCO 1 | Ignition Coils Power | 12 AWG | Red / Blue | **Was Water Pump** | **Repurpose** |
| E02 | HCO 2 | Cooling Fan | 12 AWG | Red / Green | Existing | None |
| E03 | HCO 3 | Injectors + VVT Power | 14 AWG | Red / Yellow | **Was Starter** | **Repurpose** |
| E04 | HCO 4 | Fuel Pump | 12 AWG | Red / Orange | Existing | None |

## Summary of Major Moves
1.  **Injectors:** Added Inj 5 & 6 (A05, A06).
2.  **Coils:** Added Ign 5 & 6 (A31, A32).
3.  **VVT:** Repurposed VTEC/VTC wires and added new ones for 4x Solenoids.
4.  **Cams:** Took over SPI 2 & 3 (Oil Press/Flex) for Cam sensors.
5.  **Sensors:** Moved Oil Pressure to AVI 4 (C13) and Flex Fuel to SPI 6 (C20).
6.  **Reverse:** Assigned Reverse Switch Input to IGN 7 (A33).
7.  **Trans Temp:** Moved to AVI 11 (C28) for proper pull-up support.
8.  **Combo Sensor:** Added Aftermarket Oil Pressure to SPI 5 (C19) and Oil Temp to AVI 2 (C11).
9.  **Power:** Repurposed Water Pump and Starter power feeds for Coils and Injectors.
10. **Starter:** Added Starter Relay control on HBO 5 (A18).
11. **Coolant Pressure:** Added Coolant Pressure Sensor to SPI 6 (C20).
12. **Flex Fuel:** Moved to SPI 4 (C08) as VSS is now CAN-based.
13. **Kill Switch:** Added Kill Switch Input to INJ 7 (A07).
14. **Spare Connector:** Created 6-Pin DTM with INJ 8, HBO 4, HBO 6, 12V, 5V, Gnd.
