# AIEO Governance

**Version:** 1.0.0  
**Status:** Approved
**Owner:** Organization Governance  
**Last Updated:** 2026-11-02

## 1. Purpose

Define how AIEO standards, Agent Definitions, Skills, Workflows, and releases are proposed, reviewed, approved, changed, and retired.

## 2. Governance principles

- Human accountability: AI Agents may execute delegated work but do not acquire business or organizational authority by default.
- Explicit ownership: every controlled artifact has an owner.
- Risk-proportionate control: approval depth is proportional to impact and risk.
- Traceability: material decisions and exceptions are recorded.
- Versioned evolution: changes are released as identifiable versions.
- Project autonomy within boundaries: projects may extend Organization standards but may not silently weaken mandatory controls.

## 3. Authority model

| Decision | Primary authority |
|---|---|
| Business goals, priority, scope trade-offs | Product Manager / authorized business stakeholder |
| System architecture and technical design | Solution Architect |
| Execution sequencing and coordination | Engineering Manager |
| Test strategy and QA acceptance evidence | QA Engineer |
| Code quality review | Code Reviewer |
| Security assessment | Security Engineer |
| Deployment engineering and operational readiness | DevOps Engineer |
| UAT acceptance | Human business stakeholder |
| Go-live authorization | Authorized human stakeholder |
| Acceptance of material residual risk | Authorized human risk owner |
| Organization-level policy approval | AIEO owner / designated human approver |

An Agent may recommend a decision outside its authority but must escalate rather than approve it.

## 4. Artifact lifecycle

1. Proposed
2. Under Review
3. Approved
4. Released
5. Deprecated
6. Retired

Approval of document content and saving/committing a file are separate events. A document must not be described as released merely because its content was discussed or approved.

## 5. Change classes

- **Editorial:** wording or formatting without changing meaning.
- **Minor:** additive clarification or compatible capability.
- **Major:** changes to role authority, mandatory gates, protocol behavior, compatibility, or security posture.

The AIEO owner determines the final version impact. Major changes require explicit human review.

## 6. Exceptions

An exception request must identify:
- Requirement being excepted.
- Business and technical rationale.
- Scope and affected projects.
- Risk assessment and compensating controls.
- Owner and expiry/review date.
- Human approver.

Exceptions must be time-bounded where practical. An Agent cannot approve an exception to its own task constraints.

## 7. Project adoption and upgrades

- New projects use the latest approved stable release unless explicitly pinned otherwise.
- Existing projects remain pinned to their adopted version.
- Upgrades are assessed and adopted deliberately.
- AIEO maintainers may flag urgent security or governance changes for mandatory project review.
- Upgrade impact must identify changed files, behavior, migration steps, and compatibility concerns.

## 8. Human oversight

Human review is mandatory for:
- Business decisions beyond delegated authority.
- Material architecture trade-offs when authority is not delegated.
- Significant security, privacy, compliance, financial, or operational risks.
- UAT acceptance.
- Go-live authorization.
- Material risk acceptance.
- Changes to Organization governance.

## 9. Evidence and auditability

Important approvals and execution outcomes should be traceable to:
- Work item or change identifier.
- Responsible human or Agent Role.
- Decision and rationale.
- Evidence reviewed.
- Date and version.
- Follow-up actions, where applicable.

## 10. Governance review

Review this policy at least when:
- AIEO undergoes a major release.
- A significant incident exposes a governance gap.
- Roles or authority boundaries change.
- New runtime capabilities materially change execution risk.
