# Space Plan - neuroscience-hippocampal-circuits-combo-0070

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-cholinergic-modulation-shifts-response-ca1-pyramidal-cells-depolarizing-ramps-via-osb267599-model, neuroscience-other-cholinergic-modulation-shifts-the-response-of-ca-267599-model, neuroscience-other-circadian-rhythmicity-shapes-astrocyte-morpholog-257027-model, neuroscience-other-circadian-rhythmicity-shapes-astrocyte-morphology-neuronal-function-ca1-osb257027-model

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
