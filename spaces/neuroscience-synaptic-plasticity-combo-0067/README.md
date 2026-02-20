# COMBO_0067 - Neuroscience Synaptic Plasticity

## Scientific Question
How do synaptic changes influence network-level outcomes?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-effect-of-the-initial-synaptic-state-on-the-prob-157339-model`: Neuroscience: EffectOfTheInitialSynapticStateOnTheProb157339Model
- `neuroscience-other-effects-of-chloride-accumulation-and-diffusion-o-148253-model`: Neuroscience: EffectsOfChlorideAccumulationAndDiffusionO148253Model
- `neuroscience-other-effects-of-synaptic-location-and-timing-on-synap-116981-model`: Neuroscience: EffectsOfSynapticLocationAndTimingOnSynap116981Model
- `neuroscience-other-electrically-coupled-retzius-neurons-vazquez-et-120910-model`: Neuroscience: ElectricallyCoupledRetziusNeuronsVazquezEt120910Model

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
- neuroscience-other-effect-of-the-initial-synaptic-state-on-the-prob-157339-model :: modeldb:157339 :: https://modeldb.science/157339
- neuroscience-other-effects-of-chloride-accumulation-and-diffusion-o-148253-model :: modeldb:148253 :: https://modeldb.science/148253
- neuroscience-other-effects-of-synaptic-location-and-timing-on-synap-116981-model :: modeldb:116981 :: https://modeldb.science/116981
- neuroscience-other-electrically-coupled-retzius-neurons-vazquez-et-120910-model :: modeldb:120910 :: https://modeldb.science/120910

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
