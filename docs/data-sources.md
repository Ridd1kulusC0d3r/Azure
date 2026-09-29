# Azure Security Data Sources

This file is the telemetry inventory for hunts and detections.

| Domain | Example telemetry | Typical use |
|---|---|---|
| Identity | SigninLogs, AuditLogs | Authentication, role and directory activity |
| Azure control plane | AzureActivity | Resource changes and administrative operations |
| Defender XDR | Advanced Hunting tables | Endpoint, identity, email, cloud app and alert correlation |
| Sentinel | SecurityAlert, SecurityIncident | Detection and incident context |
| Defender for Cloud | Alerts / recommendations | Cloud workload and posture context |

## Rule

Each hunt must declare the exact tables it expects. Queries without documented telemetry dependencies are demos, not operational detections.

## Schema drift

Microsoft security schemas evolve. Validate field names in the target tenant before promoting a query into production.
