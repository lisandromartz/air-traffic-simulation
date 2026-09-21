# Project Background

## 2023 — Original project

The project originated from an academic air traffic simulation developed in 2023 for Sistemas de Tiempo Real at Universidad Nacional de La Plata.

That work established the initial simulation model and experimental scenarios.

The simulation was implemented in Arena and focused on domestic air traffic between a selected group of Argentine airports.

Aircraft were generated at each airport and routed to their corresponding destinations using flight frequencies and route probabilities derived from historical aviation data obtained from ANAC and EANA. Aircraft were disposed once they reached their destinations.

Airports were represented using Arena Stations, which acted both as origins and destinations for aircraft.

The 2023 model introduced probabilistic route selection, airport capacity restrictions and basic scenarios for normal operation, reduced capacity and airport disruption.

## 2024 — Continuation

In 2024, the project was developed using the previous work as its starting point, extending the model to include international flights and a larger set of airports.

For domestic traffic, the model used aircraft as persistent entities. A population of 145 aircraft was created at the beginning of the simulation and remained in the system throughout the simulated period, allowing the same aircraft entities to be reused for multiple flights.

## 2026 — Current project

The current work revisits the 2024 model as part of the final requirements for Sistemas de Tiempo Real.

The main extension is the incorporation of La Plata Airport (LPG) and the analysis of its potential role as an alternative airport under capacity restrictions at other airports.

The project also revisits the traffic-generation methodology using more detailed historical flight movement data.

Unlike the previous implementations, the current workflow integrates data processing, statistical analysis and simulation within the Python ecosystem.

The simulation is being reimplemented using SimPy and is initially formulated as a discrete-event simulation.

## Evolution

The current project is not intended to reproduce the previous Arena model exactly.

Instead, the 2024 model serves as the immediate baseline for a new iteration that revisits the traffic model, simulation architecture and capacity scenarios.

The evolution can therefore be summarized as:

2023
→ Initial air traffic simulation with probabilistic routes and capacity scenarios

2024
→ Extension using Arena, persistent aircraft and international flights

2026
→ Data-driven reformulation using Python and SimPy, revised traffic modeling and La Plata Airport scenarios