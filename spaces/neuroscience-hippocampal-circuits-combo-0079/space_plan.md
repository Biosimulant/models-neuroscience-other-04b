# Space Plan - neuroscience-hippocampal-circuits-combo-0079

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-compartmental-differences-camp-signaling-pathways-hippocam-osb245529-model, neuroscience-other-compartmental-differences-in-camp-signaling-path-245529-model, neuroscience-other-complex-ca1-neuron-study-ap-initiation-osb123927-model, neuroscience-other-complex-ca1-neuron-to-study-ap-initiation-wimmer-123927-model

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
