# Space Plan - neuroscience-general-combo-0056

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-contribution-of-atp-sensitive-potassium-channels-120243-model, neuroscience-other-control-of-vibrissa-motoneuron-firing-harish-and-127022-model, neuroscience-other-controlling-kca-channels-with-different-ca2-buff-138382-model, neuroscience-other-csashowcase-csashowcase-model

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
