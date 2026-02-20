# Space Plan - neuroscience-hippocampal-circuits-combo-0014

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-effect-of-polysynaptic-facilitaiton-between-piri-181032-model, neuroscience-other-effects-of-increasing-creb-on-storage-and-recall-151126-model

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
