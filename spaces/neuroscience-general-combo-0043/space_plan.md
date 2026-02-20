# Space Plan - neuroscience-general-combo-0043

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-code-szoboszlay-et-al-functional-properties-dendritic-gap-junctions-cerebellar-osbGolgiCellDendGapJunctions-model, neuroscience-other-code-to-calc-spike-trig-ave-sta-conduct-from-vm-116086-model, neuroscience-other-coding-explains-development-of-binocular-vision-261483-model

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
