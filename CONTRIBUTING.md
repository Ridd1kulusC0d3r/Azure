# Contributing

Contributions should improve defensive security engineering quality rather than increase query count for its own sake.

## Adding a hunt

Include:

- hypothesis
- intelligence or threat-model driver
- required telemetry
- KQL
- ATT&CK mapping where applicable
- expected output
- known noise
- analyst next step

## Adding a detection

Use `detection-engineering/templates/detection.md`.

A detection PR should demonstrate:

- telemetry exists
- query was tested
- thresholds are justified
- known false positives are documented
- investigation guidance exists
- ATT&CK mapping is defensible

## KQL style

- Use explicit time windows.
- Prefer readable intermediate variables for complex logic.
- Avoid unnecessary wide projections.
- Comment assumptions and tenant-specific thresholds.
- Treat schema names as environment-dependent until validated.
