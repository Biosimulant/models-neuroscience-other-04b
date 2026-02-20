# COMBO_0065 - Neuroscience Cortical Circuits

## Scientific Question
How do cortical circuit motifs transform and propagate activity?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-drt-neuron-model-sousa-et-al-2014-151949-model`: Neuroscience: DrtNeuronModelSousaEtAl2014151949Model
- `neuroscience-other-dynamic-cortical-interlaminar-interactions-carra-150806-model`: Neuroscience: DynamicCorticalInterlaminarInteractionsCarra150806Model
- `neuroscience-other-dynamics-of-spike-initiation-prescott-et-al-2008-116123-model`: Neuroscience: DynamicsOfSpikeInitiationPrescottEtAl2008116123Model
- `neuroscience-other-ebneretal2019-ebneretal2019-model`: Neuroscience: Ebneretal2019Ebneretal2019Model

## Wiring Rationale
- Comparative (non-causal) mode: no direct causal links were created.

## Visualization Strategy
- Monitor-driven visualization is required for this space.
- State streams are routed into explicit monitor ports (`state_a..state_d`) to avoid signal overwrite.
- At minimum, monitor visuals include one timeseries panel and one summary table.
- Rationale: A dedicated monitor model receives all participating model state streams (`state_a..state_d`) so trajectories can be compared in one place without claiming causal coupling when IO semantics are incomplete.

## Expected Behaviors
- Model output trajectories under shared runtime settings.
- Cross-model agreement/divergence in key state or metric signals.
- Relative behavior comparison without causal linkage claims.

## Known Limitations
- No new biology is introduced beyond what upstream models encode.
- Cross-model semantic matching is rule-based and may under-connect uncertain routes.

## Source Provenance
- neuroscience-other-drt-neuron-model-sousa-et-al-2014-151949-model :: modeldb:151949 :: https://modeldb.science/151949
- neuroscience-other-dynamic-cortical-interlaminar-interactions-carra-150806-model :: modeldb:150806 :: https://modeldb.science/150806
- neuroscience-other-dynamics-of-spike-initiation-prescott-et-al-2008-116123-model :: modeldb:116123 :: https://modeldb.science/116123
- neuroscience-other-ebneretal2019-ebneretal2019-model :: opensourcebrain:EbnerEtAl2019 :: https://github.com/OpenSourceBrain/EbnerEtAl2019

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
