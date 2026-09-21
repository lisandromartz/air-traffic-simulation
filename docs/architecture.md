# Architecture

The project follows a modular architecture that separates data processing, statistical analysis, simulation, experimentation and visualization.

```text
Historical data
      │
      ▼
Data preprocessing
      │
      ▼
Statistical analysis
      │
      ▼
Traffic-generation models
      │
      ▼
Discrete-event simulation
      │
      ├── Airports
      ├── Flights
      ├── Capacity resources
      ├── Operational delays
      └── Disruption events
      │
      ▼
Scenario experiments
      │
      ▼
Analysis and validation
```

## Main components

### Data

Responsible for loading, cleaning and transforming historical flight movement data.

### Analysis

Responsible for the statistical characterization of historical traffic and the construction of traffic-generation models.

### Simulation

Contains the discrete-event simulation implemented using SimPy.

It represents airports, flights, resources, delays, queues and disruptions.

### Scenarios

Defines the configurations used to run the different experimental conditions.

### Visualization

Provides plots and other visualizations for historical data, simulation results and comparisons.

## Design principles

* Separate data processing from simulation logic.
* Keep simulation components independent from exploratory notebooks.
* Separate exploratory analysis from reusable code.
* Make simulation experiments reproducible through explicit configuration and random seeds.
* Prefer reusable Python modules over duplicated notebook code.
* Keep scenario definitions separate from the core simulation model.