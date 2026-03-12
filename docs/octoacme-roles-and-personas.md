# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## QA / Testing

### Role Summary
QA Engineers validate that delivered features meet acceptance criteria and quality standards. They own the test strategy, execute manual and automated tests, and act as the quality gate before release.

### Responsibilities
- Define and maintain the test strategy and test plans
- Write and execute functional, regression, and integration tests
- Report defects with clear reproduction steps and severity ratings
- Verify acceptance criteria and sign off on features before release
- Contribute to the Definition of Done

### Goals
- Ensure high product quality and reduced production defects
- Provide fast, reliable feedback loops to developers
- Protect users from regressions and unexpected behavior

### Typical Communication / Interactions
- Works closely with **Developers** during test-driven development and defect triage
- Partners with **PdM** to validate acceptance criteria and user stories
- Coordinates with **PM** on test scheduling and release readiness
- Hands off test results and known issues to the **Release Manager** before deployment

---

## UX Designer

### Role Summary
UX Designers ensure that features are usable, accessible, and aligned with user needs. They translate product requirements into designs and validate those designs with users before and after development.

### Responsibilities
- Conduct user research and translate findings into design decisions
- Create wireframes, prototypes, and high-fidelity designs
- Define UX acceptance criteria and usability standards
- Review implemented features for design fidelity and accessibility
- Collaborate on design systems and component libraries

### Goals
- Deliver intuitive, accessible experiences that meet user needs
- Reduce rework caused by unclear or late design decisions
- Ensure design consistency across the product

### Typical Communication / Interactions
- Works with **PdM** to understand requirements and user goals before starting design
- Hands off designs and acceptance criteria to **Developers** before implementation begins
- Partners with **QA** on usability testing and accessibility validation
- Communicates design decisions and rationale to **PM** to keep timelines realistic

---

## Release Manager

### Role Summary
Release Managers coordinate and own the end-to-end release process. They ensure releases are planned, tested, communicated, and deployed safely while minimizing risk to production.

### Responsibilities
- Own and maintain the release calendar and deployment schedule
- Coordinate pre-release sign-off across QA, Developers, and Security Lead
- Draft and distribute release notes and stakeholder communications
- Enforce the release checklist and manage go/no-go decisions
- Lead rollback decisions and post-release monitoring

### Goals
- Deliver predictable, low-risk releases on schedule
- Ensure all stakeholders are informed before and after deployment
- Reduce production incidents caused by release process gaps

### Typical Communication / Interactions
- Coordinates with **PM** on release scheduling and scope confirmation
- Works with **Developers** to finalize build artifacts and packaging
- Receives QA sign-off and known-issues list from **QA** before go/no-go
- Collaborates with **DevOps Engineer** on pipeline readiness and deployment execution
- Hands off release notes and monitoring context to **Support Specialist** post-deploy

---

## DevOps Engineer

### Role Summary
DevOps Engineers maintain the infrastructure and automation pipelines that enable reliable, repeatable delivery. They bridge development and operations to improve deployment frequency and system reliability.

### Responsibilities
- Design, build, and maintain CI/CD pipelines and deployment automation
- Manage environment consistency across dev, staging, and production
- Monitor system health, alerts, and SLOs post-deployment
- Advise on infrastructure needs and capacity planning
- Implement and enforce infrastructure security controls

### Goals
- Maximize deployment reliability and reduce mean time to recovery (MTTR)
- Eliminate manual, error-prone deployment steps through automation
- Ensure environment parity to reduce "works on my machine" issues

### Typical Communication / Interactions
- Partners with **Developers** to integrate new services and automate workflows
- Coordinates with **Release Manager** on deployment windows and pipeline status
- Works with **Security Lead** to implement security scanning in the pipeline
- Reports environment and infrastructure issues to **PM** for risk tracking

---

## Security Lead

### Role Summary
The Security Lead owns application and infrastructure security across the delivery lifecycle. They identify risks early, run security reviews, and ensure compliance with security policies.

### Responsibilities
- Conduct threat modeling and security reviews for new features and architecture changes
- Maintain and update the risk register with security findings
- Define secure coding standards and conduct developer training
- Coordinate incident response for security events
- Review and approve security controls in the CI/CD pipeline

### Goals
- Prevent security vulnerabilities from reaching production
- Build a security-aware culture across the delivery team
- Ensure compliance with relevant standards and regulations

### Typical Communication / Interactions
- Engages with **Developers** and **QA** to promote secure coding practices and security test coverage
- Escalates high-severity risks to **PM** for prioritization and decision-making
- Partners with **Release Manager** on go/no-go decisions when security findings are outstanding
- Advises **DevOps Engineer** on pipeline security controls and secrets management

---

## Support Specialist

### Role Summary
Support Specialists serve as the first point of contact for user issues after a release. They triage incoming requests, escalate complex issues, and feed user feedback back into the product process.

### Responsibilities
- Triage and resolve user-reported issues in line with SLA commitments
- Document common issues and maintain the support knowledge base
- Escalate defects and bugs to the development team with clear context
- Participate in retrospectives to represent user and support perspectives
- Monitor support queues after releases and flag elevated ticket volumes

### Goals
- Resolve user issues quickly to maintain trust and satisfaction
- Reduce repeat issues by feeding learnings back to the development cycle
- Ensure smooth handoffs from the release team at deployment time

### Typical Communication / Interactions
- Receives release notes, known issues, and on-call contacts from **Release Manager** at deployment
- Reports user-facing defects to **Developers** with reproduction steps and log context
- Provides product usage and pain-point feedback to **PdM**
- Updates **PM** on support ticket volumes and escalation trends

---

## How these personas interact

The following examples illustrate common handoffs between personas during a typical delivery cycle:

1. **PdM → UX Designer**: PdM shares requirements and user research; UX Designer returns wireframes and acceptance criteria for review.
2. **UX Designer → Developers**: UX Designer hands off finalized designs, component specs, and UX acceptance criteria; Developers implement and flag technical constraints early.
3. **Developers → QA**: Developers signal feature completion; QA validates against acceptance criteria and returns a defect list or sign-off.
4. **QA → Release Manager**: QA provides a test summary, pass/fail status, and known issues; Release Manager uses this for the go/no-go decision.
5. **Release Manager → DevOps Engineer**: Release Manager confirms scope and window; DevOps Engineer executes the pipeline and reports deployment status.
6. **Release Manager → Support Specialist**: Release Manager shares release notes, known issues, monitoring links, and on-call contacts so Support is ready at go-live.
7. **Support Specialist → PdM / PM**: Support Specialist surfaces recurring user issues and feedback to inform the next planning cycle.

See also:
- [Role Responsibility Matrix](role-responsibility-matrix.md) for a full RACI view across all roles and activities.
- [Release Manager Checklist](release-manager-checklist.md) for step-by-step release process guidance.
- [Handoff Checklists](handoff-checklists.md) for artifact checklists at each major handoff point.

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

