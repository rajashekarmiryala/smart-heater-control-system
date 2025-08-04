# Smart Heater Control System

**Author:** Rajashekar Miryala  
**Platform:** ESP32 (Wokwi Simulation)  
**Submission For:** Embedded Systems Intern – upliance.ai  
**Date:** August 2025

---

## Project Overview

The Smart Heater Control System is designed to monitor ambient temperature using an analog temperature sensor (simulated via potentiometer) and automatically control a heater based on defined temperature thresholds. The system includes overheat detection and alerts using a buzzer.

This project demonstrates embedded systems design principles including real-time sensor interfacing, GPIO control, analog-to-digital conversion, and state-based control logic using the ESP32 platform.

---

## Features

- Temperature sensing using ADC
- Automatic heater ON/OFF control based on threshold
- Buzzer alert for overheat condition
- LED indicator for heater status
- Serial output for real-time temperature and state information

---

## Hardware Components

| Component       | Quantity | Description                        |
|----------------|----------|------------------------------------|
| ESP32 DevKit-C | 1        | Main Microcontroller               |
| Potentiometer  | 1        | Simulates LM35 Analog Temp Sensor  |
| Buzzer         | 1        | Provides Overheat Alert            |
| LED            | 1        | Represents Heater ON/OFF Status    |

**Note:** The LM35 sensor is not available in Wokwi. A potentiometer is used to simulate analog temperature values in the circuit.

---

## System Logic

### Temperature State Table

| Temperature Range (°C) | System State | Action                     |
|------------------------|--------------|----------------------------|
| Below 20               | IDLE         | Heater OFF, Buzzer OFF     |
| 20 to 30               | HEATING      | Heater ON, Buzzer OFF      |
| Above 30               | OVERHEAT     | Heater OFF, Buzzer ON      |

---

## Simulation Instructions

1. Open the Wokwi simulation link provided below.
2. Adjust the potentiometer to change the analog temperature value.
3. Observe the behavior:
   - Heater (LED) turns ON when temperature is between 20°C and 30°C.
   - Buzzer is activated when temperature exceeds 30°C.
   - Serial Monitor displays the temperature and current state.

---

## File Structure

```plaintext
├── diagram.json         # Wokwi circuit diagram
├── sketch.ino           # Arduino code for the ESP32
├── README.md            # Project documentation
├── screenshots/         # Captured images of simulation states



