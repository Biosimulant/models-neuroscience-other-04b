# COMBO_0060 - Neuroscience Basal Ganglia Dopamine

## Scientific Question
How do basal ganglia dopamine mechanisms compare across these models?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-comparison-full-reduced-globus-pallidus-models-osb127728-model`: Neuroscience: Model127728127728Model
- `neuroscience-other-comparison-of-full-and-reduced-globus-pallidus-m-127728-model`: Neuroscience: ComparisonOfFullAndReducedGlobusPallidusM127728Model
- `neuroscience-other-composite-spiking-network-neural-field-model-of-147366-model`: Neuroscience: CompositeSpikingNetworkNeuralFieldModelOf147366Model
- `neuroscience-other-composite-spiking-network-neural-field-parkinsons-osb147366-model`: Neuroscience: Model147366147366Model

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
- neuroscience-other-comparison-full-reduced-globus-pallidus-models-osb127728-model :: opensourcebrain:127728 :: https://github.com/OpenSourceBrain/127728
- neuroscience-other-comparison-of-full-and-reduced-globus-pallidus-m-127728-model :: modeldb:127728 :: https://modeldb.science/127728
- neuroscience-other-composite-spiking-network-neural-field-model-of-147366-model :: modeldb:147366 :: https://modeldb.science/147366
- neuroscience-other-composite-spiking-network-neural-field-parkinsons-osb147366-model :: opensourcebrain:147366 :: https://github.com/OpenSourceBrain/147366

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
