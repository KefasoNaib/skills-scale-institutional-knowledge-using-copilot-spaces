# OctoAcme Role Responsibility Matrix

Refs: #5

## Purpose
Provide a compact RACI-style reference that makes ownership and collaboration explicit for key project activities across all OctoAcme roles.

## How to use this matrix

| Code | Meaning |
|------|---------|
| **R** | **Responsible** — does the work |
| **A** | **Accountable** — owns the outcome; final decision-maker |
| **C** | **Consulted** — provides input before or during the activity |
| **I** | **Informed** — kept up to date on progress or outcome |

- Each activity should have exactly one **A** (accountable) owner.
- More than one role can share **R** (responsible).
- Consult this matrix at the start of a project or sprint to align ownership.
- Review and adjust with your team before finalizing — add a comment or open an issue if any mapping is unclear.

## Matrix

| Activity | PdM | PM | Developers | QA | UX Designer | Release Manager | DevOps Engineer | Security Lead | Support Specialist | Stakeholders |
|----------|-----|----|------------|----|-------------|-----------------|-----------------|---------------|--------------------|--------------|
| Define requirements | **A** | C | C | C | C | I | I | C | I | C |
| Prioritize backlog | **A** | C | C | I | C | I | I | C | C | I |
| Design UX | C | I | C | C | **A** | I | I | I | I | I |
| Implement feature | C | I | **A/R** | C | C | I | C | C | I | I |
| Write tests | I | I | R | **A** | I | I | I | C | I | I |
| Code review | I | I | **A/R** | C | I | I | C | C | I | I |
| Security review | C | C | C | C | I | C | C | **A** | I | I |
| CI/CD pipeline changes | I | I | C | I | I | C | **A** | C | I | I |
| Create release notes | I | C | C | C | I | **A** | I | I | C | I |
| Approve release (go/no-go) | C | C | C | C | I | **A** | C | C | I | I |
| Post-release support / triage | I | I | C | C | I | C | C | C | **A** | I |
| Run retrospective actions | I | **A** | R | R | R | R | R | R | R | I |

> **Note:** This matrix reflects a typical team configuration. Adjust role assignments based on your team size, structure, and project context.

## Related docs
- [Roles & Personas](octoacme-roles-and-personas.md)
- [Release Manager Checklist](release-manager-checklist.md)
- [Handoff Checklists](handoff-checklists.md)
