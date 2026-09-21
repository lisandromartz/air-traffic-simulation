# Methodology

## 1. Overview

The project follows a data-driven discrete-event simulation methodology.

Historical flight movement data is processed and statistically analyzed to characterize commercial air traffic. The resulting traffic models are then used to generate stochastic demand in a simulation of the selected airport network.

The overall workflow is:

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
      ▼
Scenario experiments
      │
      ▼
Analysis and validation
```

## 2. Data preprocessing

Historical flight movement data is cleaned and transformed before being used for analysis.

The preprocessing stage includes:

* selecting the relevant flight classifications;
* selecting the airports included in the study;
* distinguishing domestic and international movements;
* distinguishing departures and arrivals;
* standardizing timestamps;
* selecting the analysis period; and
* aggregating movements into suitable temporal and spatial units.

The resulting datasets are used as the basis for both statistical analysis and model calibration.

## 3. Traffic characterization

The observed traffic is analyzed to identify its main spatial and temporal characteristics.

The analysis considers variables such as:

* airport;
* origin and destination;
* movement type;
* day of week; and
* hour of day.

Particular attention is given to route-specific traffic profiles and their variation throughout the week.

Temporal dependence in the observed traffic may also be analyzed where relevant.

## 4. Probabilistic traffic model

The statistical analysis is used to construct stochastic models of flight demand.

The initial approach considers the number of flights associated with a given route, day of week and hour.

Depending on the characteristics of the observed data, different probability models may be evaluated to reproduce the frequency and temporal distribution of flight movements.

The selected models will be calibrated using historical observations and their assumptions will be documented explicitly.

## 5. Discrete-event simulation

The simulation is implemented using SimPy.

The model represents the operational flow of flights through the selected airport network.

The main simulation components are:

* airports;
* flights;
* airport capacity resources;
* operational delays;
* queues;
* flight travel times; and
* disruption events.

Flight demand is generated according to the probabilistic traffic models obtained in the previous stages.

## 6. Capacity and disruption scenarios

The simulation is used to evaluate different operating conditions.

A baseline scenario represents normal operation. Additional scenarios introduce capacity reductions or disruptions at selected airports.

Particular attention is given to Aeroparque (AEP) and Ezeiza (EZE), including scenarios in which affected traffic may be redirected to alternative airports.

La Plata Airport (LPG) is incorporated as a potential alternative in these scenarios.

## 7. Experimental analysis

Each scenario is executed using controlled simulation parameters and reproducible random seeds.

The experiments will evaluate relevant system-level indicators, including:

* flight throughput;
* airport utilization;
* redirected flights;
* cancelled flights, where applicable;
* queue lengths;
* waiting times; and
* distribution of traffic across airports.

Multiple replications may be used where necessary to account for stochastic variability.

## 8. Validation

The simulation results are compared with historical observations to evaluate whether the model reproduces relevant characteristics of the observed system.

Validation will consider both aggregate and temporal properties, including:

* total flight volume;
* traffic by airport;
* traffic by route;
* hourly traffic profiles;
* day-of-week patterns; and
* temporal dependence.

The specific validation metrics and acceptance criteria will be defined as the model develops.