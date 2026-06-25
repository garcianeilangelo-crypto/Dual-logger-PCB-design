# 📡 EchoLight — Dual Noise & Light Logger

A compact, low-power embedded sensing platform that simultaneously captures acoustic and ambient light data and transmits synchronized measurements over Bluetooth Low Energy (BLE).

Developed at **Politecnico di Torino (DET)** as a complete embedded system project covering hardware design, firmware development, power management, sensor integration, and wireless communication.

---

## 🚀 Overview

EchoLight is a dual-sensor environmental logger designed to monitor and correlate acoustic and illumination conditions in real time.

The device:

* Measures sound levels from **60 Hz to 20 kHz**
* Measures ambient light from **0.01 lux to 83 klux**
* Synchronizes sensor measurements in firmware
* Performs onboard signal processing (IIR filtering and RMS computation)
* Transmits data wirelessly using Bluetooth Low Energy (BLE)
* Operates for approximately **5 days** on a **2000 mAh Li-ion battery**

---

## ✨ Key Features

### 🎤 Acoustic Monitoring

* Digital MEMS microphone acquisition
* Wide frequency response
* Noise-resilient digital audio path
* Real-time signal processing

### 💡 Ambient Light Monitoring

* High-resolution lux measurements
* Wide dynamic range sensing
* I²C-based sensor communication

### 🔄 Synchronized Data Acquisition

Both sensing channels are time-aligned in firmware to ensure accurate environmental correlation between sound and light measurements.

### 📶 Bluetooth Low Energy Connectivity

* Wireless data transmission
* Low-power communication
* Mobile application compatibility
* Efficient packet structure

### 🔋 Low-Power Operation

* Duty-cycled acquisition strategy
* Optimized BLE advertising and transmission
* Long battery lifetime

---

## 🧩 Hardware Architecture

### Microcontroller

**TI CC2640R2F**

* ARM Cortex-M3 MCU
* Integrated Bluetooth Low Energy radio
* Ultra-low-power operation

### Acoustic Sensor

**ICS-43434 Digital MEMS Microphone**

* I²S digital interface
* High signal integrity
* Reduced analog noise susceptibility

### Light Sensor

**OPT3001 Ambient Light Sensor**

* I²C interface
* Human-eye spectral response
* High measurement accuracy

### Power Management

**MAX1555**

* Li-ion battery charger

**TLV75801**

* 3.0 V low-dropout regulator (LDO)

### RF Section

* Chip antenna
* LC matching network
* Controlled-impedance 50 Ω microstrip routing

### User Interface

* RGB status LEDs
* Hardware reset button

---

## 🛠 Engineering Highlights

### Synchronous Sensing Architecture

Accurate temporal alignment between acoustic and optical measurements enables meaningful environmental correlation and analysis.

### Noise-Robust Design

The use of a digital MEMS microphone eliminates sensitive analog audio paths and improves immunity to electromagnetic interference.

### RF-Aware PCB Design

The wireless subsystem incorporates:

* Controlled impedance traces
* RF matching network
* Optimized antenna placement

to maximize communication reliability.

### Battery Optimization

Power consumption was minimized through:

* Duty-cycled sensor acquisition
* Efficient firmware scheduling
* Lightweight BLE packet transmission

allowing multi-day autonomous operation.

---

## 📂 Repository Structure

```text
echolight/
├── firmware/
├── hardware/
│   ├── Schematics
│   ├── PCB Layout
│   └── Gerbers
├── documentation/
│   ├── Technical Report
│   └── Presentation
├── BOM/
│   └── Bill of Materials.xlsx
└── README.md
```

---

## 🧠 Technical Skills Demonstrated

* Embedded C Development
* Bluetooth Low Energy (BLE)
* ARM Cortex-M Firmware
* Digital Signal Processing (DSP)
* I²C Communication
* I²S Audio Interfaces
* Low-Power Embedded Design
* PCB Design and Layout
* RF Design Fundamentals
* Battery-Powered Systems
* Hardware/Firmware Co-Design
* Sensor Integration

---

## 📊 System Block Diagram

```text
           +--------------------+
           | ICS-43434 MEMS Mic |
           +---------+----------+
                     |
                     | I²S
                     |
                     v
+-----------+   +----------------+   +-----------+
| OPT3001   |-->| TI CC2640R2F   |-->| BLE Radio |
| Light Sen.|   | ARM Cortex-M3  |   +-----------+
+-----------+   +----------------+
                     |
                     |
                     v
              +-------------+
              | RGB LEDs    |
              +-------------+

                     |
                     v
              +-------------+
              | Li-Ion Batt |
              +-------------+
```

---

## 👥 Team

**Neil Angelo Ilagan Garcia**
**Maikel Maakaroun**
**Pietro Sciolla**

Department of Electronics and Telecommunications (DET)
Politecnico di Torino

---

## 📜 Project Summary

EchoLight demonstrates the complete development cycle of a modern embedded IoT sensing platform, combining hardware design, firmware engineering, digital signal processing, low-power techniques, and wireless communication into a compact battery-powered device capable of synchronized environmental monitoring.

---

### Keywords

Embedded Systems • Firmware Engineering • BLE • ARM Cortex-M • DSP • I²C • I²S • MEMS Microphone • Ambient Light Sensing • Low-Power Design • PCB Design • RF Design • IoT • Wireless Sensor Networks
