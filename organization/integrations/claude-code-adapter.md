# Claude Code Adapter — Design Specification

**Version:** 1.0.0  
**Status:** Approved
## Purpose

Describe how AIEO logical definitions may be mapped to Claude Code. This is a design specification, not a claim that all mappings have already been implemented or tested.

## Mapping

| AIEO concept | Claude Code implementation direction |
|---|---|
| Project entry point | Project `CLAUDE.md` |
| Agent Definition | Claude Code subagent definition |
| Skill | Skill/instruction package where supported |
| Project context | Project docs referenced from `CLAUDE.md` |
| Delegation | Runtime-supported subagent/team/task mechanisms |
| Permissions | Runtime permission configuration and user approvals |
| Workflow | Instructions plus scripts/hooks only where justified |
| Quality Gate | Explicit workflow checks and evidence requirements |

## Implementation rules

1. Verify current Claude Code capabilities and syntax before generating runtime files.
2. Keep Organization logical definitions as the source of truth.
3. Generate runtime configuration from approved definitions where practical.
4. Do not assume project repositories inherit user-level configuration.
5. Keep project context and sessions isolated.
6. Apply least privilege and explicit approval for sensitive operations.
7. Test generated configurations in a disposable pilot project before broad adoption.

## Known boundary

The adapter must be versioned separately from the Organization model because runtime capabilities and configuration formats can change independently.
