# ADR-0002: Enterprise Organization Graph™

> Architecture Decision Record  
> Status: Accepted  
> Decision Date: July 2026  
> Platform: Cougar OS  
> Authority: Cougar Constitution™

---

## Context

Cougar OS must understand how organizational objects relate to one another.

Traditional databases can store missions, decisions, documents, agents, and memories, but isolated records do not provide a complete model of organizational meaning.

The platform must answer questions such as:

- Which mission produced this decision?
- Which evidence supports this policy?
- Which Lane owns this department?
- Which memories influenced this recommendation?
- Which risks affect this product?
- Which agents worked on this project?

A connected organizational model is required.

---

## Decision

Cougar OS will maintain an **Enterprise Organization Graph™** as the authoritative relationship model for organizationally significant entities.

Major organizational objects may become graph nodes.

Connections between those objects become governed relationships.

The graph will be updated only through approved graph runtime services.

---

## Node Eligibility Rule

Not every fact becomes a graph node.

A fact becomes a node only when it has durable organizational significance.

Examples of valid nodes include:

- organizations
- founders
- Executive Lanes
- departments
- Foundries
- missions
- decisions
- policies
- products
- risks
- research
- memories
- customers
- partners
- assets

Supporting facts should remain:

- evidence attached to an existing node
- Intelligence DNA
- Memory Foundry records
- temporary mission context

This prevents node explosion and graph pollution.

---

## Runtime Architecture

```text
Verified Intelligence
        ↓
Knowledge Graph Updater
        ↓
Enterprise Graph Event
        ↓
Enterprise Graph Runtime
        ↓
Enterprise Graph Store
        ↓
Graph Snapshot
```

Direct graph mutation outside the governed runtime is prohibited.

---

## Node Intelligence

Every node may include intelligence metadata such as:

- confidence
- importance
- knowledge weight
- usage count
- risk score
- executive value
- last evaluation time

This supports organizational prioritization and future intelligence scoring.

---

## Relationships

Relationships are directional and explain how nodes interact.

Examples include:

- owns
- leads
- governs
- belongs-to
- reports-to
- assigned-to
- created
- approved
- supports
- depends-on
- protects
- monitors
- related-to

Every relationship must have an organizational purpose.

---

## Consequences

### Positive

- Connected organizational intelligence
- Stronger explainability
- Better executive reasoning
- Traceable mission and decision history
- Easier dependency analysis
- Foundation for visual graph exploration
- Support for predictive organizational intelligence

### Tradeoffs

- Graph governance adds complexity
- Duplicate prevention requires deterministic identity rules
- Relationship quality must be maintained
- Not all stored information can become a node
- Persistent storage will eventually be required beyond in-memory runtime state

---

## Alternatives Considered

### Relational database only

Rejected as the sole organizational model because complex cross-domain relationships would become difficult to reason about and explore.

### Every fact as a graph node

Rejected because it would create node explosion, noise, and reduced organizational meaning.

### Agent-owned private graphs

Rejected because organizational truth must remain shared, governed, and independent of individual agents.

---

## Constitutional Alignment

This decision supports:

- Article III — Organization First
- Article IV — Governance
- Article VII — Enterprise Organization Graph™
- Article XI — Event-Driven Architecture
- Article XIV — Continuous Learning

---

## Implementation Requirements

Graph implementations must provide:

- deterministic node identities
- relationship deduplication
- governed mutation paths
- event publication
- provenance links
- Intelligence DNA traceability
- lifecycle status
- audit history
- memory integration

---

## Review Triggers

Revisit this decision when:

- persistent graph infrastructure is selected
- multi-organization graphs are introduced
- temporal graph versioning is implemented
- graph federation becomes necessary
- relationship inference becomes autonomous

---

## Outcome

The Enterprise Organization Graph™ becomes the connected structural model of Cougar OS.

It represents what the organization is, what it owns, what it knows, and how its work is connected.

---

**Cougar Technologies**  
**ADR-0002: Enterprise Organization Graph™**
