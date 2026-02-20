# Space Plan - neuroscience-basal-ganglia-dopamine-combo-0064

## Scientific Scope
- Domain: neuroscience
- Theme: basal_ganglia_dopamine
- Base models: neuroscience-other-dopamine-activation-of-signaling-pathways-in-a-m-154968-model, neuroscience-other-dopamine-modulated-medium-spiny-neuron-reduced-m-128818-model, neuroscience-other-dopaminergic-cell-bursting-model-kuznetsov-et-al-64285-model, neuroscience-other-dynamic-dopamine-modulation-in-the-basal-ganglia-79488-model

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
