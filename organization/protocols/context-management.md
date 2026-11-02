# Context Management Protocol

**Version:** 1.0.0  
**Status:** Approved
## 1. Purpose

Define how project information is discovered, selected, packaged, refreshed, and maintained for Agent execution.

## 2. Context sources

Context may come from approved Organization documents, project documentation, work items, architecture artifacts, source repositories, contracts, test evidence, and authorized operational records.

Every source should be identifiable and its authority understood.

## 3. Source precedence

Use the source explicitly designated as authoritative for the relevant information. Do not apply a universal rule that source code always overrides approved requirements or architecture decisions.

When sources conflict:
1. Record the conflict and affected scope.
2. Identify owners of the conflicting information.
3. Gather implementation and decision evidence.
4. Escalate unresolved intent or authority questions.
5. Update the authoritative source after confirmation.

## 4. Context package assembly

The delegating Agent should select:
- Organization rules relevant to the assigned Role.
- Project entry point and profile.
- Relevant Feature and Task context.
- Application/service documentation.
- Architecture, contracts, data ownership, and dependencies relevant to the change.
- Verification and operational instructions.

Prefer links/references to large artifacts over copying entire documents.

## 5. Context confidence labels

Use:
- **Verified:** explicitly confirmed by an authoritative source or direct reliable evidence.
- **Inferred:** derived from evidence but not explicitly documented.
- **Assumed:** temporary working assumption.
- **Unknown:** not established.

Assumptions that materially affect implementation require confirmation.

## 6. Freshness

Context owners should update documentation when material changes are accepted. Agents should flag stale documents when observed implementation or approved decisions materially diverge.

## 7. Security

Do not place secrets, credentials, personal data, or unrestricted production data in ordinary context packages. Use approved secret and access mechanisms.

## 8. Completion

A context package is adequate when the assigned Agent can identify its objective, relevant system boundaries, constraints, dependencies, expected output, verification method, and escalation route.
