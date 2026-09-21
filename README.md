# 🇦🇷 Air Traffic Simulation

Discrete-event simulation of Argentina's commercial air transport network.

> Academic project — Sistemas de Tiempo Real, Universidad Nacional de La Plata.

## Overview

This project develops a discrete-event simulation model of commercial air traffic through a selected network of Argentine airports.

The model uses historical flight movement data to characterize traffic patterns and generate stochastic flight demand.

The simulation is used to study airport capacity scenarios, including the potential incorporation of La Plata Airport (LPG) as an alternative under capacity restrictions at Aeroparque (AEP) and Ezeiza (EZE).

## Background

This project is an evolution of an air traffic simulation developed for Sistemas de Tiempo Real at Universidad Nacional de La Plata.

The work originated with a project developed in 2023, which served as the basis for a subsequent version developed in 2024.

The current project revisits those models and extends them through a data-driven workflow implemented in Python and SimPy. The new iteration introduces more detailed historical flight movement data, a revised traffic-generation methodology and the incorporation of La Plata Airport (LPG) into the scenario analysis.

## Objectives

- Characterize domestic and international air traffic using historical data.
- Develop probabilistic flight-generation models.
- Build a discrete-event simulation of the selected airport network.
- Model airport capacity constraints.
- Evaluate capacity-reduction scenarios.
- Study the potential role of La Plata Airport.
- Validate simulated traffic against historical observations.

## Methodology

The project follows the following pipeline:

Historical data
→ Data preprocessing
→ Statistical analysis
→ Probabilistic modeling
→ Discrete-event simulation
→ Scenario experiments
→ Validation

## Technology

- Python 3.14
- Pandas
- NumPy
- SciPy
- SimPy
- Matplotlib
- Jupyter
- Quarto
- pytest
- Ruff

## Project structure

```text
src/          Source code
data/         Datasets and data documentation
notebooks/    Exploratory analysis
experiments/  Simulation experiments
tests/        Automated tests
docs/         Technical documentation
report/       Quarto manuscript
```

## Documentation

Technical documentation is available in [`docs/`](docs/).

The academic report is developed as a Quarto manuscript in [`report/`](report/).

## Reproducibility

The project uses uv to manage Python dependencies and reproducible environments.

```bash
uv sync
uv run pytest
uv run ruff check .
uv run ruff format --check .
```

## Project status

🚧 In development.

## Academic context

This project is developed as part of the final requirements for Sistemas de Tiempo Real at Universidad Nacional de La Plata.

## Author

Lisandro Martinez