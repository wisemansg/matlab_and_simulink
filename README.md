# Aspen HYSYS - Pipeline Pressure Drop Simulation

## 📖 Overview
This is a basic steady-state simulation in Aspen HYSYS for a 350-meter water pipeline transporting feed water from a storage tank to a heat exchanger. The project focuses on modeling the pressure drop and temperature change along the pipeline under specified flow conditions.

## 🎯 Project Objective
The main objective is to accurately simulate the hydraulic performance of the pipeline with an inlet pressure of 1000 kPag and a flow rate of 15 m³/h, aiming to achieve a target outlet pressure of 400 kPag at the heat exchanger inlet. This study evaluates the pressure drop due to friction losses and provides insight into proper pipeline sizing.
![Project Goal](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%200.jpeg)  
## 📸 Project Model 


![Model](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%202.jpeg)  

![Model](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%201.jpeg)  


## ⚙️ Simulation Results

| Parameter         | Inlet       | Outlet (at 350 m) |
|-------------------|-------------|-------------------|
| Temperature       | 25.00 °C   | 24.44 °C         |
| Pressure          | 1000 kPag  | 732.8 kPag       |
| Flow Rate         | 15.01 m³/h | 15.01 m³/h       |
| **Pressure Drop** | —          | **267.2 kPa**    |

Main Results
![Main Flowsheet](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%204.jpeg)  

Detailed pressure and temperature profile along the pipe.
![Pipe Profile](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%203.jpeg)  

## 📊 Realistic Assessment
The simulation converged successfully without any errors or warnings (except hydrate formation being ignored). The outlet pressure achieved at the end of the 350-meter pipe is 732.8 kPag, while the target outlet pressure specified in the problem statement was 400 kPag. This means the pressure drop obtained in the simulation is only 267.2 kPa, which is significantly lower than the required pressure drop of approximately 600 kPa. This difference suggests that the pipe diameter chosen in the model is likely too large, resulting in lower friction losses than expected.

## 💭 Reflection
This project helped me practice setting up a simple pipeline in HYSYS, using the Pipe Segment unit operation, defining material streams with proper specifications, running the solver, and viewing the detailed pressure and temperature profiles along the pipe length. It also gave me good experience in comparing simulation results with the given design targets and understanding the importance of correct pipe sizing for achieving desired pressure drops in process piping systems.
