# Data

This directory contains the datasets and derived data used by the air traffic simulation project.

## Data sources

### ANAC

- **Provider:** Administración Nacional de Aviación Civil (ANAC)
- **Maintainer:** Dirección Nacional de Desarrollo Tecnológico, Secretaría de Transporte
- **Dataset:** [Aterrizajes y despegues procesados por ANAC](https://datos.transporte.gob.ar/dataset/aterrizajes-y-despegues-procesados-por-la-administracion-nacional-de-aviacion-civil-anac)
- **Access date:** 2026-09-17
- **License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

Only records from 2023 to 2025 will be used.

The original ANAC dataset is not included in this repository.

## Data processing

The original data resources are filtered, transformed and aggregated for statistical analysis and simulation purposes.

The processing may include:

- selecting the relevant flight classifications;
- selecting the airports included in the study;
- distinguishing domestic and international movements;
- distinguishing departures and arrivals;
- standardizing timestamps;
- selecting the analysis period; and
- aggregating flight movements into suitable temporal and spatial units.

## Directory structure

```text
data/
├── raw/
│   └── Original datasets
│
├── processed/
│   └── Derived datasets used by analysis and simulation
│
└── README.md
```

## Reproducibility

Raw datasets are not stored in the repository when their size or distribution conditions make repository storage impractical. Users should obtain those datasets from their official sources and place the corresponding files in `data/raw/`.

Derived datasets are generated from the raw data through the project's data-processing workflow. The transformations applied to the original data should be documented.

Each dataset used by the project should document:

* data provider;
* dataset name;
* source;
* access date;
* applicable license; and
* relevant transformations.