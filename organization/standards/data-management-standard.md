# Data Management Standard

**Version:** 1.0.0 | **Status:** Draft

## Purpose
Make data responsibility, integrity, access, and lifecycle explicit.

## Requirements
- Identify data domains and authoritative owners.
- Define read/write responsibilities and approved access paths.
- Avoid direct cross-service writes that bypass ownership boundaries.
- Define schema migration and compatibility strategy.
- Consider consistency, concurrency, idempotency, and recovery.
- Minimize sensitive data collection and exposure.
- Define retention, deletion, backup, and restoration requirements where applicable.
- Use synthetic or appropriately protected test data.

## Distributed systems
Document replication, synchronization, eventual consistency, conflict handling, and failure recovery where relevant.

## Change control
Data model changes require impact assessment, migration/rollback or recovery strategy, and verification evidence.
