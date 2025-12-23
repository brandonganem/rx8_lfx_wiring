# LFX + TR-3160 Haltech Nexus R3 — New Harness Build

## Design Philosophy
- **100% new wiring** — No legacy harness reuse
- **Flying leads for shielded signals** — Crank, Cam, Knock run continuous ECU-to-sensor
- **Single bulkhead connector** for non-shielded signals
- **PDM for all high-current loads** — Coils, injectors, pumps, fans
- **Mil-Spec construction** — DR-25 boots, Raychem splices, proper strain relief

---

# Section 1: ECU Pinout

## Connector A (34 Pin)
| Pin | Function | Description | Wire | Color |
|:----|:---------|:------------|:-----|:------|
| A01 | INJ 1 | Cylinder 1 Injector | 20 AWG | Blue/Red |
| A02 | INJ 2 | Cylinder 2 Injector | 20 AWG | Blue/Yellow |
| A03 | INJ 3 | Cylinder 3 Injector | 20 AWG | Blue/Green |
| A04 | INJ 4 | Cylinder 4 Injector | 20 AWG | Blue/Orange |
| A05 | INJ 5 | Cylinder 5 Injector | 20 AWG | Blue/Black |
| A06 | INJ 6 | Cylinder 6 Injector | 20 AWG | Blue/White |
| A07 | INJ 7 | Kill Switch Input | 20 AWG | White/Blue |
| A08 | INJ 8 | Spare | 20 AWG | White/Green |
| A09 | DPO 1 | Brake Switch Input | 20 AWG | Violet/Red |
| A10 | GND | Battery Ground | 14 AWG | Black |
| A11 | GND | Battery Ground | 14 AWG | Black |
| A12 | DPO 2 | Clutch Switch Input | 20 AWG | Violet/Blue |
| A13 | IGN SW | Ignition Switch +12V | 20 AWG | Pink |
| A14 | DPO 3 | Alternator Control | 20 AWG | Violet/Green |
| A15 | DPO 4 | VVT Bank 1 Intake | 20 AWG | Violet/Yellow |
| A16 | DPO 5 | VVT Bank 1 Exhaust | 20 AWG | Violet/Orange |
| A17 | DPO 6 | VVT Bank 2 Intake | 20 AWG | Violet/White |
| A18 | HBO 5 | Starter Relay Trigger | 18 AWG | Gray/Red |
| A19 | HBO 1 | DBW Motor + | 18 AWG | Orange/Red |
| A20 | HBO 2 | DBW Motor - | 18 AWG | Orange/Blue |
| A21 | HBO 3 | Spare (High Current) | 18 AWG | Gray/Yellow |
| A22 | HBO 4 | Spare (High Current) | 18 AWG | Gray/Green |
| A23 | CAN 1 H | Vehicle CAN High | 22 AWG Twist | Yellow |
| A24 | CAN 1 L | Vehicle CAN Low | 22 AWG Twist | Green |
| A25 | HBO 6 | Spare (High Current) | 18 AWG | Gray/Black |
| A26 | +12V | 12V Low Current Out | 20 AWG | Red/White |
| A27 | IGN 1 | Cylinder 1 Coil | 20 AWG | Yellow/Red |
| A28 | IGN 2 | Cylinder 2 Coil | 20 AWG | Yellow/Yellow |
| A29 | IGN 3 | Cylinder 3 Coil | 20 AWG | Yellow/Green |
| A30 | IGN 4 | Cylinder 4 Coil | 20 AWG | Yellow/Orange |
| A31 | IGN 5 | Cylinder 5 Coil | 20 AWG | Yellow/Black |
| A32 | IGN 6 | Cylinder 6 Coil | 20 AWG | Yellow/White |
| A33 | IGN 7 | Reverse Switch Input | 20 AWG | Yellow/Blue |
| A34 | IGN 8 | VVT Bank 2 Exhaust | 20 AWG | Yellow/Purple |

## Connector C (34 Pin)
| Pin | Function | Description | Wire | Color |
|:----|:---------|:------------|:-----|:------|
| C01 | Trigger + | Crank Signal | **Flying Lead** | — |
| C02 | Trigger - | Crank Ground | **Flying Lead** | — |
| C03 | Home + | Cam 1 Signal (B1 Int) | **Flying Lead** | — |
| C04 | Home - | Cam Ground | **Flying Lead** | — |
| C05 | SPI 1 | Cam 2 Signal (B1 Exh) | **Flying Lead** | — |
| C06 | SPI 2 | Cam 3 Signal (B2 Int) | **Flying Lead** | — |
| C07 | SPI 3 | Cam 4 Signal (B2 Exh) | **Flying Lead** | — |
| C08 | SPI 4 | Flex Fuel | 22 AWG | White/Yellow |
| C09 | +8V | Unused | — | Cap |
| C10 | AVI 1 | MAP Sensor | 22 AWG | Orange/White |
| C11 | AVI 2 | Oil Temp | 22 AWG | Orange/Black |
| C12 | AVI 3 | IAT Sensor | 22 AWG | Orange/Red |
| C13 | AVI 4 | Oil Pressure | 22 AWG | Orange/Blue |
| C14 | AVI 5 | TPS 1 Signal | 22 AWG | Orange/Green |
| C15 | AVI 6 | TPS 2 Signal | 22 AWG | Orange/Yellow |
| C16 | AVI 7 | Pedal Position 1 | 22 AWG | Orange/Purple |
| C17 | AVI 8 | Pedal Position 2 | 22 AWG | Orange/Gray |
| C18 | AVI 9 | ECT Sensor | 22 AWG | Orange/Brown |
| C19 | SPI 5 | Coolant Pressure | 22 AWG | White/Orange |
| C20 | SPI 6 | Spare | 22 AWG | White/Purple |
| C21 | CAN 2 H | Haltech CAN High | 22 AWG Twist | White |
| C22 | CAN 2 L | Haltech CAN Low | 22 AWG Twist | Blue |
| C23 | Knock 1 | Knock Bank 1 | **Flying Lead** | — |
| C24 | Knock 2 | Knock Bank 2 | **Flying Lead** | — |
| C25 | +5V | Sensor 5V Reference | 20 AWG | Orange |
| C26 | Sig Gnd | Sensor Signal Ground | 20 AWG | Black/White |
| C27 | AVI 10 | Fuel Pressure | 22 AWG | Green/Red |
| C28 | AVI 11 | Trans Temp | 22 AWG | Green/Blue |
| C29 | WB1 H+ | Wideband Heater + | Haltech Cable | Red |
| C30 | WB1 Ip | Wideband Pump | Haltech Cable | White |
| C31 | WB1 Vs | Wideband Sense | Haltech Cable | Black |
| C32 | WB1 Vs/Ip | Wideband Common | Haltech Cable | Gray |
| C33 | WB1 H- | Wideband Heater - | Haltech Cable | Yellow |
| C34 | WB1 Rcal | Wideband Cal | Haltech Cable | Green |

## Connector E (4 Pin - High Current)
| Pin | Function | Description | Wire | Color |
|:----|:---------|:------------|:-----|:------|
| E01 | HCO 1 | PDM Trigger - Coils | 20 AWG | Red/Blue |
| E02 | HCO 2 | PDM Trigger - Fans | 20 AWG | Red/Green |
| E03 | HCO 3 | PDM Trigger - Injectors | 20 AWG | Red/Yellow |
| E04 | HCO 4 | PDM Trigger - Fuel Pump | 20 AWG | Red/Orange |

---

# Section 2: Shielded Flying Leads

**Strategy:** All position sensors run as continuous shielded cables from ECU to sensor. No bulkhead break. Shields grounded at ECU only.

## Shielded Cable Runs
| Sensor | ECU Pins | Cable Type | Length | Shield Ground |
|:-------|:---------|:-----------|:-------|:--------------|
| Crank | C01, C02 | 2-core shielded | 8 ft | ECU Sig Gnd (C26) |
| Cam 1 (B1 Int) | C03, C04 | 2-core shielded | 6 ft | ECU Sig Gnd (C26) |
| Cam 2 (B1 Exh) | C05, C04 | 2-core shielded | 6 ft | ECU Sig Gnd (C26) |
| Cam 3 (B2 Int) | C06, C04 | 2-core shielded | 7 ft | ECU Sig Gnd (C26) |
| Cam 4 (B2 Exh) | C07, C04 | 2-core shielded | 7 ft | ECU Sig Gnd (C26) |
| Knock 1 | C23 | 1-core shielded | 6 ft | ECU Sig Gnd (C26) |
| Knock 2 | C24 | 1-core shielded | 7 ft | ECU Sig Gnd (C26) |

## Firewall Routing
- **Grommet:** Separate sealed grommet for shielded bundle
- **Protection:** Braided loom from firewall to sensor junction
- **Splices:** None — continuous runs only

---

# Section 3: Bulkhead Connector

**Purpose:** Pass all non-shielded signals through firewall via single disconnect point.

## Connector Selection
| Option | Part Number | Pins | Notes |
|:-------|:------------|:-----|:------|
| Deutsch HDP20 | HDP24-24-31PE / HDP26-24-31SE | 31 | Industrial, affordable |
| Deutsch HD30 | HD34-24-31PE / HD36-24-31SE | 31 | Compact, good sealing |
| Autosport AS | AS616-35S | 35 | Mil-spec, expensive |

**Recommendation:** Deutsch HD30-31 — compact, sealed, easy to source.

## Bulkhead Pinout (31 Pins)
| Pin | Size | ECU Pin | Function | Wire |
|:----|:-----|:--------|:---------|:-----|
| 1 | 16 | HBO 1 | DBW Motor + | 18 AWG |
| 2 | 16 | HBO 2 | DBW Motor - | 18 AWG |
| 3 | 16 | PDM | Coil Power (+12V) | 12 AWG |
| 4 | 16 | PDM | Injector Power (+12V) | 14 AWG |
| 5 | 16 | PDM | VVT Power (+12V) | 16 AWG |
| 6 | 20 | INJ 1 | Cyl 1 Injector | 20 AWG |
| 7 | 20 | INJ 2 | Cyl 2 Injector | 20 AWG |
| 8 | 20 | INJ 3 | Cyl 3 Injector | 20 AWG |
| 9 | 20 | INJ 4 | Cyl 4 Injector | 20 AWG |
| 10 | 20 | INJ 5 | Cyl 5 Injector | 20 AWG |
| 11 | 20 | INJ 6 | Cyl 6 Injector | 20 AWG |
| 12 | 20 | IGN 1 | Cyl 1 Coil | 20 AWG |
| 13 | 20 | IGN 2 | Cyl 2 Coil | 20 AWG |
| 14 | 20 | IGN 3 | Cyl 3 Coil | 20 AWG |
| 15 | 20 | IGN 4 | Cyl 4 Coil | 20 AWG |
| 16 | 20 | IGN 5 | Cyl 5 Coil | 20 AWG |
| 17 | 20 | IGN 6 | Cyl 6 Coil | 20 AWG |
| 18 | 20 | DPO 4 | VVT B1 Intake | 20 AWG |
| 19 | 20 | DPO 5 | VVT B1 Exhaust | 20 AWG |
| 20 | 20 | DPO 6 | VVT B2 Intake | 20 AWG |
| 21 | 20 | IGN 8 | VVT B2 Exhaust | 20 AWG |
| 22 | 20 | DPO 3 | Alternator Control | 20 AWG |
| 23 | 20 | AVI 5 | TPS 1 | 22 AWG |
| 24 | 20 | AVI 6 | TPS 2 | 22 AWG |
| 25 | 20 | AVI 9 | ECT | 22 AWG |
| 26 | 20 | AVI 3 | IAT | 22 AWG |
| 27 | 20 | AVI 10 | Fuel Pressure | 22 AWG |
| 28 | 20 | +5V | Sensor 5V | 20 AWG |
| 29 | 20 | Sig Gnd | Signal Ground | 20 AWG |
| 30 | 20 | SPI 4 | Flex Fuel | 22 AWG |
| 31 | 20 | AVI 1 | MAP Sensor | 22 AWG |

## What's NOT in Bulkhead
| Signal | Reason |
|:-------|:-------|
| Crank/Cam/Knock | Flying leads (shielded) |
| Wideband | Haltech integrated cable |
| Oil Temp/Pressure | Routed to cabin gauge/ECU |
| Trans Temp | Routed from trans tunnel |
| Pedal Position | Stays in cabin |
| CAN Bus | Stays in cabin |
| Brake/Clutch Switch | Stays in cabin |

---

# Section 4: Engine Harness

## Harness Sections
```
ECU ─┬─► Cabin Harness (Pedals, Switches, CAN, Gauges)
     │
     ├─► Shielded Bundle ─► Firewall Grommet ─► Crank/Cam/Knock
     │
     └─► Bulkhead Connector ─► Engine Harness ─┬─► Injector Sub
                                               ├─► Coil Sub
                                               ├─► VVT Sub
                                               ├─► Throttle Body
                                               └─► Sensors
```

## Engine Sub-Harnesses

### Injector Sub-Harness
| Wire | From | To | Splice |
|:-----|:-----|:---|:-------|
| INJ 1 | Bulkhead 6 | Cyl 1 Injector | — |
| INJ 2 | Bulkhead 7 | Cyl 2 Injector | — |
| INJ 3 | Bulkhead 8 | Cyl 3 Injector | — |
| INJ 4 | Bulkhead 9 | Cyl 4 Injector | — |
| INJ 5 | Bulkhead 10 | Cyl 5 Injector | — |
| INJ 6 | Bulkhead 11 | Cyl 6 Injector | — |
| +12V | Bulkhead 4 | All 6 Injectors | 6-way splice |
| Ground | Engine Block | All 6 Injectors | 6-way splice |

### Coil Sub-Harness
| Wire | From | To | Splice |
|:-----|:-----|:---|:-------|
| IGN 1 | Bulkhead 12 | Cyl 1 Coil | — |
| IGN 2 | Bulkhead 13 | Cyl 2 Coil | — |
| IGN 3 | Bulkhead 14 | Cyl 3 Coil | — |
| IGN 4 | Bulkhead 15 | Cyl 4 Coil | — |
| IGN 5 | Bulkhead 16 | Cyl 5 Coil | — |
| IGN 6 | Bulkhead 17 | Cyl 6 Coil | — |
| +12V | Bulkhead 3 | All 6 Coils | 6-way splice |
| Ground | Engine Block | All 6 Coils | 6-way splice |

### VVT Sub-Harness
| Wire | From | To |
|:-----|:-----|:---|
| DPO 4 | Bulkhead 18 | VVT Solenoid B1 Int |
| DPO 5 | Bulkhead 19 | VVT Solenoid B1 Exh |
| DPO 6 | Bulkhead 20 | VVT Solenoid B2 Int |
| IGN 8 | Bulkhead 21 | VVT Solenoid B2 Exh |
| +12V | Bulkhead 5 | All 4 VVT | 4-way splice |

### Throttle Body
| Wire | From | To |
|:-----|:-----|:---|
| DBW + | Bulkhead 1 | TB Motor + |
| DBW - | Bulkhead 2 | TB Motor - |
| TPS 1 | Bulkhead 23 | TB TPS 1 |
| TPS 2 | Bulkhead 24 | TB TPS 2 |
| +5V | Bulkhead 28 | TB 5V |
| Sig Gnd | Bulkhead 29 | TB Ground |

---

# Section 5: Power Distribution (PDM)

## PDM Channel Assignments
| Channel | Load | Fuse | Trigger |
|:--------|:-----|:-----|:--------|
| 1 | Coil Power | 15A | HCO 1 |
| 2 | Injector Power | 10A | HCO 3 |
| 3 | VVT Power | 7.5A | Always On (IGN) |
| 4 | Fuel Pump | 15A | HCO 4 |
| 5 | Cooling Fan 1 | 30A | HCO 2 |
| 6 | Cooling Fan 2 | 30A | CAN Trigger |
| 7 | DBW Throttle | 10A | Always On (IGN) |
| 8 | Starter | 40A | HBO 5 |

## Benefits of PDM
- Current monitoring per channel
- Soft-start (reduces inrush)
- Short circuit protection with auto-retry
- Logging for diagnostics
- No fuse box or relays needed

---

# Section 6: Wire Bill of Materials

## TXL Wire (WireBarn)
| Gauge | Color | Length | Purpose |
|:------|:------|:-------|:--------|
| 14 AWG | Black | 10 ft | Ground |
| 14 AWG | Red | 5 ft | Injector Power |
| 12 AWG | Red | 5 ft | Coil Power |
| 18 AWG | Orange/Red | 15 ft | DBW + |
| 18 AWG | Orange/Blue | 15 ft | DBW - |
| 20 AWG | Blue/Red | 8 ft | INJ 1 |
| 20 AWG | Blue/Yellow | 8 ft | INJ 2 |
| 20 AWG | Blue/Green | 8 ft | INJ 3 |
| 20 AWG | Blue/Orange | 8 ft | INJ 4 |
| 20 AWG | Blue/Black | 8 ft | INJ 5 |
| 20 AWG | Blue/White | 8 ft | INJ 6 |
| 20 AWG | Yellow/Red | 8 ft | IGN 1 |
| 20 AWG | Yellow/Yellow | 8 ft | IGN 2 |
| 20 AWG | Yellow/Green | 8 ft | IGN 3 |
| 20 AWG | Yellow/Orange | 8 ft | IGN 4 |
| 20 AWG | Yellow/Black | 8 ft | IGN 5 |
| 20 AWG | Yellow/White | 8 ft | IGN 6 |
| 20 AWG | Violet/Yellow | 8 ft | VVT B1 Int |
| 20 AWG | Violet/Orange | 8 ft | VVT B1 Exh |
| 20 AWG | Violet/White | 8 ft | VVT B2 Int |
| 20 AWG | Yellow/Purple | 8 ft | VVT B2 Exh |
| 22 AWG | Orange (Various) | 50 ft | Sensors |

## Shielded Cable
| Type | Length | Purpose |
|:-----|:-------|:--------|
| 2-core 22 AWG shielded | 40 ft | Crank + 4x Cam |
| 1-core 22 AWG shielded | 15 ft | 2x Knock |

## Connectors
| Part | Qty | Purpose |
|:-----|:----|:--------|
| Deutsch HD34-24-31PE | 1 | Bulkhead Receptacle |
| Deutsch HD36-24-31SE | 1 | Bulkhead Plug |
| HD30 Size 16 Pins | 5 | High current |
| HD30 Size 20 Pins | 52 | Signals |
| HD30 Backshell | 2 | Strain relief |
| GM Injector Pigtails | 6 | Engine side |
| GM Coil Pigtails | 6 | Engine side |
| GM VVT Pigtails | 4 | Engine side |
| GM Throttle Body Pigtail | 1 | Engine side |
| GM Sensor Pigtails | Various | Engine side |

## Supplies
| Item | Qty |
|:-----|:----|
| DR-25 Heat Shrink (various) | 1 kit |
| Raychem Solder Splices | 50 |
| Split Loom (1/2") | 20 ft |
| Braided Sleeving (1/4") | 30 ft |
| Tesa Tape | 3 rolls |
| Firewall Grommet (1") | 2 |

---

# Section 7: Build Order

1. **ECU Bench Harness**
   - Pin all ECU connectors
   - Test continuity on bench

2. **Shielded Bundle**
   - Cut shielded cables to length
   - Terminate ECU ends
   - Leave engine ends long

3. **Bulkhead to Engine**
   - Build bulkhead pigtail (cabin side)
   - Build engine main trunk
   - Add sub-harness branches

4. **Cabin Harness**
   - Pedal, switches, CAN
   - Oil/trans sensors if routed to cabin

5. **Final Assembly**
   - Join sections
   - Install in car
   - Test each circuit before starting

---

# Section 8: Testing Checklist

## Before Install
- [ ] Continuity: Every ECU pin to destination
- [ ] No shorts: Pin-to-pin isolation
- [ ] Shield isolation: Shields only grounded at ECU

## After Install
- [ ] Key on: 5V reference present
- [ ] Crank signal during cranking
- [ ] Injector pulse with noid lights
- [ ] Coil spark with inline tester
- [ ] VVT solenoid click test

## First Start
- [ ] Oil pressure within 5 seconds
- [ ] No CEL codes
- [ ] All 6 cylinders firing
- [ ] Wideband reading correctly
