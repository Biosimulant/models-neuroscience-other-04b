# COMBO_0064 - Neuroscience Basal Ganglia Dopamine

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
- `neuroscience-other-dopamine-activation-of-signaling-pathways-in-a-m-154968-model`: Neuroscience: DopamineActivationOfSignalingPathwaysInAM154968Model
- `neuroscience-other-dopamine-modulated-medium-spiny-neuron-reduced-m-128818-model`: Neuroscience: DopamineModulatedMediumSpinyNeuronReducedM128818Model
- `neuroscience-other-dopaminergic-cell-bursting-model-kuznetsov-et-al-64285-model`: Neuroscience: DopaminergicCellBurstingModelKuznetsovEtAl64285Model
- `neuroscience-other-dynamic-dopamine-modulation-in-the-basal-ganglia-79488-model`: Neuroscience: DynamicDopamineModulationInTheBasalGanglia79488Model

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
- neuroscience-other-dopamine-activation-of-signaling-pathways-in-a-m-154968-model :: modeldb:154968 :: https://modeldb.science/154968
- neuroscience-other-dopamine-modulated-medium-spiny-neuron-reduced-m-128818-model :: modeldb:128818 :: https://modeldb.science/128818
- neuroscience-other-dopaminergic-cell-bursting-model-kuznetsov-et-al-64285-model :: modeldb:64285 :: https://modeldb.science/64285
- neuroscience-other-dynamic-dopamine-modulation-in-the-basal-ganglia-79488-model :: modeldb:79488 :: https://modeldb.science/79488

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
