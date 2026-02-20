# COMBO_0061 - Neuroscience Basal Ganglia Dopamine

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
- `neuroscience-other-d2-dopamine-receptor-modulation-of-interneuronal-98005-model`: Neuroscience: D2DopamineReceptorModulationOfInterneuronal98005Model
- `neuroscience-other-dbs-of-a-multi-compartment-model-of-subthalamic-151460-model`: Neuroscience: DbsOfAMultiCompartmentModelOfSubthalamic151460Model
- `neuroscience-other-differential-modulation-of-pattern-and-rate-in-a-84612-model`: Neuroscience: DifferentialModulationOfPatternAndRateInA84612Model
- `neuroscience-other-dopamine-activation-of-signaling-pathways-in-a-m-154968-model`: Neuroscience: DopamineActivationOfSignalingPathwaysInAM154968Model

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
- neuroscience-other-d2-dopamine-receptor-modulation-of-interneuronal-98005-model :: modeldb:98005 :: https://modeldb.science/98005
- neuroscience-other-dbs-of-a-multi-compartment-model-of-subthalamic-151460-model :: modeldb:151460 :: https://modeldb.science/151460
- neuroscience-other-differential-modulation-of-pattern-and-rate-in-a-84612-model :: modeldb:84612 :: https://modeldb.science/84612
- neuroscience-other-dopamine-activation-of-signaling-pathways-in-a-m-154968-model :: modeldb:154968 :: https://modeldb.science/154968

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
