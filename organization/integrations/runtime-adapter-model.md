# Runtime Adapter Model

**Version:** 1.0.0  
**Status:** Approved
## 1. Purpose

Define the boundary between AIEO's logical Organization model and a specific AI execution runtime.

## 2. Logical model

AIEO defines:
- Roles and Agent Definitions.
- Skills and capability metadata.
- Protocols and workflows.
- Context requirements.
- Delegation packages.
- Permissions and approval boundaries.
- Quality Gates and evidence expectations.

These concepts remain stable even if the underlying runtime changes.

## 3. Adapter responsibilities

A runtime adapter translates logical definitions into runtime-specific constructs:
- Agent configuration.
- System/developer instructions.
- Tool permissions.
- Context loading rules.
- Delegation and team mechanisms.
- Hooks or lifecycle automation where supported.
- Output and evidence capture.

## 4. Adapter constraints

An adapter must not:
- Expand a Role's authority.
- Remove mandatory human approval.
- Weaken Organization security or quality controls.
- Mix contexts between projects.
- Claim a runtime feature exists without verifying the runtime version and capability.

## 5. Compatibility

Each adapter declares supported runtime versions, required features, known limitations, and mapping gaps.

## 6. Separation

Keep logical Organization documents runtime-agnostic. Store Claude Code-specific files in a clearly identified adapter or distribution package.
