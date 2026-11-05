# Industrial Methanol Production Plant – Process Simulation & Optimisation
A steady-state process simulation and parametric optimization of an industrial-scale methanol production plant, developed using DWSIM.

**Farhan Ali** | Department of Chemical Engineering, National Institute of Technology Rourkela

## Project Overview

This project focuses on the process simulation of an industrial methanol production plant using **DWSIM**, an open-source chemical process simulator.

The process is based on the catalytic hydrogenation of carbon monoxide using hydrogen to produce methanol. The flowsheet incorporates feed compression, mixing, heating, an equilibrium reactor, cooling, gas–liquid separation, and gas recycle.

The primary objective is to simulate the methanol production process, obtain a converged recycle loop, and analyse the composition and production rate of the methanol-rich product stream.

## Project Details

| Information | Details |
|---|---|
| Project Title | Industrial Methanol Production Plant |
| Simulation Software | DWSIM Classic |
| Project Type | Process Simulation and Analysis |

## Process Chemistry

The main reaction considered in the simulation is:

$$
\text{CO} + 2\text{H}_2 \rightleftharpoons \text{CH}_3\text{OH}
$$

Carbon monoxide reacts with hydrogen to produce methanol.

## Process Flow Description

The simulated process consists of the following major operations:

1. **Fresh Syngas Feed:** Hydrogen and carbon monoxide are introduced at a molar ratio of 2:1.
2. **Compression:** The fresh feed is compressed from 30 bar to 80 bar.
3. **Mixing:** Compressed fresh syngas is mixed with recycled unreacted gas.
4. **Heating:** The combined feed is heated to 251.85°C.
5. **Equilibrium Reactor:** The synthesis gas undergoes the methanol formation reaction.
6. **Cooling:** The reactor outlet is cooled to 35°C.
7. **Gas–Liquid Separation:** The methanol-rich liquid product is separated from the unreacted gas.
8. **Gas Recycle:** The unreacted gas is recycled to the feed mixer.

## Process Flowsheet

The DWSIM flowsheet represents the complete process configuration, including the recycle loop.

![Methanol Production Plant Flowsheet]("C:\Users\farha\OneDrive\Desktop\Methanol-Production-Plant-DWSIM\Images\Full_Flowsheet.jpg")

## Simulation Components

The following chemical components were included in the simulation:

- Hydrogen (H₂)
- Carbon Monoxide (CO)
- Carbon Dioxide (CO₂)
- Methanol (CH₃OH)
- Water (H₂O)
- Nitrogen (N₂)

**Property Package:** Peng–Robinson (PR)

## Operating Conditions

| Parameter | Value |
|---|---:|
| Fresh Feed Flow Rate | 100 kmol/h |
| Fresh Feed Temperature | 25°C |
| Fresh Feed Pressure | 30 bar |
| Hydrogen Composition | 66.6667 mol% |
| Carbon Monoxide Composition | 33.3333 mol% |
| Compressor Outlet Pressure | 80 bar |
| Compressor Efficiency | 75% |
| Reactor Temperature | 251.85°C |
| Reactor Pressure | 80 bar |
| Cooler Outlet Temperature | 35°C |
| Separator Pressure | 80 bar |

## Key Simulation Results

The following results were obtained from the recorded DWSIM product-stream data.

| Performance Parameter | Result |
|---|---:|
| Total Product Flow | 33.5448 kmol/h |
| Methanol Mole Fraction | 99.057 mol% |
| Methanol Production Rate | 33.2286 kmol/h |
| Methanol Mass Production | 1,064.64 kg/h |
| Daily Methanol Production | 25.55 tonnes/day |
| Product Temperature | 35°C |
| Product Pressure | 80 bar |

## Recycle Loop Convergence

A recycle loop was implemented to return unreacted synthesis gas to the feed mixer.

Recorded convergence information:

- Recycle block: `RCY-101`
- Convergence status: Converged
- Iterations taken: 2
- Maximum iterations: 20
- Reported average recycle error: 0.00%

The convergence result indicates that the recycle calculation reached the simulator's convergence criterion for the recorded run.

## Results and Analysis

The simulation produced a methanol-rich liquid product with approximately 99.057 mol% methanol.

The recycle arrangement allows unreacted gases to return to the reactor feed instead of being treated as a once-through outlet. This provides a basis for studying the effect of recycle on process performance.

The reported production rate is approximately 25.55 tonnes of methanol per day, assuming continuous operation for 24 hours.
