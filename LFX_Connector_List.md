# GM LFX Engine Harness Connector List
**Engine:** GM LFX V6 (3.6L) 2010-2015 (Camaro, CTS, etc.)

This list details the electrical connectors required to build a harness for the GM LFX engine.

## 1. Ignition System
### Ignition Coils (x6)
*   **Component Part Number:** ACDelco D510C / GM 12611424
*   **Connector Series:** **Delphi GT 150**
*   **Pin Count:** 4-Way
*   **Gender:** Female (Harness Side)
*   **Notes:** Standard GM 4-pin coil connector.
    *   Pin A: Ground
    *   Pin B: Low Reference (Signal Ground)
    *   Pin C: Ignition Control (Trigger)
    *   Pin D: Ignition Voltage (12V)

## 2. Fuel System
### Fuel Injectors (Port Injection Retrofit)
*   **Component:** Standard LS3/LS7 Style Injectors (Typical for retrofits)
*   **Connector Series:** **USCAR / EV6**
*   **Pin Count:** 2-Way
*   **Notes:** Most port injection kits for the LFX (e.g., Overkill) use LS3-style injectors which use the EV6/USCAR connector.
    *   *If using older EV1 injectors:* Jetronic / EV1 connector.
    *   *Stock DI Injectors (Reference only):* Bosch Direct Injection 2-pin (Not used in this build).

### High Pressure Fuel Pump (HPFP)
*   **Component:** Stock LFX HPFP (Hitachi)
*   **Connector Series:** **Sumitomo / Hitachi** 2-Way
*   **Notes:** Usually removed or left unplugged for Port Injection conversions, unless used as a pass-through or idler.

## 3. Position Sensors
### Camshaft Position Sensors (x4)
*   **Component Part Number:** GM 12608424
*   **Connector Series:** **Bosch Compact 1.1a** (3-Way)
*   **Pin Count:** 3-Way
*   **Notes:** Often black or grey.
    *   Pin 1: 5V Reference
    *   Pin 2: Low Reference (Ground)
    *   Pin 3: Signal

### Crankshaft Position Sensor (58x)
*   **Component Part Number:** GM 12616646
*   **Connector Series:** **Bosch Compact 1.1a** (3-Way)
*   **Pin Count:** 3-Way
*   **Notes:** Same series as Cam sensors.
    *   Pin 1: 5V Reference
    *   Pin 2: Low Reference (Ground)
    *   Pin 3: Signal

## 4. Variable Valve Timing (VVT)
### Camshaft Actuators / VVT Solenoids (x4)
*   **Component Part Number:** GM 12636175
*   **Connector Series:** **Delphi Metri-Pack 150**
*   **Pin Count:** 2-Way
*   **Notes:** Sealed connector.
    *   Pin A: Control (Low Side)
    *   Pin B: Ignition Voltage (12V)

## 5. Air & Throttle
### Electronic Throttle Body
*   **Component Part Number:** GM 12616995
*   **Connector Series:** **Delphi GT 150**
*   **Pin Count:** 6-Way
*   **Notes:**
    *   Pin A: Motor +
    *   Pin B: Motor -
    *   Pin C: Low Reference
    *   Pin D: TPS 1 Signal
    *   Pin E: 5V Reference
    *   Pin F: TPS 2 Signal

### Manifold Absolute Pressure (MAP) Sensor
*   **Component Part Number:** GM 12644228
*   **Connector Series:** **Bosch Compact 1.1a** (3-Way)
*   **Pin Count:** 3-Way
*   **Notes:**
    *   Pin 1: 5V Reference
    *   Pin 2: Low Reference
    *   Pin 3: Signal

### Mass Air Flow (MAF) / IAT Sensor
*   **Component Part Number:** GM 23262343 (Card Style)
*   **Connector Series:** **Delphi GT 150**
*   **Pin Count:** 5-Way
*   **Notes:** Combined MAF and IAT.
    *   Pin A: IAT Signal
    *   Pin B: Low Reference
    *   Pin C: MAF Signal
    *   Pin D: Ignition Voltage (12V)
    *   Pin E: Ground

## 6. Fluid Sensors
### Coolant Temperature Sensor (CLT)
*   **Component Part Number:** GM 12608814
*   **Connector Series:** **Delphi Metri-Pack 150**
*   **Pin Count:** 2-Way
*   **Notes:**
    *   Pin A: Low Reference
    *   Pin B: Signal

### Oil Pressure Sensor
*   **Component Part Number:** GM 12621234
*   **Connector Series:** **Delphi GT 150**
*   **Pin Count:** 3-Way
*   **Notes:**
    *   Pin A: Low Reference
    *   Pin B: 5V Reference
    *   Pin C: Signal

## 7. Other
### Knock Sensors (x2)
*   **Component Part Number:** GM 12629635
*   **Connector Series:** **Bosch Compact 1.1a** (2-Way) or **Molex**
*   **Pin Count:** 2-Way
*   **Notes:** Located on the side of the block.

### Alternator / Generator
*   **Component:** Valeo (Typical)
*   **Connector Series:** **Yazaki** or **Metri-Pack 150**
*   **Pin Count:** 2-Way
*   **Notes:** PWM control.

### EVAP Purge Solenoid
*   **Component Part Number:** GM 12610560
*   **Connector Series:** **Delphi Metri-Pack 150**
*   **Pin Count:** 2-Way
