# Haltech Nexus R3 Pinout - GM LFX + TR-3160

## Connector A (34 Pin)
| Pin | Function | Description | Wire Color | Notes |
| :--- | :--- | :--- | :--- | :--- |
| A01 | INJ 1 | Cylinder 1 Injector (Trigger) | | Switched Ground |
| A02 | INJ 2 | Cylinder 2 Injector (Trigger) | | Switched Ground |
| A03 | INJ 3 | Cylinder 3 Injector (Trigger) | | Switched Ground |
| A04 | INJ 4 | Cylinder 4 Injector (Trigger) | | Switched Ground |
| A05 | INJ 5 | Cylinder 5 Injector (Trigger) | | Switched Ground |
| A06 | INJ 6 | Cylinder 6 Injector (Trigger) | | Switched Ground |
| A07 | INJ 7 | Unused | | |
| A08 | INJ 8 | Unused | | |
| A09 | DPO 1 | VVT Bank 1 Intake Solenoid | | Low Side (PWM) |
| A10 | GND | Battery Ground Out | | Shield Ground |
| A11 | GND | Battery Ground Out | | Shield Ground |
| A12 | DPO 2 | VVT Bank 1 Exhaust Solenoid | | Low Side (PWM) |
| A13 | IGN SW | Ignition Switch Input | | 12V Wake Up |
| A14 | DPO 3 | VVT Bank 2 Intake Solenoid | | Low Side (PWM) |
| A15 | DPO 4 | VVT Bank 2 Exhaust Solenoid | | Low Side (PWM) |
| A16 | DPO 5 | Reverse Lockout Solenoid | | Low Side (On/Off) |
| A17 | DPO 6 | Unused | | |
| A18 | HBO 5 | Unused | | |
| A19 | HBO 1 | DBW Motor + | | Electronic Throttle Motor |
| A20 | HBO 2 | DBW Motor - | | Electronic Throttle Motor |
| A21 | HBO 3 | Unused | | |
| A22 | HBO 4 | Unused | | |
| A23 | CAN 1 H | CAN High | | Main CAN Bus |
| A24 | CAN 1 L | CAN Low | | Main CAN Bus |
| A25 | HBO 6 | Unused | | |
| A26 | +12V | 12V Low Current Out | | Relay Trigger (Optional) |
| A27 | IGN 1 | Cylinder 1 Coil (Trigger) | | 5V Logic Signal |
| A28 | IGN 2 | Cylinder 2 Coil (Trigger) | | 5V Logic Signal |
| A29 | IGN 3 | Cylinder 3 Coil (Trigger) | | 5V Logic Signal |
| A30 | IGN 4 | Cylinder 4 Coil (Trigger) | | 5V Logic Signal |
| A31 | IGN 5 | Cylinder 5 Coil (Trigger) | | 5V Logic Signal |
| A32 | IGN 6 | Cylinder 6 Coil (Trigger) | | 5V Logic Signal |
| A33 | IGN 7 | Unused | | |
| A34 | IGN 8 | Unused | | |

## Connector C (34 Pin)
| Pin | Function | Description | Wire Color | Notes |
| :--- | :--- | :--- | :--- | :--- |
| C01 | Trigger + | Crank Position Sensor Signal | | 58X Signal |
| C02 | Trigger - | Crank Sensor Ground | | |
| C03 | Home + | Cam 1 (Bank 1 Intake) Signal | | Hall Effect |
| C04 | Home - | Cam Sensor Ground | | |
| C05 | SPI 1 | Cam 2 (Bank 1 Exhaust) Signal | | Hall Effect |
| C06 | SPI 2 | Cam 3 (Bank 2 Intake) Signal | | Hall Effect |
| C07 | SPI 3 | Cam 4 (Bank 2 Exhaust) Signal | | Hall Effect |
| C08 | SPI 4 | VSS (Vehicle Speed Sensor) | | Transmission Speed |
| C09 | +8V | Sensor 8V Supply | | Not typically used |
| C10 | AVI 1 | DBW TPS 1 Signal | | Throttle Position |
| C11 | AVI 2 | DBW TPS 2 Signal | | Throttle Position |
| C12 | AVI 3 | Pedal APP 1 Signal | | Accelerator Pedal |
| C13 | AVI 4 | Pedal APP 2 Signal | | Accelerator Pedal |
| C14 | AVI 5 | IAT (Intake Air Temp) | | |
| C15 | AVI 6 | CLT (Coolant Temp) | | |
| C16 | AVI 7 | Oil Pressure Signal | | 0-5V Sensor |
| C17 | AVI 8 | Fuel Pressure Signal | | 0-5V Sensor |
| C18 | AVI 9 | Reverse Switch Input | | Trans Reverse Switch |
| C19 | SPI 5 | Unused | | |
| C20 | SPI 6 | Flex Fuel Sensor | | Optional |
| C21 | CAN 2 H | CAN 2 High | | Aux CAN Bus |
| C22 | CAN 2 L | CAN 2 Low | | Aux CAN Bus |
| C23 | Knock 1 | Knock Sensor Bank 1 | | |
| C24 | Knock 2 | Knock Sensor Bank 2 | | |
| C25 | +5V | Sensor 5V Supply | | Ref for DBW, Pedal, Pressures |
| C26 | Sig Gnd | Signal Ground | | Ground for Sensors |
| C27 | AVI 10 | Unused | | |
| C28 | AVI 11 | Unused | | |
| C29 | WB1 H+ | Wideband Heater + | | LSU 4.9 Pin 3 |
| C30 | WB1 Ip | Wideband Ip | | LSU 4.9 Pin 1 |
| C31 | WB1 Vs | Wideband Vs/Cell | | LSU 4.9 Pin 2 |
| C32 | WB1 Vs/Ip | Wideband Common | | LSU 4.9 Pin 6 |
| C33 | WB1 H- | Wideband Heater - | | LSU 4.9 Pin 4 |
| C34 | WB1 Rcal | Wideband Cal Resistor | | LSU 4.9 Pin 5 |

## Connector E (4 Pin - High Current)
| Pin | Function | Description | Wire Color | Notes |
| :--- | :--- | :--- | :--- | :--- |
| E01 | HCO 1 | Fuel Pump Power | | 25A Max |
| E02 | HCO 2 | Cooling Fan Power | | 25A Max |
| E03 | HCO 3 | Ignition Coils Power | | 25A Max |
| E04 | HCO 4 | Injectors + VVT Solenoids Power | | 25A Max |
