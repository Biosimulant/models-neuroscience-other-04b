# Space Plan - neuroscience-general-combo-0051

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-competition-model-of-pheromone-ratio-detection-z-143753-model, neuroscience-other-competition-pheromone-ratio-detection-osb143753-model, neuroscience-other-complex-dynamics-reproducing-golgi-cell-electror-262456-model

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
