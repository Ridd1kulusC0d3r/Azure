# Detection Engineering

The purpose of this section is to turn validated threat hypotheses into maintainable detection content.

## Lifecycle

```text
Threat → Model → Hunt → Validate → Detection → Tune → Measure → Review
```

## Required metadata

Every detection should contain:

- ID
- title
- description
- data source
- query
- ATT&CK mapping
- severity rationale
- known false positives
- investigation guidance
- validation evidence
- owner
- version
- last reviewed date

See [detection-lifecycle.md](detection-lifecycle.md).
