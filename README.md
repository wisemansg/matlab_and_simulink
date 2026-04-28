# ☀️ Photovoltaic Power Generation System

## 📖 1. Project Overview

This project deals with the **design and simulation** of a photovoltaic (PV) power generation system for home use using **MATLAB and Simulink** software. 

The power plant is composed of:
- Photovoltaic panels
- DC-DC boost converter
- DC-AC inverter with passive filter

The system converts solar energy into usable AC power through a two-stage power conversion architecture.

## ⚙️ 2. System Architecture

**PV Array → DC-DC Boost Converter → DC-AC Inverter → Passive LC Filter**

![System Architecture](https://raw.githubusercontent.com/wisemansg/matlab_and_simulink/main/assets/Project1%20System%20Architecture.png)

## 🖼️ 3. Simulink Model

### Full Simulink Model View

![Complete Simulink Model](https://raw.githubusercontent.com/wisemansg/matlab_and_simulink/main/assets/Full%20Simulink%20Model%20View.png)

### Key Subsystems

**PV Array & Boost Converter Stage**  
![PV Array and Boost Converter](https://raw.githubusercontent.com/wisemansg/matlab_and_simulink/main/assets/PV_Array_Boost_Converter_Stage.png)

**Inverter & Filter Stage**  
![Inverter and Filter Stage](https://raw.githubusercontent.com/wisemansg/matlab_and_simulink/main/assets/Inverter%20%2B%20Filtered%20Output.png)

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

**1. PV Array Output (Voltage)**  
![PV Array Output](https://raw.githubusercontent.com/wisemansg/matlab_and_simulink/main/assets/PV%20Array%20Output%20(Voltage).png)

**2. DC Link Voltage (After Boost Converter)**  
![DC Link Voltage](https://raw.githubusercontent.com/wisemansg/matlab_and_simulink/main/assets/DC%20Link%20Voltage%20(After%20Boost%20Converter).png)

**3. Inverter + Filtered Output**  
![Inverter and Filtered AC Output](https://raw.githubusercontent.com/wisemansg/matlab_and_simulink/main/assets/Inverter%20%2B%20Filtered%20Output.png)

## 🔍 5. Deep Dive Analysis & Key Parameters

### Simulation Parameters
| Parameter          | Value              |
|--------------------|--------------------|
| Solver             | VariableStepAuto   |
| Stop Time          | 10.0 seconds       |
| Relative Tolerance | 1e-3               |

### PV Array Configuration
| Parameter           | Value             |
|---------------------|-------------------|
| Parallel Strings    | 20                |
| Series Modules      | 10                |
| Temperature         | [45 25] °C        |

### PWM & Inverter Settings
| Parameter            | Value          |
|----------------------|----------------|
| Carrier Frequency    | 1620 Hz        |
| Modulation Index     | 0.8            |
| Fundamental Frequency| 60 Hz          |


## 🛠️ 6. Technology Stack

- **Simulation Software:** MATLAB + Simulink
- **Library:** Simscape Electrical (Power Systems Blockset)
- **Key Components:** PV Array, Universal Bridge, PWM Generator (2-Level), IGBT/Diode, Series RLC Branch, powergui


## 📥 7. Download the Model

You can directly download the complete project files:

- **Main Simulink Model**: [`Project1.slx`](https://github.com/wisemansg/matlab_and_simulink/blob/main/assets/Project1.slx)


## 🚀 8. How to Run the Simulation

1. Open MATLAB
2. Load the model: `Project1.slx`
3. Make sure **Simscape Electrical** toolbox is installed
4. Run the simulation (`Ctrl + T`)
5. View results in the Scope blocks


## 📝 Notes

- The model uses detailed switching devices (IGBT/Diode) for realistic simulation.
- Parameters can be adjusted for different weather conditions.
- Good base for learning grid-tied or standalone PV systems.
