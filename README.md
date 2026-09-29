# Azure Security Engineering

> Threat Intelligence · Threat Modeling · Threat Hunting · Detection Engineering for Microsoft Azure, Microsoft Sentinel, Microsoft Defender XDR and Microsoft Entra.

This repository is a practical security engineering knowledge base focused on turning Azure telemetry and threat intelligence into **attack hypotheses, hunts, detections, investigation playbooks and measurable coverage**.

## Mission

The repository is organized around the defensive intelligence lifecycle:

```text
Threat Intelligence
        ↓
Threat Modeling
        ↓
Hunting Hypotheses
        ↓
Detection Engineering
        ↓
Validation / Investigation
        ↓
Coverage & Feedback
        ↺
```

The goal is not to collect random KQL snippets. The goal is to maintain a traceable chain from **threat → behavior → telemetry → hunt → detection → response**.

## Repository map

| Area | Purpose |
|---|---|
| [threat-intelligence/](threat-intelligence/) | Intelligence requirements, actor/TTP tracking, IOC lifecycle and reporting |
| [threat-modeling/](threat-modeling/) | Azure attack surfaces, abuse cases, attack paths and ATT&CK mapping |
| [threat-hunting/](threat-hunting/) | Hypothesis-driven hunts and KQL investigations |
| [detection-engineering/](detection-engineering/) | Detection lifecycle, analytics logic, tuning and validation |
| [coverage/](coverage/) | ATT&CK coverage, telemetry dependencies and gap analysis |
| [playbooks/](playbooks/) | Investigation and triage procedures |
| [labs/](labs/) | Safe reproducible exercises for validating detections |
| [docs/](docs/) | Architecture, operating model and data-source guidance |
| [Sentinel/](Sentinel/) | Legacy material retained for reference |

## Core platforms

- Microsoft Sentinel
- Microsoft Defender XDR
- Microsoft Defender for Cloud
- Microsoft Entra ID
- Azure Monitor / Log Analytics
- Azure Activity Logs
- Microsoft Graph security telemetry where applicable

## Operating model

Every hunt or detection should document:

1. **Intelligence driver** — what threat, campaign, TTP or risk motivated the work.
2. **Threat scenario** — the behavior being modeled.
3. **ATT&CK mapping** — tactic / technique where applicable.
4. **Required telemetry** — tables, connectors and retention assumptions.
5. **KQL logic** — readable and scoped query logic.
6. **Expected signal** — what constitutes suspicious behavior.
7. **Known noise** — common benign causes.
8. **Validation** — how the logic was tested.
9. **Tuning** — exclusions and thresholds.
10. **Response path** — what an analyst should do next.

## Starter hunts

Current starter pack:

- Repeated failed Entra sign-ins by identity
- Rare privileged role assignment activity
- Azure resource operations by unusual callers
- High-severity Defender / Sentinel alert review

See [threat-hunting/kql/](threat-hunting/kql/).

## Detection quality principles

A detection is not considered useful merely because the query runs without syntax errors. It should be:

- **Relevant** — mapped to an explicit threat scenario.
- **Observable** — backed by available telemetry.
- **Explainable** — understandable by an analyst who did not write it.
- **Testable** — accompanied by a validation procedure.
- **Tunable** — noise sources and exclusions are documented.
- **Actionable** — the expected analyst response is clear.
- **Measurable** — coverage and operational outcomes can be reviewed.

## Current status

This repository is being rebuilt from a minimal Azure/Sentinel collection into a structured security engineering project.

### v0.1 — Foundation
- [x] Repository architecture
- [x] Threat intelligence workflow
- [x] Threat modeling workflow
- [x] Hunting workflow
- [x] Detection engineering lifecycle
- [x] Initial KQL starter pack
- [ ] Detection metadata standard
- [ ] Automated query validation

### v0.2 — Coverage
- [ ] MITRE ATT&CK Azure coverage matrix
- [ ] Telemetry dependency matrix
- [ ] Detection gap analysis
- [ ] Defender XDR advanced hunting pack
- [ ] Entra identity attack-path pack

### v0.3 — Operationalization
- [ ] Sentinel Analytics Rule templates
- [ ] Hunting → Detection promotion workflow
- [ ] CI checks for metadata and KQL
- [ ] Atomic / lab validation evidence
- [ ] Detection changelog and versioning
- [ ] GitHub Pages documentation

## Reference architecture

See [docs/architecture.md](docs/architecture.md).

## Official references

- Microsoft Sentinel: https://learn.microsoft.com/azure/sentinel/
- Microsoft Defender XDR Advanced Hunting: https://learn.microsoft.com/defender-xdr/advanced-hunting-overview
- Microsoft Defender for Cloud: https://learn.microsoft.com/azure/defender-for-cloud/
- Microsoft Entra monitoring: https://learn.microsoft.com/entra/identity/monitoring-health/
- MITRE ATT&CK: https://attack.mitre.org/

## Disclaimer

This repository is intended for defensive security research, authorized security operations, detection engineering and threat hunting in environments you own or are explicitly authorized to assess.
