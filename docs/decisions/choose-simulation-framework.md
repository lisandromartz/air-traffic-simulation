# Choose simulation framework

- Date: 2026-09-18
- Decision: Use SimPy for the current simulation implementation

## Context

The previous projects were implemented using Arena.

Arena provided the simulation environment used to model aircraft, airports, routes, operational delays and capacity restrictions.

For the current iteration, the project requires closer integration between historical data processing, statistical analysis and the simulation model.

The current workflow is primarily based on Python and uses tools such as Pandas, NumPy and SciPy for data analysis.

## Decision

The current simulation will be implemented using SimPy.

Python will serve as the common environment for the entire project workflow.

## Rationale

The main reason for selecting SimPy is the integration between the simulation and the existing Python-based data analysis workflow.

This allows historical data and simulation models to share the same programming environment and data structures.

It also allows the project to maintain the simulation logic as version-controlled source code and to test components using standard Python tooling.

The 2024 project also documented practical limitations associated with the student version of Arena, including restrictions affecting the scale of simulations and collaboration.

These limitations are part of the context for evaluating a different implementation approach in the current project.

## Alternatives considered

### Arena

Arena was used successfully in the previous projects and therefore represents the most direct continuation of the implementation.

It was not selected for the current iteration because the new workflow places greater emphasis on integration with Python-based data analysis, reproducibility and source-code-based development.

### SimPy

Selected for the current implementation.

It provides the event, process and resource abstractions required by the current model while remaining within the Python ecosystem.

### Salabim

Could provide additional simulation-oriented functionality and visualization capabilities.

It may be considered if integrated animation becomes an important requirement.

### AnyLogic

Provides extensive support for multiple simulation paradigms and visual modeling.

It was not selected because the current project does not require that level of modeling integration.

## Consequences

### Positive

- Direct integration with Pandas, NumPy and SciPy.
- Simulation logic is represented as Python source code.
- Easier integration with automated testing.
- Reproducible execution through Python environments and random seeds.
- Easier integration with notebooks and statistical analysis.

### Negative

- Visualization must be implemented or integrated separately.
- The model requires more software development than a purely graphical modeling environment.
- Some functionality available directly in specialized commercial simulation software must be implemented explicitly.

## Reassessment

The framework decision may be revisited if the project requires simulation features that cannot be implemented reasonably with SimPy.