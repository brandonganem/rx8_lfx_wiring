# Haltech Nexus R3 Quick Start Guide

## Nexus R3 Overview

### What is a NEXUS R3 Vehicle Control Unit?
*   A new generation engine management system
*   A power distribution module
*   A data logger
*   A universal wideband controller
*   A high speed Wi-Fi communications module
*   All natively interconnected with each other
*   All programmable with one single piece of software

The NEXUS R3 is one of Haltech’s Vehicle Control Units (VCU) which features additional functionality that extends beyond just engine control. Boasting innovative yet user-friendly technology, it sets a new market standard for engine management and power distribution systems. An ECU, PDM, Wi-Fi module, wideband controller and a data logger all in one.

**NEX-US [noun]**
*   a connection or series of connections linking two or more things.
*   a connected group or series
*   the central or most important point or place

### Optional Accessories (Sold Separately)
*   **Plug and pins set:** AMP 34 pin key 1, AMP 34 pin key 2, DTP 4 pin: `HT-030013`
*   **NEXUS R3 Universal Wiring Harness 2.5m:** `HT-183200`
*   **Glass mount Wi-Fi antenna with 1.5m terminated lead:** `HT-011401`
*   **Wideband Flying Lead Adaptor Harness 400mm:** `HT-010723`
*   **LSU4.9 Wideband Hardware Pack:** Inc sensor, adaptor harness and weld-in bung. `HT-010746`
*   **NTK Wideband Hardware Pack:** Inc sensor, adaptor harness and weld in bung. `HT-010747`
*   **NEXUS R3 Tube Mount Kit:** 1.625” `HT-039067`, 1.25” `HT-039065`
*   **Hydraulic cable lug crimping tool:** `HT-070306`

### What’s in the box?
*   NEXUS R3 VCU
*   SurLok connectors (Red and Black)
*   Wi-Fi Antenna RP-SMA 108mm
*   Mounting bolts
*   USB-C cable
*   USB-C dust cap
*   Reverse mount VCU label
*   Quick start guide
*   Haltech product catalogue

## Nexus R3 LED Behaviour

| LED Colour | Condition |
| :--- | :--- |
| **Power** | |
| Green | Normal operation (on main power or low power mode) |
| Blue | Connect to unit and install firmware |
| Red | Hardware fault |
| **DTC** | |
| None | DTCs not present |
| Yellow | A DTC is present (of any kind, past/present/not severe/severe) |
| **WiFi** | |
| None | Wi-Fi is disabled |
| Green solid | Wi-Fi is enabled |
| Green flashing | Wi-Fi is enabled and connected to NSP |
| **Datalog** | |
| None | Unit is not logging |
| Yellow flashing | Unit is logging, unit is not looping or not full |
| Yellow | Unit is logging, unit is looping or full |
| **HCO (25A)** | |
| None | Channel is off |
| Green | Channel is on - duty cycle is >0% and operating correctly |
| Red | Channel is not allowed to be driven. Usually caused by (but not limited to) an overcurrent this drive cycle |

## Nexus R3 Specifications

### Outputs
*   Ignition: 8
*   Injector (peak and hold): 8
*   Digital Pulsed Outputs (DPO): 6
*   Power for Ignition Switch: 1
*   Half Bridge Outputs (HBO): 6
*   25A High Current Outputs (25A HCO): 4

### Inputs
*   Onboard MAP sensor (4 bar): 1
*   Analog Voltage Inputs (AVI): 11
*   Differential Engine Position Inputs: 2 (Trigger and Home)
*   Synchronised Pulsed Inputs (SPI): 6
*   Knock Inputs: 2
*   Universal Wideband Controllers (NTK/LSU 4.9): 1
*   Ignition Switch Input: 1

### Other
*   Inertial Measurement Sensor: Onboard, 6 Axis
*   4 Channel Oscilloscope: 50kSa/s per channel, 2ms/Div limit, optional external trigger
*   5V Sensor Supply: 1
*   8V Sensor Supply: 1
*   Sensor Ground: 1
*   Spare Ground pins for shields, sensors and low current CAN devices: 2

### Communications
*   CAN Bus Networks: 1000, 500 or 250 kbit/s (2 channels)
*   High Speed USB 2.0 (USB-C interface): 480 Mbit/s connection (1 channel)
*   Power up over USB: Datalogging, settings and firmware upgrade available
*   Wi-Fi: 900 kB/s datalog extraction. Hardware lockout for security

### Data Logging
*   Location: Onboard
*   Storage: 128MB
*   Max sampling frequency: 1kHz
*   Maximum channels per log: 300

### Dimensions
*   Enclosure (Not including connector protrusion): 196x130x44.5mm (7.7x5.2x1.8in)
*   Overall (Including connector protrusion): 196 x 149 x 44.5 mm (7.7 x 5.9 x 1.8 in)
*   Weight: 1.15 kg (2.53 lbs)
*   Operating Temperature (ambient): -40 to 85°C (-40 to 185°F)
*   12 x Onboard Temperature Sensing Zones:
    *   ECU: -40 to 125°C (-40 to 255°F)
    *   PDM: -40 to 150°C (-40 to 302°F)

### Electrical
*   Power Supply (across power terminals): 8 to 22V
*   No output static current draw: < 1A
*   Low Power Mode (USB): 4 to 5.5V
*   Static current draw from USB port: < 500mA

### Features
*   Drive-By-Wire Throttle Support: 2
*   Flex Fuel: YES
*   Closed Loop O2 Control: Dual Bank
*   Knock Control: Dual
*   Variable Cam Control: Up to 4
*   Long Term Learning: Up to 4D
*   Data Logging: Laptop + Onboard
*   Anti-Lag Rotational Idle: YES
*   Launch Control: YES
*   Traction Control: YES
*   Tuning Table Resolution: 32 x 32 x 8 4D
*   Engine Protection: Multi Level
*   CAN Networks: 2
*   Nitrous Control: Stage 6
*   Boost Control: 4D Closed Loop
*   CO2 Control: YES
*   Intake Air Bleed Control: YES
*   Flat Shift Control: Advanced
*   Shock Travel & Ride Height: YES
*   Trans Brake: YES
*   Race Timer: YES
*   Advanced Torque Management: YES
*   On-board Wideband: Single Channel LSU 4.9 / NTK

## Nexus Software - NSP

### Installing the NSP software
Haltech NSP (Nexus Software Programmer) is the software used for tuning and programming the NEXUS R3 VCU. Follow these steps to install the Haltech NSP software:
1.  **Download the NSP installer:** Go to the Haltech website (www.haltech.com), navigate to the ‘Downloads’ section, and click on the download link.
2.  **Run the installer file:** Once the download is complete, locate the downloaded file (usually in the ‘Downloads’ folder of your computer) and double-click on the file to run the Nexus Software Setup Wizard.
3.  **Launch Haltech NSP:** Once the installation is complete, you can launch the Haltech NSP software from the Windows ‘Start’ menu or using the desktop shortcut that was created.

### Setting up Wi-Fi communications
Wi-Fi communication is another method for connecting the NEXUS R3 VCU to your laptop, serving as an alternative to a USB connection once the Wi-Fi module is enabled.

To set up your Wi-Fi connection follow these steps:
1.  Open NSP and connect your NEXUS R3 VCU using the provided USB-C cable.
2.  Click on ‘Connections’ in the navigation tree and enable the Wi-Fi module.
3.  Under ‘Connections’, select ‘Wi-Fi’ to set up your SSID and password. Note that your SSID must be at least 1 character long, and your password at least 8 characters.
4.  Click ‘Apply’.
5.  Power up the ECU using main power (ignition switch on), then go to your computer’s Network settings. Connect to your NEXUS R3 VCU by selecting your chosen SSID and entering your password.

**NOTE:** The VCU must be powered by the main power source for Wi-Fi communication. Up to two computers can connect to the VCU via Wi-Fi, and one via USB-C, at any given time. When the Wi-Fi module is disabled, it is completely inactive and held in an OFF state.

### Going online with the ECU
With the NSP software open, connect the supplied Haltech USB cable between your laptop and the USB-C port on the front of the NEXUS R3 VCU. The USB connection will let the NSP software automatically recognize the VCU and activate the unit in low power mode. This allows you to either upload a basemap or create a new one before installing the VCU into the vehicle. In low power mode, the VCU’s inputs and outputs are disabled, ensuring you to safely configure your vehicle setup prior to installing the unit and powering it up.

## Nexus R3 Connections

### Main power and ground
The NEXUS R3 must be connected to battery positive and battery negative at all times for correct operation. Connect the NEXUS R3 to the positive battery terminal via the supplied RED SurLok connector using a 4AWG cable and to the negative battery terminal via the black SurLok connector using a 4AWG cable.

### Ignition switch
The ignition switch input pin (A13) must be connected to a switched +12V source to turn the NEXUS R3 on.

*   **Method 1:** If wiring to an existing ignition key switch in the vehicle, it is important to make sure to wire A13 to the main ignition wire (i.e. not accessory) so it doesn’t loose power while the engine is cranking causing the VCU to momentarily turn off.
*   **Method 2:** Alternatively, the ignition switch input (A13) and the low current +12V power source (A26) can be switched together to turn the VCU On or Off.

**NOTE:** Pin A26 is a low current +12V source and must not be used to power any other device in the vehicle. Insulate and isolate if not used.

### Battery Ground Output
The battery ground output pins (A10, A11) are capable of 3A per pin and are directly linked to the battery negative stud internal to the NEXUS R3. These pins can be used for cable shielding connections or to ground low current CAN devices, digital sensors, or switch grounds.

**These battery ground output pins are NOT meant to ground the VCU and should not be connected to battery negative or the chassis.**

## Nexus R3 Wiring

### Crank (Trigger) and Cam (Home) Inputs
The crank and cam position sensors are required so that the VCU has the necessary information available to determine engine speed and position at any point in time. Generally two sensors are required - a cam position and crank position, however many engines will have just a cam position sensor that is capable of giving the VCU enough information to run the engine correctly.

Vehicles that have a crank position sensor only are not capable of determining the difference between compression stroke and exhaust stroke and therefore are not suitable for sequential fire applications. In this case a cam position sensor may need to be added.

It is recommended that four-core or twin-core shielded cable is used for crank and cam position sensors. Shields must be terminated to battery ground at one end only.

**Specs:**
*   -10V to +10V input
*   Selectable 1k2 or 440R pull-up to 5V
*   Selectable ground reference (full differential standard mode)
*   -75 to +75V indefinite withstand
*   48kHz max signal frequency

There are two common types of crank/cam sensor signals:
*   **Hall effect/optical signal (0-5V digital square wave signal):** This type of sensor sends out a digital square wave signal. Hall effect sensors usually have 3 wires; a power supply (5V, 8V or 12V), a ground and a signal out wire. The power supply can be taken from the Sensor +5V pin, sensor +8V pin or a HBO as required. The internal pullup will typically need to be enabled in the settings for Hall effect / optical sensors.
*   **Reluctor signal (analog style signal):** This type of sensor sends out a sine wave type of signal and will generally use two wires, signal positive (+) and signal negative ( - ). Reluctor sensors do not require external power as these sensors can generate their own voltage signal as the sensor reads a moving tooth or trigger. The internal pullup will need to be disabled in the settings in NSP for reluctor sensors.

### Injector Outputs
All injectors are to be wired directly to the VCU’s corresponding cylinder output pins. When an injection event occurs the VCU will ground the output pin, opening the injector. All injectors must be wired to a common +12V supply from one of the High Current Outputs on the NEXUS R3.

When not used for injection, pins can be used as generic Digital Pulsed Outputs (DPO) capable of switching 2A to ground.

**Specs:**
*   Number of channels: 8
*   Current controlled output
*   8A Peak, 2A Hold
*   0 to 55V voltage feedback

**Unused injector outputs can also be used as:**
*   Generic switched or PWM outputs (2A)
*   Low speed digital switch inputs (0-12V)

### Ignition Outputs
The ignition outputs produce a signal between 12V and ground to control the charging and firing of an ignition coil. Ignition outputs can only be connected directly to ignition coils if the coils are equipped with internal ignitors.

Ignition coils without internal ignitors draw large amounts of current and thus must use an external ignitor module to be safely triggered by the VCU. Connecting directly to ignition coils without internal ignitors will damage the VCU.

**Specs:**
*   Number of channels: 8
*   Software selectable global 12V or 5V pull-up
*   Software selectable individual 270R pull-up
*   10kHz switching speed
*   Automatic overtemp, overcurrent, flyback protection
*   0 to 27V voltage feedback

**Unused ignition outputs can also be used as:**
*   Generic DPO (3A sink) or PWM outputs
*   Low speed digital switch inputs (0-12V)

**WARNING:** Connecting the VCU to an ignition module before setting the ignition firing edge correctly may damage the module and coils, therefore it is advised to disconnect the module or disable the power to the ignition system until the unit has been setup and configured.

### Half Bridge Outputs (HBO)
Half Bridge Outputs are push-pull Pulse Width Modulated (PWM) outputs that can be used to control DBW throttle motors, idle air stepper motors or electronic wastegates. If not being used as push-pull drivers, Half Bridge Outputs on the NEXUS R3 can also be used as generic high side or low side outputs capable of driving 8A to 12V, or sinking 8A to ground.

When used for DBW throttle motors, any HBO pair can be arbitrarily used and assigned (e.g. HBO 1 and HBO 4) in the DBW wiring settings in the NSP software.

**Specs:**
*   Number of channels: 6
*   8A to 12V (high), or 8A to ground (low) output
*   5A max when used as push-pull PWM (eg DBW)
*   Automatic overcurrent and overtemperature protection
*   0 to 27V feedback
*   High side current feedback
*   18kHz switching speed in DBW mode

**Unused HBOs can be used as:**
*   Generic push/pull 2.2kHz PWM output DPO

### 25A High Current Outputs
The NEXUS R3 features four high/low outputs capable of sinking 25A to ground and driving 25A to 12V. Each output has a programmable fuse current, slow-start current and duration. Once the electronic fuse blows the output turns off for a pre-programmed delay duration before reactivating the output. You can use the NSP software to define the maximum number of retries before the output is deactivated until the next VCU reboot. The VCU LEDs conveniently display the output state.

25A HCOs are PWM capable and can be used for ignition power and injector power as well as to PWM thermofans and fuel pumps, control transbrake solenoids, nitrous solenoids etc.

**Specs:**
*   Number of channels: 4
*   25A source or sink current output
*   Automatic high and low side overcurrent and undervoltage lockout protection
*   0 to 30V feedback
*   High and low side current feedback
*   1kHz switching speed
*   Capable of 0-100% duty cycle

### Digital Pulsed Outputs (DPO)
Digital Pulsed Outputs are capable of producing pulsed waveforms with varying duty, varying frequency, or switched states. When a DPO is activated by the VCU the output will switch to ground. DPOs can be used to control various low-current devices such as shift lights, bypass air control valves, boost control solenoids, tachometers etc.

**Specs:**
*   Number of channels: 6
*   Selectable 4k7 pullup to 12V, to 5V, or disable.
*   Overcurrent, overheat, and flyback protection
*   Low side drive (3A max current)
*   10kHz switching speed
*   0 to 27V feedback

**Unused DPOs can be also be used as:**
*   Generic PWM outputs
*   Low speed digital switch inputs (0-12V) with pullup enable

### Synchronised Pulsed Inputs (SPI)
Synchronised Pulsed Inputs are capable of measuring the position, duty cycle, frequency or state of a signal, as well as analog voltage inputs. These inputs are suitable for sensors such as cam position sensors, fuel composition sensors, road speed sensors and flat shift switch.

Synchronised Pulsed Inputs are compatible with digital (hall effect or optical) and analog (reluctor) based sensors, have a maximum input voltage rating of 25V and can measure up to 22.5kHz Maximum frequency.

**Specs:**
*   Number of channels: 6
*   -10 to +10V digital input
*   0 to 5V analog input
*   Selectable 1k pull-up to 5V
*   -15 to +30V indefinite withstand
*   22.5kHz signal frequency max

### Knock Inputs
A knock sensor detects engine knock and sends a voltage signal to the VCU. The NEXUS R3 VCU uses the knock sensor signal to modify ignition timing if knocking occurs. Knock detection can be performed by the VCU by installing a compatible piezoelectric knock sensor mounted to the engine block.

It is recommended that twin-core shielded cable is used for knock sensors. Shields must be terminated to battery ground at one end only.

**Specs:**
*   Number of channels: 2
*   -2.5 to +2.5V AC input only
*   160Hz to 48kHz signal frequency band
*   +/-3V indefinite AC voltage withstand
*   50V indefinite DC withstand

### Analog Voltage Inputs (AVI)
Analog Voltage Inputs are inputs to the VCU that accept variable voltage signals from 0V to 5V such as signals from pressure, temperature and position sensors. These inputs can also accept switched inputs that change between two different voltage levels. The On Voltage and Off Voltage set in NSP defines what the thresholds are between the On and Off states. Common examples of switched inputs include A/C Request switch and intercooler spray switch.

AVIs have a software selectable 1K pull-up resistor to 5V, which can be enabled or disabled within the setup page. Pull-up resistors are generally enabled for temperature related sensors and switched to ground inputs and disabled with external +5V supply like a MAP sensor or throttle position sensor.

**Specs:**
*   Number of channels: 11
*   0 to 5V analog inputs
*   1000 samples per second
*   Selectable 1k pull-up to 5V
*   -10 to +30V indefinite withstand
*   1.5kHz signal frequency max

### Wideband Sensor Input
A wideband O2 sensor can be connected directly to the NEXUS R3’s onboard wideband controller. A wideband O2 sensor, by definition, measures a broad section of the Air Fuel Ratio (AFR) scale which is a useful tool for fuel tuning, closed loop O2 control, or for engine protection.

The NEXUS R3 supports onboard wideband control for Bosch LSU 4.9 or NTK wideband sensors, which can be selected in the wideband O2 sensor settings in NSP.

If more than one wideband O2 sensor is required, the NEXUS R3 can be further expanded to use multiple wideband O2 sensors by using external Haltech CAN wideband controller kits such as the Haltech WB1 or Haltech WB2.

### Haltech CAN System
The NEXUS R3 includes two channels of CAN: CAN 1 and CAN 2 - which may be used with a range of Haltech CAN expansion products, or to work with a supported vehicle CAN device (eg factory cluster).

**Specs:**
*   Supports CAN speeds up to 1 Mbit/s
*   Selectable 120ohm termination resistor per CAN channel
*   Supports all Haltech CAN expansion products
*   Selectable preconfigured vehicle CAN interface (OBDII compliant)

## Warranty & Contact

### Haltech Limited Warranty
Unless specified otherwise, Haltech warrants its products to be free from defects in material or workmanship for a period of 12 months from the date of purchase.

### Haltech Off-Road Usage Policy
Haltech products are designed and sold for sanctioned off-road/competition non-emissions controlled vehicles only and may never be used on a public road or highway.

### Contact Information
*   **Haltech Australia:** +61 2 9729 0999 | aus@haltech.com
*   **Haltech New Zealand:** 09 887 0616 | nz@haltech.com
*   **Haltech USA East:** (888) 298 8116 | usa@haltech.com
*   **Haltech USA West:** (888) 298 8116 | usa@haltech.com
*   **Haltech UK:** +44 121 285 6650 | uk@haltech.com
*   **Haltech Europe:** +43 720 883968 | europe@haltech.com
