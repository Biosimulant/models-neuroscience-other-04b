# COMBO_0069 - Neuroscience Hippocampal Circuits

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
- `neuroscience-other-chirp-stimulus-responses-in-a-morphologically-re-147578-model`: Neuroscience: ChirpStimulusResponsesInAMorphologicallyRe147578Model
- `neuroscience-other-cholinergic-modulation-shifts-response-ca1-pyramidal-cells-depolarizing-ramps-via-osb267599-model`: Neuroscience: Model267599267599Model
- `neuroscience-other-cholinergic-modulation-shifts-the-response-of-ca-267599-model`: Neuroscience: CholinergicModulationShiftsTheResponseOfCa267599Model
- `neuroscience-other-circadian-rhythmicity-shapes-astrocyte-morpholog-257027-model`: Neuroscience: CircadianRhythmicityShapesAstrocyteMorpholog257027Model

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
- neuroscience-other-chirp-stimulus-responses-in-a-morphologically-re-147578-model :: modeldb:147578 :: https://modeldb.science/147578
- neuroscience-other-cholinergic-modulation-shifts-response-ca1-pyramidal-cells-depolarizing-ramps-via-osb267599-model :: opensourcebrain:267599 :: https://github.com/OpenSourceBrain/267599
- neuroscience-other-cholinergic-modulation-shifts-the-response-of-ca-267599-model :: modeldb:267599 :: https://modeldb.science/267599
- neuroscience-other-circadian-rhythmicity-shapes-astrocyte-morpholog-257027-model :: modeldb:257027 :: https://modeldb.science/257027

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
