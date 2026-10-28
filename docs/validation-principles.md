# Validation Principles

## Claims must match the evidence

The three outputs have different scientific meanings and validation requirements:

- **Habitability and biosignature potential** identifies evidence relevant to environments that
  could support or preserve life, or to candidate biosignatures. It does not prove life exists.
- **Resource potential** identifies candidate materials under declared detectability, value, and
  accessibility assumptions. It is not a mineral reserve estimate.
- **Landing suitability** identifies evidence relevant to a declared vehicle and operating envelope.
  It is not landing certification.

## Independent references

Scientific evaluation must use withheld scenes, independent reference products, laboratory or field
measurements, or higher-confidence labels appropriate to each goal. A model cannot establish its
validity by agreeing with features produced by the same model family.

## Sensor availability is a test dimension

The pipeline must be evaluated with:

- one sensor, complementary combinations, and deliberately redundant combinations;
- missing bands, gaps, no-data regions, and partial coverage;
- invalid or incomplete calibration and geometry metadata;
- contradictory modalities and shared systematic errors;
- changes in spatial resolution, viewing geometry, illumination, and noise;
- instruments, missions, terrain classes, and planetary bodies absent from model development.

## Uncertainty and abstention

A useful uncertainty estimate must distinguish known evidence, missing evidence, model uncertainty,
measurement noise, and shared systematics. Coverage must not be confused with confidence. When a
plugin's prerequisites or applicability conditions are unmet, it should abstain rather than emit an
apparently precise score.

Uncertainty should be tested for calibration, not just used as a ranking value. Confidence intervals
or probabilities must be checked against observed frequencies on withheld evaluation data.

## Goal-aligned metrics

Evaluation should include:

- uncertainty calibration and spatial coverage;
- precision/recall or ranking performance for independently defined target phenomena;
- false discoveries and false exclusions at decision-relevant thresholds;
- improvement contributed by each modality and combination;
- degradation under sensor removal and metadata corruption;
- consistency across instruments, missions, resolutions, and planetary bodies;
- processing cost, memory, latency, and reproducibility;
- frequency and correctness of insufficiency or abstention decisions.

Goal-specific scientific metrics and reference standards must be declared before release acceptance.

## Provenance and reproducibility

Every derived product should retain source asset identifiers and digests, calibration and geometry,
quality masks, coordinate transformations, plugin and model versions, feature lineage, uncertainty
assumptions, and the selection policy that produced the recommendation.

## Escalating fidelity

Development progresses from unit and synthetic contract tests through recorded real-data replay,
cross-mission evaluation, processor-in-the-loop, hardware-in-the-loop, and field or analogue
validation where relevant. Higher-fidelity tests complement rather than replace deterministic
regression tests.
