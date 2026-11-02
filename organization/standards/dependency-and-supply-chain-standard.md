# Dependency and Supply Chain Standard

**Version:** 1.0.0 | **Status:** Draft

## Purpose
Control risks introduced by third-party libraries, tools, images, packages, and external services.

## Requirements
- Use approved package sources and registries.
- Prefer maintained dependencies with clear ownership and licensing.
- Pin or constrain versions according to project policy.
- Review security advisories and vulnerability findings.
- Minimize dependency footprint and unnecessary privileges.
- Record material external service dependencies.
- Avoid downloading and executing untrusted artifacts.
- Define update and remediation responsibility.

## Exceptions
A dependency with unresolved material risk requires documented rationale, mitigation, owner, and human approval where risk acceptance is required.
