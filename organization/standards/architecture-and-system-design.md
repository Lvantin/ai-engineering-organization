# Architecture and System Design Standard

**Version:** 1.0.0 | **Status:** Draft

## Purpose
Ensure architecture is explicit, reviewable, and proportionate to project complexity.

## Required considerations
- Business capabilities and system boundary.
- Applications, services, components, and ownership.
- Data ownership and data flows.
- Synchronous and asynchronous interfaces.
- External dependencies and trust boundaries.
- Deployment topology and environments.
- Security, reliability, scalability, performance, and operability.
- Migration and evolution constraints.

## Architecture artifacts
Select depth by complexity and risk. Typical artifacts include System Context Diagram, System Component Diagram, Service Catalog, Service Dependency Map, API/Event Contracts, Data Ownership Map, ADRs, Deployment Architecture, NFR Specification, and Security Architecture.

## Design review
Review responsibilities, coupling, failure modes, consistency, retries, idempotency, backward compatibility, observability, and operational support.

## Decisions
Significant decisions require an ADR with context, options, decision, consequences, and status. Architecture decisions belong to Solution Architect within delegated authority.
