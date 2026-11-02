# Security by Design Standard

**Version:** 1.0.0 | **Status:** Draft

## Purpose
Integrate security considerations into architecture, implementation, testing, and operations.

## Baseline expectations
- Identify assets, trust boundaries, and threat scenarios proportionate to risk.
- Apply least privilege and deny-by-default where appropriate.
- Authenticate identities and authorize actions at trusted boundaries.
- Validate input and encode output appropriately.
- Protect secrets through approved secret-management mechanisms.
- Protect sensitive data in transit and at rest where required.
- Use maintained dependencies and assess known vulnerabilities.
- Log security-relevant events without exposing secrets or unnecessary personal data.
- Apply secure configuration and environment separation.
- Plan incident response, backup, and recovery for relevant systems.

## Review
Security Engineer performs risk-based review. Material residual risks require an authorized human risk owner; an Agent cannot accept them.
