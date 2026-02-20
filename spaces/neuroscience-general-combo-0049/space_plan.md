# Space Plan - neuroscience-general-combo-0049

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-compartmentalization-gabaergic-inhibition-dendritic-spines-osb143604-model, neuroscience-other-compartmentalization-of-gabaergic-inhibition-by-143604-model, neuroscience-other-competing-oscillator-5-cell-circuit-and-paramete-149910-model

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
