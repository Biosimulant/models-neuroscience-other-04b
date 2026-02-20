# Space Plan - neuroscience-basal-ganglia-dopamine-combo-0061

## Scientific Scope
- Domain: neuroscience
- Theme: basal_ganglia_dopamine
- Base models: neuroscience-other-d2-dopamine-receptor-modulation-of-interneuronal-98005-model, neuroscience-other-dbs-of-a-multi-compartment-model-of-subthalamic-151460-model, neuroscience-other-differential-modulation-of-pattern-and-rate-in-a-84612-model, neuroscience-other-dopamine-activation-of-signaling-pathways-in-a-m-154968-model

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
