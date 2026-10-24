# Precision Signal Conditioning & L298N Actuator Control Module

## 📌 Project Overview
This project focuses on the design, simulation, and fault isolation analysis of an isolated signal conditioning circuit integrated with an L298N motor driver. Built for noisy industrial control environments, the module protects sensitive microcontroller units (MCUs) from transient voltage spikes (up to 24V) and Electromagnetic Interference (EMI) using an Optocoupler (PC817) interface.

## 🛠️ Key Technical Features
- **Optocoupler Signal Isolation:** Converts and dampens high-voltage transient noise/spikes (24V) into clean 5V TTL logic levels for safe MCU pin interface.
- **Actuator Control Interface:** L298N H-Bridge driver for bidirectional motor control with flyback diode protection (1N4007) against inductive back-EMF.
- **Dual Power Rail Architecture:** Separated logic supply (5V) and heavy-duty motor supply (12V) to eliminate electrical noise coupling.
- **Fault Isolation & Diagnosis:** Comprehensive troubleshooting matrix for board-level repair and component failure analysis.

## 📊 Circuit Simulation & Oscilloscope Results
- **Simulation Platform:** Proteus 8 Professional (VSM)
- **Input Signal:** 24V AC/Transient Industrial Voltage Spike
- **Conditioned Output:** 0-5V Precision Square Wave Logic

*(Insert your Oscilloscope & Schematic Screenshots here)*

## 📋 Board-Level Troubleshooting & Fault Matrix
| Component / Node | Failure Mode | Root Cause | Corrective Action |
| :--- | :--- | :--- | :--- |
| **Input Resistor (R1)** | MCU Input Stuck High | High Resistance (220kΩ) limiting LED current | Replace with 220Ω (1/4W) precision resistor |
| **L298N Logic Supply (Pin 9)** | Driver Overheating / Fault | Incorrect connection to +12V Motor Rail | Re-route VCC to isolated +5V logic rail |
| **Sense Pins (1 & 15)** | Motor Inoperative | Open circuit / Floating return path | Connect SENSA and SENSB directly to GND |
| **Inductive Load (Motor)** | Voltage Spikes on Switching | Missing flyback/freewheeling diodes | Install 4x 1N4007 fast-recovery diodes |

## 👨‍💻 Author
**Muhammad Hilmi Faidhi**  
Computer Engineering Technology Student – Politeknik Pertanian Negeri Payakumbuh
