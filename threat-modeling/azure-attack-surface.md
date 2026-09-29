# Azure Attack Surface Model

Use this document as the top-level model for deciding where threats, hunts and detections belong.

| Domain | Assets | Example threat themes | Primary telemetry |
|---|---|---|---|
| Identity | Users, service principals, managed identities | credential abuse, privilege escalation, persistence | SigninLogs, AuditLogs, Defender XDR |
| Privilege | Entra roles, Azure RBAC, PIM | unexpected assignment, role activation, excessive permissions | AuditLogs, AzureActivity |
| Control plane | ARM operations, subscriptions, resource groups | resource modification, security-control changes | AzureActivity |
| Secrets | Key Vault, application credentials, certificates | secret access, credential addition, key misuse | service diagnostic logs, AuditLogs |
| Compute | VMs, containers, app services | execution, persistence, lateral movement | Defender for Cloud / XDR, platform logs |
| Storage | Storage accounts, blobs, files | collection, exfiltration, public exposure | storage diagnostics, AzureActivity |
| Network | NSGs, firewalls, public IPs, private endpoints | exposure, policy changes, tunneling paths | AzureActivity, network telemetry |
| DevOps | repositories, pipelines, federated identities | token abuse, pipeline compromise, secret theft | platform audit logs |
| Security plane | Sentinel, Defender, logging configuration | defense evasion, alert suppression, visibility loss | AzureActivity, Sentinel / Defender telemetry |

## Modeling questions

For each domain:

1. What are the crown-jewel assets?
2. Which identities can change them?
3. Which trust boundaries exist?
4. Which operations materially change security posture?
5. Which actions are observable?
6. Which actions are only partially observable?
7. Which threat behaviors deserve continuous detection?
8. Which behaviors are better suited to hunting?
