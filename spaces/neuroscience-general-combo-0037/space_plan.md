# Space Plan - neuroscience-general-combo-0037

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-circadian-clock-model-in-mammals-pk-pd-model-kim-148320-model, neuroscience-other-classic-model-of-the-tritonia-swim-cpg-getting-1-93326-model, neuroscience-other-classic-tritonia-swim-cpg-osb93326-model

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
