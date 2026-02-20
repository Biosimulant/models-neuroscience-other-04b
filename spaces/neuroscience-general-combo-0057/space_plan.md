# Space Plan - neuroscience-general-combo-0057

## Scientific Scope
- Domain: neuroscience
- Theme: general
- Base models: neuroscience-other-currents-contributing-to-decision-making-in-neur-116606-model, neuroscience-other-cytoplasmic-electric-fields-and-electroosmosis-a-147740-model, neuroscience-other-dandiarchiveshowcase-dandiarchiveshowcase-model, neuroscience-other-data-driven-hh-type-model-of-the-lateral-pyloric-116957-model

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
