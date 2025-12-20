# Wiring Splice & Grounding Plan: GM LFX + Haltech Nexus R3

This document details how to construct the shared power and ground circuits (splices) for your harness. Since the Nexus R3 handles power distribution, we group these by the High Current Output (HCO) assignments from the **Hybrid Pinout**.

## 1. Sensor Power & Ground (5V & Signal Ground)
These are critical for clean sensor data. Do **not** ground high-current devices (coils, solenoids, fans) to these splices.

### **5V Reference Splice (Source: Pin C25)**
*   **Wire Color:** White/Black (Recommended) or Red/White
*   **Splice Location:** Main Trunk near engine firewall
*   **Destinations:**
    1.  **Accelerator Pedal (APP):** Pin for 5V Ref.
    2.  **Throttle Body (TPS):** Pin E (Typical GM).
    3.  **MAP Sensor:** Pin 3 (Typical).
    4.  **Oil Pressure Sensor:** 5V Input.
    5.  **Fuel Pressure Sensor:** 5V Input.
    6.  **Cam Sensor 1 (Bank 1 Intake):** Pin 1 (Reference).
    7.  **Cam Sensor 2 (Bank 1 Exhaust):** Pin 1 (Reference).
    8.  **Cam Sensor 3 (Bank 2 Intake):** Pin 1 (Reference).
    9.  **Cam Sensor 4 (Bank 2 Exhaust):** Pin 1 (Reference).
    *   *Note: Verify your specific Cam Sensors are 5V. Most GM LFX sensors are 5V.*

### **Signal Ground Splice (Source: Pin C26)**
*   **Wire Color:** Black/White (Recommended) or Black
*   **Splice Location:** Main Trunk near engine firewall
*   **Destinations:**
    1.  **Accelerator Pedal (APP):** Pin for Low Ref.
    2.  **Throttle Body (TPS):** Pin C (Typical GM).
    3.  **MAP Sensor:** Pin 1 (Typical).
    4.  **Oil Pressure Sensor:** Ground.
    5.  **Fuel Pressure Sensor:** Ground.
    6.  **IAT Sensor:** Ground pin.
    7.  **ECT Sensor:** Ground pin.
    8.  **Oil Temp Sensor:** Ground pin.
    9.  **Cam Sensors (1-4):** Pin 2 (Low Ref).
    *   *Note: Do NOT connect this splice to the chassis or engine block manually. It grounds internally through the ECU.*

---

## 2. Power Distribution Splices (12V)
Based on the Hybrid Pinout using the Nexus R3 HCOs.

### **Ignition Coil Power Splice (Source: HCO 1 / Pin E01)**
*   **Wire Gauge:** 12-14 AWG from ECU -> Splice -> 18-20 AWG to Coils.
*   **Destinations:**
    1.  **Coil 1:** Pin D (Pink).
    2.  **Coil 2:** Pin D (Pink).
    3.  **Coil 3:** Pin D (Pink).
    4.  **Coil 4:** Pin D (Pink).
    5.  **Coil 5:** Pin D (Pink).
    6.  **Coil 6:** Pin D (Pink).
    *   *Note: LFX Coils often have 4 pins: A(Gnd), B(Ref Low), C(Trigger), D(12V).*

### **Injector & VVT Power Splice (Source: HCO 3 / Pin E03)**
*   **Wire Gauge:** 12-14 AWG from ECU -> Splice -> 18-20 AWG to components.
*   **Destinations:**
    1.  **Injector 1:** 12V Pin (Pink/Black).
    2.  **Injector 2:** 12V Pin.
    3.  **Injector 3:** 12V Pin.
    4.  **Injector 4:** 12V Pin.
    5.  **Injector 5:** 12V Pin.
    6.  **Injector 6:** 12V Pin.
    7.  **VVT Solenoid 1 (B1 Int):** 12V Pin.
    8.  **VVT Solenoid 2 (B1 Exh):** 12V Pin.
    9.  **VVT Solenoid 3 (B2 Int):** 12V Pin.
    10. **VVT Solenoid 4 (B2 Exh):** 12V Pin.
    11. **Reverse Lockout Solenoid:** 12V Pin.
    12. **Flex Fuel Sensor:** 12V Pin (Pink).

### **Fuel Pump (Source: HCO 4 / Pin E04)**
*   **Direct Run:** Run 12 AWG (or larger depending on pump) directly to the Fuel Pump + terminal.

### **Cooling Fan (Source: HCO 2 / Pin E02)**
*   **Direct Run:** Run 10-12 AWG directly to the Fan + terminal.

---

## 3. High Current Grounding (Chassis/Engine)
These grounds do **not** go back to the ECU pins. They must go to the engine block or chassis.

### **Ignition Coil Ground Splice**
*   **Location:** Cylinder Heads (One splice per bank is best).
*   **Destinations:**
    *   **Bank 1 Coils (1, 3, 5):** Pin A (Black). Splice together and bolt to Bank 1 Cylinder Head.
    *   **Bank 2 Coils (2, 4, 6):** Pin A (Black). Splice together and bolt to Bank 2 Cylinder Head.
    *   *Note: Ensure the Cylinder Heads have a heavy ground strap to the Engine Block and Battery Negative.*

### **Coil Reference Ground (Optional but Recommended)**
*   **Pin B on Coils:** This is "Low Reference".
*   **Option A (Best):** Splice together and run to **Signal Ground (C26)**.
*   **Option B (Okay):** Join to the Cylinder Head Ground (Pin A).

### **Accessory Grounds**
*   **Fuel Pump:** Ground locally to clean chassis metal near the tank.
*   **Cooling Fan:** Ground locally to chassis frame rail near the radiator.
*   **ECU Ground:** The Nexus R3 has heavy ground lugs/pins. These must go directly to the **Battery Negative** or the main **Star Ground** point on the engine block. Do not ground the ECU to thin sheet metal.
