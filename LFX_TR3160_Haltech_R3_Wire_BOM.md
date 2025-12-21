# Bill of Materials: TXL Automotive Wire
**Source:** [WireBarn.com](https://www.wirebarn.com/TXL-Automotive-Wire--STRIPED-and-SOLID-colors_c_1813.html)

This BOM is based on the **Haltech Nexus R3 Pinout** we designed. It focuses on the **NEW** wires you need to add or replace.

> **Note:** WireBarn sells wire in spools (typically 10ft, 25ft, 50ft, 100ft). For a single car harness, **25ft spools** are usually the sweet spot. You will have leftovers, which is good for mistakes or future repairs.

## 1. Shielded Cable (Critical)
*WireBarn typically sells primary wire. For Crank, Cam, and Knock sensors, you need **Shielded Multi-Core Cable** to prevent interference.*
*   **Item:** 2-Core Shielded Cable (22 AWG)
    *   **Qty:** ~20 ft
    *   **Use:** Knock Sensors (x2), Crank Sensor (if VR), Cam Sensors (if VR).
*   **Item:** 3-Core Shielded Cable (22 AWG)
    *   **Qty:** ~30 ft
    *   **Use:** Hall Effect Cam Sensors (x4), Crank Sensor (if Hall).
*   **Source:** If WireBarn does not stock "Shielded TEFZEL" or "Shielded TXL", source this from **ProwireUSA**, **MilSpecWiring**, or **Haltech** directly.

---

## 2. Primary Wire (TXL) - By Gauge

### 12 AWG (High Current Power)
*Used for Main Power Feeds (Coils, Fan, Fuel Pump).*
| Color | Qty (Spool) | Circuit |
| :--- | :--- | :--- |
| **Red** | 25 ft | Main Power Feeds (HCO 1, 2, 4) |
| **Black** | 25 ft | Main Grounds (Fan, Pump) |

### 14 AWG (Medium Current Power)
*Used for Injector Power and ECU Ground.*
| Color | Qty (Spool) | Circuit |
| :--- | :--- | :--- |
| **Red / Yellow** | 25 ft | Injector & VVT Power (HCO 3) |
| **Black** | 25 ft | ECU Battery Grounds |

### 18 AWG (Auxiliary Power & Control)
*Used for DBW Motor, Starter Solenoid, and Spare High Current outputs.*
| Color | Qty (Spool) | Circuit |
| :--- | :--- | :--- |
| **Orange / Red** | 25 ft | DBW Motor + |
| **Orange / Blue** | 25 ft | DBW Motor - |
| **Gray / Red** | 25 ft | Starter Relay (High Side) |
| **Gray / Green** | 25 ft | Spare Output (HBO 4) |
| **Gray / Black** | 25 ft | Spare Output (HBO 6) |

### 20 AWG (Injectors, Coils, Solenoids)
*Used for the majority of engine actuators.*
| Color | Qty (Spool) | Circuit |
| :--- | :--- | :--- |
| **Blue / Black** | 25 ft | Injector 5 |
| **Blue / Purple** | 25 ft | Injector 6 |
| **Yellow / Black** | 25 ft | Ignition Coil 5 |
| **Yellow / Purple** | 25 ft | Ignition Coil 6 |
| **Violet / Yellow** | 25 ft | VVT Bank 1 Intake |
| **Violet / Orange** | 25 ft | VVT Bank 1 Exhaust |
| **Violet / White** | 25 ft | VVT Bank 2 Intake |
| **Gray / Yellow** | 25 ft | VVT Bank 2 Exhaust |
| **Yellow / Blue** | 25 ft | Reverse Switch |
| **Yellow / White** | 25 ft | Reverse Lockout |
| **White / Blue** | 25 ft | Kill Switch Input |
| **White / Green** | 25 ft | Spare Switch Input |
| **Red / White** | 25 ft | +12V Low Current Ref |
| **Pink** | 25 ft | Ignition Switched 12V (General) |

### 22 AWG (Sensors & Signals)
*Used for 5V sensors, Temp, Pressure, CAN Bus.*
| Color | Qty (Spool) | Circuit |
| :--- | :--- | :--- |
| **Orange** | 25 ft | +5V Reference (Shared) |
| **Black / White** | 50 ft | Signal Ground (Shared - Buy extra) |
| **White / Purple** | 25 ft | Coolant Pressure |
| **White / Orange** | 25 ft | Combo Oil Pressure |
| **Orange / Black** | 25 ft | Combo Oil Temp |
| **Green / Blue** | 25 ft | Trans Temp |
| **White** | 25 ft | CAN High (Twist with Blue) |
| **Blue** | 25 ft | CAN Low (Twist with White) |

---

## 4. Connectors & Terminals
### Main Engine Disconnect (Bulkhead)
*To make the engine harness serviceable (removable), install this connector between the ECU and the Engine.*
*   **Connector Body (Chassis Side):** Deutsch HDP24-24-47PE (1x)
*   **Connector Body (Engine Side):** Deutsch HDP26-24-47SE (1x)
*   **Contacts (Size 16):** 10x (5 for plug, 5 for receptacle) - For Power/Gnd.
*   **Contacts (Size 20):** 100x (42 for plug, 42 for receptacle + spares) - For Signals.
*   **Backshell:** Deutsch 2428-003-2405 (Straight) or 2428-004-2405 (90 Degree).
*   **Tooling:** Deutsch HDT-48-00 (Crimp Tool) or equivalent.

## 5. Consolidated "Budget" List
*If you don't want to buy 25 different spools of striped wire, you can simplify by buying solid colors and using **Heat Shrink Labels** to identify them.*

**Simplified Shopping List:**
1.  **12 AWG:** Red, Black.
2.  **14 AWG:** Red, Black.
3.  **18 AWG:** Orange, Gray.
4.  **20 AWG:**
    *   **Blue** (Injectors)
    *   **Yellow** (Coils)
    *   **Violet** (VVT)
    *   **White** (Switches)
5.  **22 AWG:**
    *   **Orange** (5V Ref & Temp Sensors)
    *   **Black** (Signal Ground)
    *   **White** (Pressure Sensors & CAN)
    *   **Green** (Aux Sensors)

**Total Spools:** ~13 Spools (vs ~30 for exact matching).
