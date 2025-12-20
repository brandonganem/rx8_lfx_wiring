# Wiring Plan: GM LFX (Port Injection) + TR-3160 + Haltech Nexus R3

## Project Overview
- **Engine:** GM LFX V6 (3.6L)
- **Induction:** Retrofitted Port Injection (6 Injectors), Direct Injection Removed.
- **Transmission:** Tremec TR-3160 (Manual)
- **ECU:** Haltech Nexus R3 VCU

## Haltech Nexus R3 Capabilities vs Requirements
The Nexus R3 is well-suited for this application.
- **Injectors:** 8 Drivers available (6 used).
- **Ignition:** 8 Drivers available (6 used).
- **VVT:** 4 Cam Control outputs needed (handled by Low Side or Half Bridge outputs).
- **DBW:** 1 Electronic Throttle (handled by Half Bridge outputs).
- **Cam Sensors:** 4 Inputs needed (handled by SPI inputs).

## Wiring Strategy
This plan uses the standard Haltech nomenclature (e.g., `INJ1`, `SPI1`). Refer to the specific "Quick Start Guide" or "Wiring Diagram" included with your Nexus R3 to identify the physical connector and pin number (e.g., Connector A, Pin 10).

### 1. Power Distribution (PDM)
The Nexus R3 has onboard PDM capabilities (HCO - High Current Outputs).
*   **HCO 1 (25A):** Fuel Pump.
*   **HCO 2 (25A):** Cooling Fan.
*   **HCO 3 (25A):** Ignition Coils Power (12V supply to all 6 coils).
*   **HCO 4 (25A):** Injectors + VVT Solenoids Power.

### 2. Ignition System (Coils)
The LFX uses 6 individual coils.
*   **Type:** Logic Level (Smart Coils).
*   **Wiring:**
    *   **12V:** From `HCO 3`.
    *   **Ground:** Cylinder Head / Battery Negative.
    *   **Signal Ground:** Sensor Ground (optional but recommended) or Battery Negative.
    *   **Trigger:** Connect to Haltech `IGN` outputs.

| Cylinder | Haltech Output | LFX Coil Pin (Typical) |
| :--- | :--- | :--- |
| Cyl 1 | `IGN 1` | Pin C (Trigger) |
| Cyl 2 | `IGN 2` | Pin C (Trigger) |
| Cyl 3 | `IGN 3` | Pin C (Trigger) |
| Cyl 4 | `IGN 4` | Pin C (Trigger) |
| Cyl 5 | `IGN 5` | Pin C (Trigger) |
| Cyl 6 | `IGN 6` | Pin C (Trigger) |

### 3. Fuel System (Port Injection Retrofit)
*   **Type:** High Impedance Injectors (Saturation).
*   **Wiring:**
    *   **12V:** From `HCO 4`.
    *   **Trigger:** Connect to Haltech `INJ` outputs (switched ground).

| Cylinder | Haltech Output |
| :--- | :--- |
| Cyl 1 | `INJ 1` |
| Cyl 2 | `INJ 2` |
| Cyl 3 | `INJ 3` |
| Cyl 4 | `INJ 4` |
| Cyl 5 | `INJ 5` |
| Cyl 6 | `INJ 6` |

### 4. Trigger & Cam Sensors (Inputs)
The LFX has 4 Cam sensors and 1 Crank sensor.
*   **Crank Sensor:** 58X Reluctor or Hall (Usually 3-wire Hall on LFX).
*   **Cam Sensors:** 4x Hall Effect (3-wire).

| Sensor | Haltech Input | Notes |
| :--- | :--- | :--- |
| **Crank Position** | `Trigger +` | If Hall: Signal to Trig+, 12V/5V to Power, Gnd to Gnd. |
| **Cam 1 (Bank 1 Intake)** | `SPI 1` | Synchronized Pulsed Input |
| **Cam 2 (Bank 1 Exhaust)**| `SPI 2` | Synchronized Pulsed Input |
| **Cam 3 (Bank 2 Intake)** | `SPI 3` | Synchronized Pulsed Input |
| **Cam 4 (Bank 2 Exhaust)**| `SPI 4` | Synchronized Pulsed Input |

*Note: Ensure Cam sensors are powered by 5V or 12V as per sensor spec (LFX usually 5V reference).*

### 5. Variable Valve Timing (VVT Solenoids)
4 Solenoids control the oil flow to the phasers.
*   **Wiring:** 2-wire. One side to 12V (`HCO 4`), other side to ECU Low Side Output.

| Solenoid | Haltech Output | Function |
| :--- | :--- | :--- |
| **Bank 1 Intake** | `DPO 1` (or `LSO 1`) | PWM Control (Low Side) |
| **Bank 1 Exhaust**| `DPO 2` (or `LSO 2`) | PWM Control (Low Side) |
| **Bank 2 Intake** | `DPO 3` (or `LSO 3`) | PWM Control (Low Side) |
| **Bank 2 Exhaust**| `DPO 4` (or `LSO 4`) | PWM Control (Low Side) |

### 6. Drive By Wire (Electronic Throttle)
*   **Throttle Body:** 6-pin connector.
*   **Pedal:** 6-pin connector (APP).

**Throttle Body:**
| Pin Function | Haltech Connection |
| :--- | :--- |
| Motor + | `HBO 1` (Half Bridge 1) |
| Motor - | `HBO 2` (Half Bridge 2) |
| TPS 1 Signal | `AVI 1` |
| TPS 2 Signal | `AVI 2` |
| 5V Ref | 5V Output |
| Signal Ground | Signal Ground |

**Accelerator Pedal (APP):**
| Pin Function | Haltech Connection |
| :--- | :--- |
| APP 1 Signal | `AVI 3` |
| APP 2 Signal | `AVI 4` |
| 5V Ref | 5V Output |
| Signal Ground | Signal Ground |

### 7. Sensors
| Sensor | Haltech Input | Notes |
| :--- | :--- | :--- |
| **MAP** | Onboard | Run vacuum line to ECU |
| **IAT** (Air Temp) | `AVI 5` | GM IAT usually in MAF or separate |
| **CLT** (Coolant) | `AVI 6` | |
| **Oil Pressure** | `AVI 7` | |
| **Fuel Pressure** | `AVI 8` | Important for safety |
| **Knock 1** (Bank 1) | `Knock 1` | |
| **Knock 2** (Bank 2) | `Knock 2` | |
| **Wideband O2** | Onboard WB1 | Connect LSU 4.9 or NTK sensor directly |

### 8. Transmission (TR-3160)
| Component | Haltech Connection | Notes |
| :--- | :--- | :--- |
| **Reverse Lockout** | `DPO 5` (Low Side) | Solenoid to allow Reverse gear. Active < 5mph. |
| **Reverse Switch** | `AVI 9` (or Digital) | Input to turn on reverse lights/camera. |
| **VSS** (Speed) | `SPI 5` | Vehicle Speed Sensor (VR or Hall). |

### 9. Accessories (Fuel Pump & Fan)
| Component | Haltech Connection | Notes |
| :--- | :--- | :--- |
| **Fuel Pump** | `HCO 1` | Direct 12V power to pump (up to 25A). Ground pump to chassis. |
| **Cooling Fan** | `HCO 2` | Direct 12V power to fan (up to 25A). Ground fan to chassis. |

### 10. Starting System
*   **Starter Relay:** External relay required (HCOs are full).
*   **Trigger:** `HBO 5` (High Side Output - +12V).
*   **Wiring:**
    *   **86 (Coil +):** To Haltech `HBO 5` (A18).
    *   **85 (Coil -):** To Chassis Ground.
    *   **30 (Common):** Battery 12V (High Current).
    *   **87 (NO):** To Starter Solenoid.
*   **Note:** This High Side configuration is safer. If the wire to the relay shorts to ground, the fuse trips rather than the starter cranking unexpectedly.

### 11. Summary of Remaining I/O
*   **Outputs:** `IGN 7-8` (Unused), `INJ 7-8` (Unused), `HBO 6` (Available), `DPO 6` (Available).
*   **Inputs:** `AVI 10-11` (Available), `SPI 6` (Available for Flex Fuel).

## Notes
*   **Grounding:** Ensure the Cylinder Heads and ECU Ground are referenced to the same point (Star Ground on Block/Battery).
*   **Fusing:** The Nexus R3 HCOs act as fuses. Configure trip currents in NSP software.
*   **Configuration:** You will need to configure the "Trigger Type" in NSP. The LFX is a "GM High Feature V6" pattern (usually 58X crank, 4x Cam pattern).
