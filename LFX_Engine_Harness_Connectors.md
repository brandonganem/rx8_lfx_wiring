# GM LFX Engine Harness Connector Spec (2010-2015 Camaro V6)

This document outlines the connectors required to build a custom engine harness for the GM LFX 3.6L V6, specifically tailored for a Port Injection retrofit application.

## 1. Ignition System
### Ignition Coils (x6)
*   **Component:** GM D510C / D585 Style Coils (LFX Stock)
*   **Connector Series:** **Delphi / Aptiv GT 150**
*   **Gender:** Female (Harness Side)
*   **Pin Count:** 4
*   **Part Numbers (Typical):**
    *   Connector: 13585860 or equivalent
    *   Terminals: GT 150 Series
*   **Pinout:**
    *   A: Ground (Cylinder Head)
    *   B: Reference Low (Signal Ground)
    *   C: Ignition Trigger (5V Logic)
    *   D: +12V Ignition Power

## 2. Fuel System (Port Injection Retrofit)
*   **Component:** Port Fuel Injectors (x6)
*   **Connector Series:** **USCAR / EV6** (Most common for modern retrofits)
*   **Gender:** Female (Harness Side)
*   **Pin Count:** 2
*   **Notes:**
    *   Stock LFX uses Direct Injection (DI) injectors which are NOT used in this retrofit.
    *   If using older style injectors, they may be **EV1 / Jetronic**. Check your specific injectors.
    *   **USCAR/EV6** is the standard for LS3/LS7 and most modern aftermarket injectors.

## 3. Camshaft & Crankshaft Position
### Camshaft Position Sensors (x4)
*   **Location:** Rear of cylinder heads (2 per bank)
*   **Connector Series:** **Bosch Compact 1.1a** (3-Way) or **Delphi GT 150** (Verify on specific sensor)
    *   *Note:* Many GM High Feature engines use the Bosch 3-pin connector for cam sensors.
*   **Pin Count:** 3
*   **Pinout:**
    *   1: +5V Reference
    *   2: Signal Ground
    *   3: Signal Output

### Crankshaft Position Sensor (x1)
*   **Location:** Side of block
*   **Connector Series:** **Bosch Compact 1.1a** (3-Way)
*   **Pin Count:** 3
*   **Pinout:**
    *   1: +5V Reference
    *   2: Signal Ground
    *   3: Signal Output (58X)

## 4. Variable Valve Timing (VVT)
### VVT Solenoids / Actuators (x4)
*   **Location:** Front of cylinder heads (2 per bank)
*   **Connector Series:** **Delphi Metri-Pack 150.2** (Pull-to-Seat) or **GT 150**
*   **Pin Count:** 2
*   **Notes:** These are often the black, 2-pin sealed connectors.
*   **Pinout:**
    *   A: Low Side Control (ECU)
    *   B: +12V Switched Power

## 5. Air & Throttle
### Electronic Throttle Body (DBW)
*   **Connector Series:** **Delphi GT 150**
*   **Pin Count:** 6
*   **Part Numbers (Typical):**
    *   Connector: 13503396
*   **Pinout:**
    *   A: Motor +
    *   B: Motor -
    *   C: Signal Ground
    *   D: TPS 1 Signal
    *   E: +5V Reference
    *   F: TPS 2 Signal

### Manifold Absolute Pressure (MAP)
*   **Location:** Top of Intake Manifold
*   **Connector Series:** **Bosch Compact 1.1a** (3-Way)
*   **Pin Count:** 3
*   **Pinout:**
    *   1: +5V Reference
    *   2: Signal Ground
    *   3: Signal Output

### Mass Air Flow (MAF) / Intake Air Temp (IAT)
*   **Location:** Intake Tube
*   **Connector Series:** **Delphi GT 150**
*   **Pin Count:** 5
*   **Pinout:**
    *   A: IAT Signal
    *   B: IAT Ground (Low Ref)
    *   C: MAF Power (12V)
    *   D: MAF Ground
    *   E: MAF Signal (Frequency)

## 6. Fluid Sensors
### Coolant Temperature (CLT)
*   **Connector Series:** **Delphi Metri-Pack 150**
*   **Pin Count:** 2
*   **Pinout:**
    *   A: Signal Ground
    *   B: Signal

### Oil Pressure Sensor
*   **Connector Series:** **Delphi GT 150**
*   **Pin Count:** 3
*   **Pinout:**
    *   A: Signal Ground
    *   B: +5V Reference
    *   C: Signal

## 7. Knock Sensors
### Knock Sensors (x2)
*   **Location:** Side of block / Valley
*   **Connector Series:** **Bosch / Tyco** (2-Way)
*   **Pin Count:** 2
*   **Notes:** Often a specific "flat" 2-pin connector.

## 8. Charging & Starting
### Alternator (Generator)
*   **Connector Series:** **Delphi Metri-Pack 150** (2-Way)
*   **Pin Count:** 2
*   **Pinout:**
    *   A: Generator Turn On / Duty Cycle Signal (L-Terminal)
    *   B: Field Duty Cycle Signal (F-Terminal) - *Check specific regulator pinout*

### Starter Solenoid
*   **Connector:** Ring Terminal (M8/M10 stud) + **Metri-Pack 150** (1-Way) or Ring Terminal for signal (depending on starter model).
*   **Notes:** LFX starters often use a simple nut for the signal wire, or a single pin Metri-Pack connector.

## 9. Emissions (Optional)
### EVAP Purge Solenoid
*   **Connector Series:** **Delphi Metri-Pack 150**
*   **Pin Count:** 2
