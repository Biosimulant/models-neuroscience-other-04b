# COMBO_0078 - Neuroscience Hippocampal Circuits

## Scientific Question
How do recurrent hippocampal motifs shape network dynamics over time?

## Biological Context
Neuronal dynamics, network signaling, and emergent circuit behavior.

## Mechanistic Assumptions
- Model implementations are used as published in their curated manifests without biological reinterpretation.
- Time integration uses a shared global tick compatible with model min_dt constraints.
- Comparative (non-causal) mode is used because full deterministic IO coverage for causal coupling was not satisfied.

## Why These Models Belong Together
The combination was selected from a shared domain/theme bucket with deterministic compatibility checks.
- `neuroscience-other-communitymodellingca1-communitymodellingca1-model`: Neuroscience: Communitymodellingca1Communitymodellingca1Model
- `neuroscience-other-compartmental-differences-camp-signaling-pathways-hippocam-osb245529-model`: Neuroscience: Model245529245529Model
- `neuroscience-other-compartmental-differences-in-camp-signaling-path-245529-model`: Neuroscience: CompartmentalDifferencesInCampSignalingPath245529Model
- `neuroscience-other-complex-ca1-neuron-study-ap-initiation-osb123927-model`: Neuroscience: Model123927123927Model

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
- neuroscience-other-communitymodellingca1-communitymodellingca1-model :: opensourcebrain:CommunityModellingCA1 :: https://github.com/OpenSourceBrain/CommunityModellingCA1
- neuroscience-other-compartmental-differences-camp-signaling-pathways-hippocam-osb245529-model :: opensourcebrain:245529 :: https://github.com/OpenSourceBrain/245529
- neuroscience-other-compartmental-differences-in-camp-signaling-path-245529-model :: modeldb:245529 :: https://modeldb.science/245529
- neuroscience-other-complex-ca1-neuron-study-ap-initiation-osb123927-model :: opensourcebrain:123927 :: https://github.com/OpenSourceBrain/123927

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
