# Operating Model

## Intake

New work can originate from:

- external threat intelligence
- incident findings
- threat modeling
- red / purple team observations
- telemetry changes
- detection gaps
- analyst hunting findings

## Decision path

```text
Is the behavior relevant?
  └─ no → document / close
  └─ yes
      ↓
Can we observe it?
  └─ no → telemetry gap
  └─ yes
      ↓
Can we hunt it reliably?
  └─ no → research / enrichment
  └─ yes
      ↓
Is the signal stable enough to automate?
  └─ no → keep as hunt
  └─ yes → detection candidate
```

## Review cadence

High-value detections should be reviewed when:

- source schemas change
- telemetry connectors change
- major threat intelligence changes
- false-positive rate materially increases
- analyst workflow changes
- the detection has not fired for an unexpectedly long period
