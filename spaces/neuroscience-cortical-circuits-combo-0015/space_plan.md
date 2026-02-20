# Space Plan - neuroscience-cortical-circuits-combo-0015

## Scientific Scope
- Domain: neuroscience
- Theme: cortical_circuits
- Base models: neuroscience-other-channel-parameter-estimation-current-clamp-neuronal-properties-osb54154-model, neuroscience-other-cholinergic-modulation-resting-state-networks-osb2016670-model

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
