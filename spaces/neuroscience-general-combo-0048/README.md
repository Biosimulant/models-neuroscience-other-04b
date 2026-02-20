# COMBO_0048 - Neuroscience General

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
- `neuroscience-other-comparison-of-da-based-stochastic-algorithms-pez-167772-model`: Neuroscience: ComparisonOfDaBasedStochasticAlgorithmsPez167772Model
- `neuroscience-other-compartmental-model-of-a-mitral-cell-popovic-et-53435-model`: Neuroscience: CompartmentalModelOfAMitralCellPopovicEt53435Model
- `neuroscience-other-compartmental-models-of-growing-neurites-graham-59582-model`: Neuroscience: CompartmentalModelsOfGrowingNeuritesGraham59582Model

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
- neuroscience-other-comparison-of-da-based-stochastic-algorithms-pez-167772-model :: modeldb:167772 :: https://modeldb.science/167772
- neuroscience-other-compartmental-model-of-a-mitral-cell-popovic-et-53435-model :: modeldb:53435 :: https://modeldb.science/53435
- neuroscience-other-compartmental-models-of-growing-neurites-graham-59582-model :: modeldb:59582 :: https://modeldb.science/59582

## How to Run
```bash
python run_local.py --duration auto --tick-dt auto
```

## How to Interpret Outputs
Use output trajectories and summary metrics to compare mechanistic consistency across constituent models.
Interpret comparative spaces as non-causal side-by-side simulation views.
