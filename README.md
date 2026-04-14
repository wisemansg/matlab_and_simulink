# Aspen HYSYS - Pipeline Pressure Drop Simulation

## 📖 Overview
This is a basic steady-state simulation in Aspen HYSYS for a 350-meter water pipeline transporting feed water from a storage tank to a heat exchanger. The main purpose of this project is to model the pressure drop and temperature change of water flowing through a long pipeline under given flow conditions. The simulation helps understand how pressure decreases along the pipe due to friction and other losses.

## 🎯 Project Objective
![Project Goal](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%200.jpeg)  
**Figure 1:** Problem statement – 350 m pipeline, inlet pressure 1000 kPag, flow rate 15 m³/h, target outlet pressure 400 kPag.

## 📸 Project Model 

![Main Flowsheet](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%204.jpeg)  


![Stream Details](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%202.jpeg)  


![Model View](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%201.jpeg)  


## ⚙️ Simulation Results

| Parameter         | Inlet       | Outlet (at 350 m) |
|-------------------|-------------|-------------------|
| Temperature       | 25.00 °C   | 24.44 °C         |
| Pressure          | 1000 kPag  | 732.8 kPag       |
| Flow Rate         | 15.01 m³/h | 15.01 m³/h       |
| **Pressure Drop** | —          | **267.2 kPa**    |

Detailed pressure and temperature profile along the pipe.
![Pipe Profile](https://raw.githubusercontent.com/wisemansg/hysys/main/hysysassets/HYSYS%20pipeline%20design%203.jpeg)  

## 📊 Realistic Assessment
The simulation converged successfully without any errors or warnings (except hydrate formation being ignored). The outlet pressure achieved at the end of the 350-meter pipe is 732.8 kPag, while the target outlet pressure specified in the problem statement was 400 kPag. This means the pressure drop obtained in the simulation is only 267.2 kPa, which is significantly lower than the required pressure drop of approximately 600 kPa. This difference suggests that the pipe diameter chosen in the model is likely too large, resulting in lower friction losses than expected.

## 💭 Reflection
This project helped me practice setting up a simple pipeline in HYSYS, using the Pipe Segment unit operation, defining material streams with proper specifications, running the solver, and viewing the detailed pressure and temperature profiles along the pipe length. It also gave me good experience in comparing simulation results with the given design targets and understanding the importance of correct pipe sizing for achieving desired pressure drops in process piping systems.

**Note:** This is an introductory-level simulation.
