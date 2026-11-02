# Agent Instantiation and Delegation Protocol

**Version:** 1.0.0  
**Status:** Approved
## 1. Purpose

Define how an Agent Instance is selected, prepared, instantiated, assigned work, supervised, validated, and closed.

## 2. Core concepts

- **Agent Definition:** approved Organization-level definition of a Role.
- **Agent Instance:** runtime instance created from an Agent Definition.
- **Task:** bounded unit of work with an objective and acceptance criteria.
- **Context Package:** curated references and information required for execution.
- **Delegation Package:** complete task instruction including scope, constraints, permissions, deliverables, and verification.
- **Evidence:** observable artifact or result supporting a completion claim.

## 3. Principles

- Instantiate only approved Roles.
- Provide context before execution.
- Delegate bounded work with explicit outcomes.
- Apply least privilege.
- Preserve role authority boundaries.
- Require evidence for completion.
- Keep traceable task and instance identifiers.
- Escalate ambiguity, conflicts, and risks.

## 4. Instance lifecycle

Requested → Role Selected → Context Prepared → Instantiated → Ready → Executing → Submitted for Validation → Accepted / Rework Required / Blocked / Rejected → Completed or Terminated.

An instance may be reused for compatible tasks only when project isolation, context integrity, role boundaries, and task traceability remain intact.

## 5. Delegation Package

Every delegated task should specify:
- Task ID and title.
- Parent Feature/User Story.
- Assigned Role and Agent Definition version.
- Objective and background.
- In-scope and out-of-scope work.
- Requirements and acceptance criteria.
- Relevant applications/services and technology context.
- Dependencies and sequencing constraints.
- Permissions and environment boundaries.
- Expected deliverables.
- Verification commands or procedures.
- Applicable Quality Gates.
- Reporting and escalation expectations.

## 6. Execution protocol

The Agent acknowledges the task, identifies missing information, executes within scope, reports material status changes, and submits results with evidence. Scope expansion requires approval from the delegating authority.

## 7. Parallel execution

Parallel tasks are permitted only when boundaries and dependencies are understood. Shared files, schemas, contracts, database migrations, and integration points require explicit coordination. Integration and conflict resolution remain assigned to the Engineering Manager or designated technical owner.

## 8. Result package

A result submission includes:
- Outcome summary.
- Files or artifacts changed.
- Implementation decisions.
- Tests and verification evidence.
- Known limitations.
- Defects or follow-up work.
- Dependencies and risks.
- Recommended status.

## 9. Validation

Engineering Manager validates task completeness and coordination requirements. Specialist Roles validate their domain-specific responsibilities. Validation outcomes are Accepted, Rework Required, Blocked, Rejected, or Escalated.

## 10. Permissions and human approval

Use least privilege and separate read, write, execute, deploy, and administrative permissions where supported. Production-impacting actions, irreversible operations, external communications, and high-impact decisions require explicit authorization under project governance.

## 11. Runtime independence

This protocol defines logical behavior and does not require a specific agent runtime, CLI, IDE, or orchestration framework.
