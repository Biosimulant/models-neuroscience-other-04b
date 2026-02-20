# Space Plan - neuroscience-cortical-circuits-combo-0065

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-drt-neuron-model-sousa-et-al-2014-151949-model, neuroscience-other-dynamic-cortical-interlaminar-interactions-carra-150806-model, neuroscience-other-dynamics-of-spike-initiation-prescott-et-al-2008-116123-model, neuroscience-other-ebneretal2019-ebneretal2019-model

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
