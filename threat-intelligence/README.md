# Threat Intelligence

Threat intelligence in this repository exists to drive collection, modeling, hunting and detection.

## Structure

- `intelligence-requirements.md` — what the team needs to know.
- `collection-plan.md` — where and how evidence is collected.
- `templates/intelligence-note.md` — standardized reporting.

## Intelligence workflow

```text
Requirement → Collection → Assessment → TTP extraction → Threat model → Hunt → Detection → Feedback
```

Prefer behavior and TTP intelligence over long-lived dependence on IOCs alone.
