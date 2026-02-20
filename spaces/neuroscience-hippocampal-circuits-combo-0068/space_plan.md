# Space Plan - neuroscience-hippocampal-circuits-combo-0068

## Scientific Scope
- Domain: neuroscience
- Theme: hippocampal_circuits
- Base models: neuroscience-other-channel-density-variability-among-ca1-neurons-osb244688-model, neuroscience-other-chirp-stimulus-responses-in-a-morphologically-re-147578-model, neuroscience-other-cholinergic-modulation-shifts-response-ca1-pyramidal-cells-depolarizing-ramps-via-osb267599-model, neuroscience-other-cholinergic-modulation-shifts-the-response-of-ca-267599-model

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
