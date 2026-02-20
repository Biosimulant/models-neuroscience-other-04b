# Space Plan - neuroscience-basal-ganglia-dopamine-combo-0060

## Scientific Scope
- Domain: neuroscience
- Theme: basal_ganglia_dopamine
- Base models: neuroscience-other-comparison-full-reduced-globus-pallidus-models-osb127728-model, neuroscience-other-comparison-of-full-and-reduced-globus-pallidus-m-127728-model, neuroscience-other-composite-spiking-network-neural-field-model-of-147366-model, neuroscience-other-composite-spiking-network-neural-field-parkinsons-osb147366-model

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
