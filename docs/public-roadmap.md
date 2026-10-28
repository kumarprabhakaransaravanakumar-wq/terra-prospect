# Public Roadmap

## Phase 1 — Sensor-agnostic contract and selection PoC

- Represent any planetary body, declared map grid, and available sensor collection.
- Define goal-specific evidence with validity, uncertainty, quality, provenance, and model version.
- Rank single sensors and multimodal combinations independently for habitability/biosignature,
  resource, and landing goals.
- Demonstrate deterministic behavior for missing sensors, unknown cells, shared systematics, and
  processing-cost tradeoffs.

**Status:** initial executable contract and synthetic demonstration implemented privately.

## Phase 2 — Real archive vertical slice

- Ingest one remotely windowed, publicly available planetary product through a traceable adapter.
- Preserve mission calibration, observation geometry, quality masks, coordinate reference, units,
  acquisition metadata, and source digest.
- Implement one scientifically bounded modality plugin per goal.
- Produce maps, uncertainty, abstentions, provenance, and a combination recommendation without a
  bulk archive download.

## Phase 3 — Multimodal and cross-mission evidence

- Add co-registration and resolution-aware fusion across complementary instruments.
- Represent correlated errors rather than counting repeated or derived measurements independently.
- Run sensor-removal, conflicting-evidence, coverage, and degraded-metadata ablations.
- Test transfer across instruments, missions, terrain classes, and planetary bodies.

## Phase 4 — Decision-quality validation

- Calibrate uncertainty on withheld scenes and independent reference products.
- Define goal-specific acceptance metrics and explicit insufficiency/abstention thresholds.
- Validate landing outputs against declared vehicle constraints and appropriate-resolution hazards.
- Distinguish resource indications from accessibility and reserve claims.
- Distinguish habitability or candidate-biosignature evidence from confirmation of life.

## Phase 5 — Operational and downstream integration

- Measure streaming and windowed-processing performance on representative compute.
- Add reproducible data-cube packaging and signed provenance manifests.
- Integrate flyover products with surface route planning, targeted sensing, or rover prospecting.
- Progress through recorded-data replay, processor-in-the-loop, hardware-in-the-loop, and analogue
  validation where justified.

Only disclosure-safe milestones and results will be mirrored into this public repository.
