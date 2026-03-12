# OctoAcme Handoff Checklists

Refs: #5

## Purpose
Reduce ambiguity and dropped context at key handoff points in the delivery lifecycle. Each checklist names the primary owner and at least one person to consult.

---

## 1. Requirements → Development

**Primary owner:** Product Manager (PdM)  
**Consult:** UX Designer, Project Manager (PM)

Use this checklist before a feature is picked up by Developers. The goal is to ensure Developers have everything they need to implement without blocking questions.

- [ ] Problem statement and user story documented
- [ ] Acceptance criteria are written, reviewed, and unambiguous
- [ ] UX designs (wireframes or high-fidelity) linked or attached
- [ ] Non-functional requirements stated (performance, accessibility, security, scalability)
- [ ] Scope boundaries are explicit (what is **not** in scope)
- [ ] Target environments and infrastructure notes provided
- [ ] Dependencies on other teams or services identified and flagged
- [ ] Open questions resolved or tracked with owners

**Handoff signal:** Developer lead confirms all items are checked before the story is moved to "In Progress."

---

## 2. Development → QA

**Primary owner:** Developers (lead or assigned engineer)  
**Consult:** QA, UX Designer (for design validation)

Use this checklist when a feature is code-complete and ready for QA validation.

- [ ] All acceptance criteria implemented and self-verified by the developer
- [ ] PR merged and build is green in CI
- [ ] Test data prepared and shared (or instructions for generating it)
- [ ] Test environment URL and credentials provided (or confirmed available)
- [ ] Runbook for manual test steps provided for complex flows
- [ ] Known issues or limitations documented with severity ratings
- [ ] Environment-specific configuration or feature flags documented
- [ ] Unit and integration tests written and passing

**Handoff signal:** QA acknowledges receipt and moves the story to "In QA."

---

## 3. Release → Support

**Primary owner:** Release Manager  
**Consult:** Project Manager (PM), Developers

Use this checklist when a release is deployed to production. The goal is to ensure Support Specialists have the context they need to handle user issues immediately.

- [ ] Release notes shared with Support (user-facing language, not technical jargon)
- [ ] Known issues list shared with workarounds where available
- [ ] Monitoring dashboard links provided (errors, latency, alerts)
- [ ] On-call contact name and channel shared for the post-release window
- [ ] Escalation path documented (Support → Developer → Release Manager)
- [ ] Expected user impact and changed workflows highlighted
- [ ] Rollback status confirmed (is rollback still available? Until when?)
- [ ] Support ticket templates or FAQ entries updated for new features

**Handoff signal:** Support Specialist confirms receipt of the above and signals readiness in the agreed channel.

---

## Related docs
- [Release Manager Checklist](release-manager-checklist.md)
- [Role Responsibility Matrix](role-responsibility-matrix.md)
- [Roles & Personas](octoacme-roles-and-personas.md)
- [Release & Deployment Guide](octoacme-release-and-deployment.md)
