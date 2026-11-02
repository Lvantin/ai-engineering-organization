# AI Engineering Organization (AIEO) — Organization Layer

**Release:** 1.0.0  
**Status:** Official baseline release  
**Release date:** 2026-11-02  
**Package scope:** Organization Layer companion package

## 1. Purpose

This release establishes the reusable Organization Layer baseline for AIEO: governance, role-based Agent Definitions, operating protocols, engineering standards, Skills, workflows, templates, quality controls, runtime adapter guidance, and machine-readable registries.

It is designed to be merged with these three foundational documents, whose content was agreed separately and is intentionally not reconstructed or overwritten in this package:
- `organization/vision.md`
- `organization/operating-model.md`
- `organization/roles-and-responsibilities.md`

**Release prerequisite:** the three foundational documents must exist in the target repository. This ZIP is the companion package, not a self-contained replacement for those files.

## 2. Installation

1. Verify that the three foundational documents above are present in the repository.
2. Extract the `AIEO_Organization_Layer/` contents into the repository root, merging the `organization/` directory.
3. Review the release notes and changelog.
4. Keep project-specific context, source code, credentials, and runtime configuration outside this Organization package.

Do not overwrite the three foundational documents with reconstructed copies. This release does not claim that the target repository has been updated or committed.

## 3. Package contents

| Group | Files | Purpose |
|---|---:|---|
| Root documentation | 3 | Package guide, release notes, and file inventory |
| Governance | 1 | Authority, approvals, exceptions, risk acceptance, version control |
| Agent Definitions | 12 | One reusable definition for each approved Role |
| Protocols | 3 | Agent instantiation/delegation, context management, engineering change |
| Standards | 9 | Project context, architecture, coding, contracts, data, documentation, security, supply chain, configuration |
| Skills | 9 | Skills catalog plus eight reusable capability definitions |
| Workflows | 6 | Onboarding, Feature 0, Feature delivery, release, incident, organization release |
| Templates | 8 | Standard project and engineering work artifacts |
| Quality | 4 | Quality model, gates, test strategy, evidence and metrics |
| Integrations | 2 | Runtime adapter model and Claude Code adapter design |
| Configuration | 2 | Organization manifest and Role registry |
| Versioning | 2 | Changelog and release checklist |
| **Total** | **61** | **Files in this ZIP** |

## 4. Core design rules

1. Roles are stable organizational responsibilities; Skills are reusable capabilities.
2. Technology stack is selected at Project/Application/Service level, not hard-coded into a Role.
3. Agent Instances are created on demand from approved Agent Definitions.
4. An Engineering Manager coordinates work but does not replace Product Manager, Solution Architect, QA, Code Reviewer, Security Engineer, or human approval authority.
5. Code Review and Security Review remain distinct responsibilities even if one Agent Instance performs both in a small project.
6. Every implementation Task requires verification evidence.
7. Human approval remains required for UAT acceptance, Go-live authorization, and high-impact risk acceptance.
8. Project context and source code remain isolated between projects by default.
9. Existing projects remain pinned to an adopted AIEO release until they choose or are required to upgrade.
10. Runtime-specific implementation must not redefine the logical Organization model.

## 5. Release scope and limitations

- Organization documents and role definitions in this package are approved as the AIEO v1.0.0 baseline.
- The Claude Code adapter is a design specification. It is **not** a tested, ready-to-run runtime integration.
- Runtime mappings, automation, and project bootstrap behavior must be implemented and validated separately before production use.
- The release does not imply that files have been committed to Git or published as a GitHub Release.

## 6. Status conventions

- **Approved:** part of the released organizational baseline.
- **Deprecated:** retained for compatibility but no longer recommended.
- **Retired:** no longer supported.

## 7. Recommended review order

1. `organization/governance.md`
2. `organization/protocols/`
3. `organization/standards/`
4. `organization/quality/`
5. `organization/agents/`
6. `organization/skills/`
7. `organization/workflows/`
8. `organization/templates/`
9. `organization/integrations/` and `organization/config/`
