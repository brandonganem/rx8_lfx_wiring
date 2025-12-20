# GM LFX 3.6L V6 Sensor Research

## 1. Oil Pressure Sensor
*   **Status:** Built-in.
*   **Part Number:** AC Delco 12621234 (Alternate: 12673134).
*   **Type:** 3-Wire Linear Pressure Sensor (0-5V).
*   **Connector:** 3-pin GT150 or similar GM connector.
*   **Pinout (Typical GM 3-wire):**
    *   **Pin 2 (or B):** Low Reference (Signal Ground) - *Usually Black wire on pigtail*
    *   **Pin 3 (or A):** 5V Reference - *Usually Grey wire on pigtail*
    *   **Pin 1 (or C):** Signal (0-5V) - *Usually Green or Blue wire on pigtail*
    *   *Note:* Verify with pigtail wire colors if available.
*   **Haltech Configuration:**
    *   Connect to an AVI (Analog Voltage Input).
    *   Requires 5V Ref and Signal Ground.
    *   Calibration: 0.5V = 0 PSI, 4.5V = 100 PSI (Standard GM Linear calibration, verify with specific part).

## 2. Oil Temperature Sensor
*   **Status:** **Not Built-in.**
*   **Details:** The factory GM ECU calculates Oil Temperature based on Coolant Temp, Run Time, and Load. There is no dedicated physical sensor on the stock LFX engine block for Oil Temp.
*   **Recommendation:** Install an aftermarket fluid temperature sensor.
    *   **Location:** Oil cooler sandwich plate, remote oil filter housing, or drill/tap the oil pan.
    *   **Sensor Type:** 2-wire Thermistor (e.g., Haltech 1/8 NPT Fluid Temp Sensor).

## 3. Coolant Temperature (ECT) Sensor
*   **Status:** Built-in.
*   **Part Number:** AC Delco 12608814.
*   **Type:** 2-Wire Thermistor (Resistance based).
*   **Location:** Rear of the engine, driver's side (Bank 2) cylinder head area / water crossover pipe.
*   **Pinout:**
    *   **Pin A:** Signal
    *   **Pin B:** Signal Ground
    *   *Note:* Polarity does not matter for thermistors.
*   **Haltech Configuration:**
    *   Connect to an AVI (Analog Voltage Input) with a Pull-up resistor enabled (standard for Temp sensors).
    *   Calibration: Standard GM Coolant Temp Sensor curve.

## 4. Oil Level Sensor
*   **Status:** Built-in (on some oil pans, typically Camaro/CTS).
*   **Part Number:** AC Delco 12603781.
*   **Type:** Switch (On/Off).
*   **Location:** Side of the oil pan.
*   **Pinout:**
    *   **Pin A:** Signal (to ECU Digital Input)
    *   **Pin B:** Ground
*   **Haltech Configuration:**
    *   Connect to a SPI (Synchronized Pulsed Input) or DPI (Digital Pulsed Input) configured as a Digital Input.
    *   Logic: Switch closes (continuity to ground) or opens when oil is low.
