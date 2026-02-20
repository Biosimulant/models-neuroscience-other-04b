# COMBO_0058 - Neuroscience General

## Scientific Question
How do general mechanisms compare across these models?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-demirtasetal19-demirtasetal19-model`: Neuroscience: Demirtasetal19Demirtasetal19Model
- `neuroscience-other-dendritic-na-inactivation-drives-a-decrease-in-i-59480-model`: Neuroscience: DendriticNaInactivationDrivesADecreaseInI59480Model
- `neuroscience-other-dendritic-na-spike-initiation-and-backpropagatio-124394-model`: Neuroscience: DendriticNaSpikeInitiationAndBackpropagatio124394Model
- `neuroscience-other-dendritic-signals-command-firing-dynamics-in-a-c-147218-model`: Neuroscience: DendriticSignalsCommandFiringDynamicsInAC147218Model

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
- neuroscience-other-demirtasetal19-demirtasetal19-model :: opensourcebrain:DemirtasEtAl19 :: https://github.com/OpenSourceBrain/DemirtasEtAl19
- neuroscience-other-dendritic-na-inactivation-drives-a-decrease-in-i-59480-model :: modeldb:59480 :: https://modeldb.science/59480
- neuroscience-other-dendritic-na-spike-initiation-and-backpropagatio-124394-model :: modeldb:124394 :: https://modeldb.science/124394
- neuroscience-other-dendritic-signals-command-firing-dynamics-in-a-c-147218-model :: modeldb:147218 :: https://modeldb.science/147218

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
