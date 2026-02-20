# Space Plan - neuroscience-cortical-circuits-combo-0018

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-coding-explains-development-binocular-vision-its-failure-amblyopia-osb261483-model, neuroscience-other-coding-stimulus-frequency-latency-thalamic-networks-osb58582-model

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
