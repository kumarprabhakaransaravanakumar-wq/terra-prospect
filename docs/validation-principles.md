# Validation Principles

## Independent truth

The simulation harness owns hidden geology and higher-fidelity sensor behavior. Autonomous flight
logic receives observations only and cannot inspect the source map used for scoring.

## Model mismatch by design

Blind campaigns perturb sensor noise, bias, spatial support, environmental nuisance factors, and
resource geometry relative to onboard assumptions. This tests robustness rather than simulator
agreement.

## Mission-aligned metrics

Evaluation should include:

- resource-map error and uncertainty calibration;
- deposit detection recall and false discoveries;
- recoverable-resource estimate error;
- useful information gained per energy consumed;
- drill precision, recall, and calibration benefit;
- hard safety and keep-out constraint violations;
- graceful behavior under sensor, compute, power, and actuator faults.

## Escalating fidelity

Development progresses from unit and model tests through software-in-the-loop, recorded-data replay,
processor-in-the-loop, hardware-in-the-loop, and analogue field trials. Higher-fidelity tests do not
replace lower-level regression tests.

