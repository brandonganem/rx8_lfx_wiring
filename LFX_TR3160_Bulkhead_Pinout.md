# Engine Bulkhead Connector Strategy
**Approach:** Use existing 47-pin connector as-is + add small Aux connector for new signals.

---

# CONNECTOR 1: Main 47-Pin (NO REWIRING)
**Connector Type:** Deutsch HDP20 Series (Existing)
**Status:** Leave 100% as-is. Software remaps only.

## Part Numbers
*   **Engine Side (Plug):** HDP26-24-47SE (Socket Contacts)
*   **Chassis Side (Receptacle):** HDP24-24-47PE (Pin Contacts)
*   **Backshell:** 2428-003-2405 (Straight) or 2428-004-2405 (90 Degree)

## Pin Assignment Strategy
*   **Legacy Compatibility:** Optimized to keep **Oil Temp, Oil Press, and Flex Fuel** on their original pins.
*   **Power Correction:** Pins 1-5 are **Size 16** (High Current) for Coils, DBW, Inj Power.
*   **Transmission:** Trans signals (Temp, Rev Sw, Lockout) removed to separate connector.
*   **Grounds:** Sensor grounds (Crank/Cam) spliced to Pin 40 inside harness to save pins.

| Pin | Size | Function | Description | Wire Gauge | Match to Old Plan? |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | 16 | **HBO 5** | DBW Motor + | 18 AWG | **Yes** (Remapped) |
| **2** | 16 | ~~HCO 1~~ | ~~Coil Power~~ | - | **ORPHAN** (Coil power from PDM) |
| **3** | 16 | ~~HBO 1~~ | ~~Starter~~ | - | **ORPHAN** (Starter from PDM) |
| **4** | 16 | **HBO 4** | DBW Motor - | 18 AWG | **Yes** (Remapped) |
| **5** | 16 | **HBO 6** | Injector & VVT Power (+12V) | 14 AWG | **Yes** (Remapped) |
| **6** | 20 | ~~HBO 3~~ | ~~VVT Bank 2 Exh~~ | - | **ORPHAN** (VVT B2 Exh on Aux) |
| **7** | 20 | **IGN 3** | Cyl 3 Coil Trigger | 20 AWG | **Yes** |
| **8** | 20 | **IGN 4** | Cyl 4 Coil Trigger | 20 AWG | **Yes** |
| **9** | 20 | **IGN 2** | Cyl 2 Coil Trigger | 20 AWG | **Yes** |
| **10** | 20 | **AVI 9** | ECT Sensor | 22 AWG | **Yes** |
| **11** | 20 | **AVI 6** | TPS 2 Signal | 22 AWG | **Yes** |
| **12** | 20 | **INJ 1** | Cyl 1 Injector | 20 AWG | **Yes** |
| **13** | 20 | **INJ 2** | Cyl 2 Injector | 20 AWG | **Yes** |
| **14** | 20 | **DPO 4** | VVT Bank 1 Intake | 20 AWG | **Yes** |
| **15** | 20 | **DPO 6** | VVT Bank 2 Intake | 20 AWG | **Yes** |
| **16** | 20 | **DPO 5** | VVT Bank 1 Exhaust | 20 AWG | **Yes** |
| **17** | 20 | **DPO 3** | Alternator Control | 20 AWG | **Yes** |
| **18** | 20 | **AVI 10** | Fuel Pressure | 22 AWG | **Yes** |
| **19** | 20 | **IGN 1** | Cyl 1 Coil Trigger | 20 AWG | **Yes** |
| **20** | 20 | ~~SPI 4~~ | ~~Trans Neutral~~ | - | **ORPHAN** (Cam 4 moved to Aux) |
| **21** | 20 | ~~AVI 11~~ | ~~Trans Temp~~ | - | **ORPHAN** (IGN 6 moved to Aux) |
| **22** | 20 | ~~HBO 2~~ | ~~DBW Motor -~~ | - | **ORPHAN** (DBW on Pins 1/4) |
| **23** | 20 | ~~SPI 5~~ | ~~Trans Temp~~ | - | **ORPHAN** (Unused) |
| **24** | 20 | **AVI 3** | IAT Sensor | 22 AWG | **Yes** |
| **25** | 20 | **Knock 1** | Knock Bank 1 | 22 AWG (Shielded) | **Yes** |
| **26** | 20 | **+5V** | Sensor 5V Reference | 20 AWG | **Yes** |
| **27** | 20 | **INJ 6** | Cyl 6 Injector | 20 AWG | *New* |
| **28** | 20 | **WB1 Ip** | Wideband Pump Current | 20 AWG | **Yes** |
| **29** | 20 | **WB1 H-** | Wideband Heater - | 20 AWG | *Changed (Was Pump)* |
| **30** | 20 | **WB1 H+** | Wideband Heater + | 20 AWG | *Changed (Was Nernst)* |
| **31** | 20 | **AVI 2** | Oil Temp | 22 AWG | **Yes** |
| **32** | 20 | ~~SPI 2~~ | ~~Oil Pressure~~ | - | **ORPHAN** (Cam 3 moved to Aux) |
| **33** | 20 | **AVI 4** | Oil Pressure (Stock) | 22 AWG | **Yes** (Remapped from Spare) |
| **34** | 20 | - | - | - | **ORPHAN** (Knock 2 on Aux) |
| **35** | 20 | ~~HBO 1~~ | ~~DBW Motor +~~ | - | **ORPHAN** (DBW on Pins 1/4) |
| **36** | 20 | **IGN 5** | Cyl 5 Coil Trigger | 20 AWG | **Yes** (Remapped from Rev Sw) |
| **37** | 20 | **Trigger +** | Crank Position Signal | 22 AWG (Shielded) | **Yes** |
| **38** | 20 | **Home +** | Cam 1 Signal | 22 AWG (Shielded) | **Yes** |
| **39** | 20 | **SPI 1** | Cam 2 Signal | 22 AWG (Shielded) | **Yes** |
| **40** | 20 | **Sig Gnd** | Signal Ground | 20 AWG | **Yes** |
| **41** | 20 | **AVI 5** | TPS 1 Signal | 22 AWG | **Yes** |
| **42** | 20 | **Spare** | Spare Output | 20 AWG | *New* |
| **43** | 20 | **WB1 Vs** | Wideband Sense | 20 AWG | *Changed (Was Htr-)* |
| **44** | 20 | **WB1 Vs/Ip**| Wideband Common | 20 AWG | *Changed (Was Cal)* |
| **45** | 20 | **WB1 Rcal** | Wideband Cal Resistor | 20 AWG | *Changed (Was Htr+)* |
| **46** | 20 | **AVI 1** | MAP Sensor | 22 AWG | **Yes** |
| **47** | 20 | **SPI 3** | Flex Fuel | 22 AWG | **Yes** (No Change) |

## Notes
1.  **Wideband:** Pins 28-30, 43-45 stay connected.
2.  **Orphaned Pins:** 2, 3, 6, 20, 21, 22, 23, 32, 34, 35 are left empty (signals on Aux or PDM).
3.  **Grounds:** Crank/Cam 1/2 grounds splice to Pin 40 inside harness.

## Software Remaps (Main Connector)
| Pin | ECU Pin | Old Function | New Function |
| :--- | :--- | :--- | :--- |
| 1 | HBO 5 | Harness +12V | DBW Motor + |
| 4 | HBO 4 | IGN Power | DBW Motor - |
| 5 | HBO 6 | INJ Power | Inj & VVT Power (No change) |
| 33 | AVI 4 | Spare 2 | Oil Pressure (Stock) |
| 36 | IGN 5 | Reverse Switch | Cyl 5 Coil |
| 47 | SPI 3 | Flex Fuel | Flex Fuel (No change) |

---

# CONNECTOR 2: Auxiliary (NEW - V6 Additions)
**Connector Type:** Deutsch DTM 12-Pin
**Purpose:** All new signals for V6 conversion + shielded cables.

## Part Numbers
*   **Engine Side (Plug):** DTM06-12SA
*   **Chassis Side (Receptacle):** DTM04-12PA
*   **Contacts:** DTM Series Size 20 (0462-201-20141 / 0460-202-20141)
*   **Backshell/Boot:** Optional (no boot = easy service)

## Aux Connector Pinout
| Pin | ECU Pin | Function | Description | Wire Gauge |
| :--- | :--- | :--- | :--- | :--- |
| **1** | INJ 5 | Cyl 5 Injector | Injector Bank 2 | 20 AWG |
| **2** | INJ 6 | Cyl 6 Injector | Injector Bank 2 | 20 AWG |
| **3** | IGN 6 | Cyl 6 Coil | Ignition Bank 2 | 20 AWG |
| **4** | IGN 8 | VVT Bank 2 Exh | Low Side PWM Solenoid | 20 AWG |
| **5** | Knock 2 | Knock Bank 2 | Shielded Signal | 22 AWG Shielded |
| **6** | SPI 2 | Cam 3 (B2 Int) | Shielded Signal | 22 AWG Shielded |
| **7** | SPI 4 | Cam 4 (B2 Exh) | Shielded Signal | 22 AWG Shielded |
| **8** | Sig Gnd | Signal Ground | Cam 3/4, Knock 2 | 20 AWG |
| **9** | Shield | Shield Drain | All Shields | 22 AWG |
| **10** | +5V | Sensor 5V | Cam 3/4 Power | 20 AWG |
| **11** | Spare | Spare | Future Use | - |
| **12** | Spare | Spare | Future Use | - |

## Power Distribution (PDM)
**Coil Power:** Haltech PDM channel, triggered by HCO 1.
*   PDM output: 12 AWG fused, routed through firewall.
*   Splices to all 6 coil +12V leads at engine.
*   Benefits: Current monitoring, soft-start, short circuit protection.

**Starter:** PDM channel (if available) or relay triggered by HBO 1.

