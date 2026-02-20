# Space Plan - neuroscience-general-combo-0058

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-demirtasetal19-demirtasetal19-model, neuroscience-other-dendritic-na-inactivation-drives-a-decrease-in-i-59480-model, neuroscience-other-dendritic-na-spike-initiation-and-backpropagatio-124394-model, neuroscience-other-dendritic-signals-command-firing-dynamics-in-a-c-147218-model

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
