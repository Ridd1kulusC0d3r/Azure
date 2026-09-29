# Threat Hunting

Hunts are hypothesis-driven investigations, not a directory of copied KQL.

## Hunt lifecycle

1. Intelligence or threat-model trigger
2. Hypothesis
3. Required telemetry
4. Query
5. Analysis
6. Findings
7. Tuning
8. Promote, retire or continue

## Query folders

- `kql/identity/`
- `kql/azure-control-plane/`
- `kql/sentinel/`

Every production hunt should be linked to a threat scenario and ATT&CK technique where appropriate.
