# Space Plan - neuroscience-general-combo-0059

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-destexhe-jcns-2009-destexhejcns2009-model, neuroscience-other-determinants-of-fast-calcium-dynamics-in-dendrit-97903-model, neuroscience-other-deterministic-chaos-in-a-mathematical-model-of-a-125683-model, neuroscience-other-development-of-orientation-selective-simple-cell-147929-model

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
