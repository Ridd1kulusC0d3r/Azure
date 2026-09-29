# Azure Detection Coverage Matrix

This is a starter matrix. ATT&CK technique IDs should be added only after the behavior-to-technique mapping has been reviewed.

| Scenario | Domain | Telemetry | Hunt | Detection | Coverage |
|---|---|---|---|---|---|
| Concentrated failed sign-ins | Identity | SigninLogs | HUNT-001 | Planned | Hunt only |
| Privileged role-management activity | Identity / Privilege | AuditLogs | HUNT-002 | Planned | Hunt only |
| New control-plane caller | Azure control plane | AzureActivity | HUNT-003 | Planned | Hunt only |
| Repeated high-severity alerts | Sentinel / Defender | SecurityAlert / AlertInfo | HUNT-004 | Planned | Hunt only |
| Security logging modification | Security plane | AzureActivity / product audit | Planned | Planned | Research gap |
| Credential changes to applications | Identity / Secrets | AuditLogs | Planned | Planned | Research gap |

## Interpretation

The purpose of this table is not to manufacture a high coverage percentage. It is to make blind spots visible.

A scenario moves to **Covered** only after a detection has validation evidence.
