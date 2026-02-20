# Space Plan - neuroscience-hippocampal-circuits-combo-0013

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-detailed-passive-cable-model-of-dentate-gyrus-ba-140789-model, neuroscience-other-distributed-synaptic-plasticity-and-spike-timing-149913-model

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
