# ☀️ Photovoltaic Power Generation System

**MATLAB/Simulink Simulation Project**  
**Author:** Wiseman Siriro

---

## 📖 1. Project Overview

This project deals with the **design and simulation** of a photovoltaic (PV) power generation system for home use using **MATLAB and Simulink** software. 

The power plant is composed of:
- Photovoltaic panels
- DC-DC boost converter
- DC-AC inverter with passive filter

The system converts solar energy into usable AC power through a two-stage power conversion architecture.

---

## ⚙️ 2. System Architecture

The power plant follows a classic **two-stage** conversion topology:

**PV Array → DC-DC Boost Converter → DC-AC Inverter → Passive LC Filter**

![System Architecture Diagram](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/assets/ARCHITECTURE_DIAGRAM.png)

---

## 🖼️ 3. Simulink Model

### Full Simulink Model View

![Complete Simulink Model](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/assets/FULL_SIMULINK_MODEL.png)

### Key Subsystems

**PV Array & Boost Converter Stage**  
![PV Array and Boost Converter](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/assets/PV_BOOST_STAGE.png)

**Inverter & Filter Stage**  
![Inverter and Filter Stage](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/assets/INVERTER_FILTER_STAGE.png)

---

## 📊 4. Simulation Results

### Key Performance Indicators

| Parameter                  | Value                  |
|---------------------------|------------------------|
| PV Array Configuration    | 20 parallel × 10 series modules |
| Boost Converter Reference | 1500 V DC              |
| Inverter Type             | 2-Level PWM Full Bridge|
| Carrier Frequency         | 1620 Hz (27×60)        |
| Simulation Stop Time      | 10.0 seconds           |
| Solver                    | VariableStepAuto       |

### Waveform Results

**PV Array Output (Voltage & Current)**  
![PV Output](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/assets/PV_OUTPUT.png)

**DC Link Voltage (After Boost Converter)**  
![DC Link Voltage](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/assets/DC_LINK_VOLTAGE.png)

**Inverter Output Before Filter**  
![Inverter PWM Output](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/assets/INVERTER_OUTPUT.png)

**Filtered AC Output (Voltage & Current)**  
![Filtered AC Output](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/assets/FILTERED_AC_OUTPUT.png)

---

## 🔍 5. Deep Dive Analysis & Key Parameters

### 5.1 Simulation Parameters
| Parameter          | Value              |
|--------------------|--------------------|
| Solver             | VariableStepAuto   |
| Stop Time          | 10.0 seconds       |
| Relative Tolerance | 1e-3               |
| Zero Crossing      | On                 |

### 5.2 PV Array Configuration (Most Important)
| Parameter              | Value                          |
|------------------------|--------------------------------|
| Parallel Strings (Npar)| 20                             |
| Series Modules (Nser)  | 10                             |
| Module Type            | User-defined                   |
| Temperature (°C)       | [45 25]                        |
| Pm (Max Power)         | 213.15 W                       |
| Voc                    | 36.3 V                         |
| Isc                    | 7.84 A                         |

### 5.3 PWM Generator Settings
| Parameter             | Value                  |
|-----------------------|------------------------|
| Modulator Type        | Single-phase           |
| Mode                  | Unsynchronized         |
| Carrier Frequency (Fc)| 27 × 60 = 1620 Hz      |
| Modulation Index (M)  | 0.8                    |
| Frequency (F)         | 60 Hz                  |

### 5.4 Boost Converter & Switching Devices
| Block                  | Key Parameter          | Value     |
|------------------------|------------------------|-----------|
| Constant (Vref)        | Value                  | 1500 V    |
| IGBT/Diode             | Ron                    | 1e-3 Ω    |
| Diode                  | Ron / Vf               | 0.001 / 0.8 V |
| Series RLC (Filter)    | L / C                  | 0.006 H / 0.006 F |

Full detailed block parameters are available in the **MATLAB PROJ1.pdf** report.

---

## 🛠️ 6. Technology Stack

- **Simulation Software:** MATLAB + Simulink
- **Library:** Simscape Electrical (Power Systems Blockset)
- **Key Components:** PV Array, Universal Bridge, PWM Generator (2-Level), IGBT/Diode, Series RLC Branch, powergui
- **Report Generation:** Simulink Default Report

---

## 📥 7. Download the Model

You can directly download the complete project files from this repository:

- **Main Simulink Model**: [`Project1.slx`](https://github.com/YOUR_USERNAME/YOUR_REPO/blob/main/Project1.slx)
- **Detailed Simulink Report**: [`MATLAB PROJ1.pdf`](https://github.com/YOUR_USERNAME/YOUR_REPO/blob/main/MATLAB%20PROJ1.pdf)
- **Entire Repository as ZIP**: [Download .zip](https://github.com/YOUR_USERNAME/YOUR_REPO/archive/refs/heads/main.zip)

---

## 🚀 How to Run the Simulation

1. Open MATLAB
2. Load the model: `Project1.slx`
3. Make sure **Simscape Electrical** toolbox is installed
4. Run the simulation (`Ctrl + T`)
5. View results in the Scope blocks

---

## 📝 Notes

- The model uses detailed switching devices for realistic dynamic simulation.
- Parameters can be adjusted for different weather conditions (irradiation & temperature).
- Suitable as a base for grid-tied or standalone PV system studies.

---

**Feel free to fork, improve, or use this model for your own photovoltaic system simulations!**

*Last updated: April 2026*
