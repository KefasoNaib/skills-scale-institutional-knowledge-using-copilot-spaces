# OctoAcme Release Manager Checklist

Refs: #5

## Purpose
Provide the Release Manager with a step-by-step checklist covering pre-release sign-off, deployment, stakeholder communications, and post-release monitoring.

See also: [Release & Deployment Guide](octoacme-release-and-deployment.md) for release types, rollback playbook, and release notes template.

---

## 1. Pre-release sign-off

### Scope confirmation
- [ ] Release scope is confirmed with PM and PdM (no last-minute additions without explicit approval)
- [ ] All acceptance criteria are met and PRs are merged to the release branch
- [ ] Feature flags are configured correctly for this release

### Quality gate
- [ ] QA sign-off received — test summary reviewed and accepted
- [ ] Known issues list reviewed; each item has a severity rating and decision (ship / hold / workaround)
- [ ] CI pipeline is green (build, unit tests, integration tests)
- [ ] Security scan results reviewed with Security Lead; no open critical or high findings without a documented exception

### Release artifacts
- [ ] Release notes drafted and reviewed by PM and PdM
- [ ] Rollback plan documented and reviewed (who triggers it, how, and within what timeframe)
- [ ] Smoke test suite identified and owners confirmed
- [ ] Deployment runbook (or automated pipeline) reviewed and up to date

### Stakeholder communications
- [ ] Deployment window communicated to impacted teams and stakeholders
- [ ] Maintenance window or downtime notice sent (if applicable)
- [ ] Support Specialist briefed: release notes, known issues, monitoring links, and on-call contact provided

---

## 2. Go / No-go decision

- [ ] QA: signed off ✅ / not signed off ❌
- [ ] Security Lead: no blocking findings ✅ / blocking findings ❌
- [ ] DevOps Engineer: pipeline and environment ready ✅ / not ready ❌
- [ ] PM: scope confirmed ✅ / scope concerns ❌
- [ ] Release Manager decision: **Go** / **No-go** — _record rationale if No-go_

> **Rule:** A single ❌ from any required sign-off delays the release unless the Release Manager explicitly documents and accepts the risk.

---

## 3. Deployment

- [ ] Deployment window started; team notified in the agreed channel
- [ ] Backup or snapshot taken (if applicable)
- [ ] Deployed to staging; smoke tests executed and passed
- [ ] Production deployment triggered (automated pipeline preferred)
- [ ] Post-deploy verifications complete (health checks, critical user journeys)
- [ ] Deployment window closed; status communicated to stakeholders

---

## 4. Post-release monitoring

- [ ] Monitoring dashboards checked within 30 minutes of deployment (error rates, latency, alerts)
- [ ] Support ticket queue monitored for elevated volume in the first hour
- [ ] On-call rotation confirmed and contacts are reachable
- [ ] Any new incidents logged, triaged, and assigned within SLA
- [ ] Rollback criteria evaluated — see the [Rollback criteria reference](#rollback-criteria-reference) table below

---

## 5. Release wrap-up

- [ ] Final release notes published to the agreed channel or changelog
- [ ] Post-release support handoff confirmed with Support Specialist (see [Handoff Checklists](handoff-checklists.md))
- [ ] Retrospective notes updated with any release process issues
- [ ] Release record stored in the project repo

---

## Rollback criteria reference

| Condition | Recommended Action |
|-----------|-------------------|
| Critical user journey failure | Immediate rollback |
| Error rate > agreed threshold | Rollback within agreed window |
| Security incident detected | Engage Security Lead; consider rollback |
| Elevated support volume (non-critical) | Monitor; escalate if sustained |
| Minor known issue already documented | No rollback; ship workaround |
