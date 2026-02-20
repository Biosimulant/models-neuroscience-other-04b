# COMBO_0039 - Neuroscience General

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
- `neuroscience-other-cn-bushy-stellate-neurons-osb37857-model`: Neuroscience: Model3785737857Model
- `neuroscience-other-cn-bushy-stellate-neurons-rothman-manis-2003-bri-126899-model`: Neuroscience: CnBushyStellateNeuronsRothmanManis2003Bri126899Model
- `neuroscience-other-cn-bushy-stellate-neurons-rothman-manis-2003-bri-231238-model`: Neuroscience: CnBushyStellateNeuronsRothmanManis2003Bri231238Model

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
- neuroscience-other-cn-bushy-stellate-neurons-osb37857-model :: opensourcebrain:37857 :: https://github.com/OpenSourceBrain/37857
- neuroscience-other-cn-bushy-stellate-neurons-rothman-manis-2003-bri-126899-model :: modeldb:126899 :: https://modeldb.science/126899
- neuroscience-other-cn-bushy-stellate-neurons-rothman-manis-2003-bri-231238-model :: modeldb:231238 :: https://modeldb.science/231238

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
