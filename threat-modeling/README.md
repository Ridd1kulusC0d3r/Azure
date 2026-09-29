# Threat Modeling

This section turns intelligence into Azure-specific threat scenarios.

## Model

For every scenario document:

```text
Asset → Trust boundary → Adversary objective → Preconditions → Technique → Observable behavior → Detection opportunity → Response
```

## Primary domains

- Identity and privileged access
- Azure control plane
- Compute and workloads
- Storage and secrets
- Networking
- CI/CD and workload identities
- Security tooling and logging

See [threat-scenario-template.md](threat-scenario-template.md).
