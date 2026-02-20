# Space Plan - neuroscience-cortical-circuits-combo-0031

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-democratic-population-decisions-result-in-robust-136807-model, neuroscience-other-dendritic-discrimination-of-temporal-input-seque-140828-model, neuroscience-other-direct-recruitment-of-s1-pyramidal-cells-and-int-147460-model

## Wiring Plan
- Comparative mode with monitor-only routing.
- Each base model state-like output connects to monitor ports `state_a..state_d`.
- No direct causal links among base models unless explicitly upgraded later.

## Visualization Plan
- Include `StateComparisonMonitor` and `StateMetricsMonitor`.
- Require at least:
  - one timeseries visual,
  - one summary table visual.

## Validation Gates
- space schema validity
- wiring endpoint validity
- smoke run success
- repo manifest/entrypoint validators pass
