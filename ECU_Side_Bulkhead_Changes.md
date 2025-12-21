# ECU Side Bulkhead Connector Work Order
**Goal:** Leave the existing 47-pin connector untouched. Add a new 12-pin Aux connector for V6-specific signals.

## Main 47-Pin Connector: NO PHYSICAL CHANGES
*The booted connector stays exactly as it is. Just configure software remaps.*

### Wires to KEEP (All of them!)
Every pin stays where it is. Orphaned pins (20, 21, 22, 23, 32, 34, 35) are simply left unconnected at the ECU side.

---

## New DTM 12-Pin Aux Connector: ADD THIS
*Mount this connector near the main 47-pin. No boot required for easy service.*

### Wires to Run (ECU -> Aux Connector)
| Aux Pin | ECU Pin | Function | Wire Gauge |
| :--- | :--- | :--- | :--- |
| 1 | A05 (INJ 5) | Cyl 5 Injector | 20 AWG |
| 2 | A06 (INJ 6) | Cyl 6 Injector | 20 AWG |
| 3 | A32 (IGN 6) | Cyl 6 Coil Trigger | 20 AWG |
| 4 | C24 (Knock 2) | Knock Bank 2 | 22 AWG Shielded |
| 5 | C06 (SPI 2) | Cam 3 (Bank 2 Int) | 22 AWG Shielded |
| 6 | C08 (SPI 4) | Cam 4 (Bank 2 Exh) | 22 AWG Shielded |
| 7 | C26 (Sig Gnd) | Signal Ground | 20 AWG |
| 8 | A10 (Gnd) | Shield Drain | 22 AWG |
| 9 | C25 (+5V) | Sensor 5V | 20 AWG |
| 10-12 | - | Spare | - |

### Coil Power (HCO 1)
*Do NOT route through either connector. Run directly:*
1.  ECU triggers **HCO 1** relay (A25 or dedicated relay board).
2.  Relay output: 12 AWG fused wire through firewall grommet.
3.  Splice to coil power leads at engine.

---

## Summary Checklist
1.  [ ] **Main 47-Pin:** Do nothing. Leave it alone.
2.  [ ] **Mount Aux Connector:** Install DTM 12-pin near main connector.
3.  [ ] **Run Aux Wires:** INJ 5/6, IGN 6, Knock 2, Cam 3/4, Ground, 5V.
4.  [ ] **Run Coil Power:** 12 AWG from cabin relay through firewall.
5.  [ ] **Software Setup:** Configure remaps:
    - HBO 5 → DBW Motor +
    - HBO 4 → DBW Motor -
    - AVI 4 → Oil Pressure
    - IGN 5 → Ignition Output (Cyl 5)
