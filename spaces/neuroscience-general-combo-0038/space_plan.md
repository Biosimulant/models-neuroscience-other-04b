# Space Plan - neuroscience-general-combo-0038

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-clc-2-channels-regulate-neuronal-excitability-no-142993-model, neuroscience-other-clc-channels-regulate-neuronal-excitability-not-intracellular-cl-levels-osb142993-model, neuroscience-other-cn-bushy-stellate-neurons-osb126899-model

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
