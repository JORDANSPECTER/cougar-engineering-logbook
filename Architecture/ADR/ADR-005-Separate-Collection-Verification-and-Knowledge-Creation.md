# ADR-005: Separate Collection, Verification, and Knowledge Creation

- **Status:** Accepted
- **Date:** 2026-07-13
- **Decision owners:** Engineering Lane™, Research Lane™, Memory Lane™

## Context

Treating successful collection as proof of truth would allow unverified information to enter organizational memory and the Enterprise Graph.

## Decision

The intelligence lifecycle is divided into explicit stages:

1. collection planning;
2. collection execution;
3. mission queue processing;
4. verification;
5. Intelligence DNA creation;
6. knowledge graph update;
7. memory and organizational use.

Each stage has separate responsibilities, events, validation, and failure states.

## Consequences

### Positive

- Prevents raw collection from becoming trusted knowledge automatically.
- Improves observability and retry handling.
- Supports specialized agents and verification policies.
- Makes quality failures traceable.

### Tradeoffs

- Adds processing latency and components.
- Requires idempotency and event correlation.
- More failure states must be tested and monitored.

