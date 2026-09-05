# ADR-0001 - Automation-First Fabric Development

## Status
Accepted

## Context
The learning environment is intended to develop Microsoft Fabric Solution Architect capability rather than only portal-based implementation skills.

## Options Considered

1. Create and configure all Fabric resources manually.
2. Automate everything immediately without first understanding the Fabric controls.
3. Understand important operations manually, then automate repeatable operations.

## Decision
Use option 3.

Manual operations will be used when they improve understanding or are appropriate for administration.

Repeatable provisioning, configuration and deployment will progressively use Fabric CLI, REST APIs, Git and CI/CD.

## Benefits
- Reproducibility
- Reduced manual configuration
- Better DEV/TEST/PROD consistency
- Source-controlled implementation
- Easier rollback
- Better auditability

## Risks
- Automation adds initial complexity.
- API and CLI capabilities can change.
- Not every Fabric setting is equally automatable.

## Revisit Trigger
Re-evaluate the automation method when Fabric deployment tooling, APIs or supported Git integration materially change.
