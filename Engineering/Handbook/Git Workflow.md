# GitHub Standards

> Version: 1.0.0  
> Status: Active

---

# Purpose

This document defines the GitHub engineering standards used across all Cougar repositories.

Applies to:

- Cougar HQ
- Cougar OS
- Cougar Trade
- Shared libraries
- Future Cougar repositories

The objective is to maintain a professional, consistent, and auditable development workflow.

---

# Engineering Philosophy

A Git repository is more than source code.

It is the permanent engineering history of the platform.

Every commit should help future engineers understand:

- What changed
- Why it changed
- When it changed
- How it affects the platform

---

# Repository Standards

Every repository should include:

```
README.md
CHANGELOG.md
LICENSE
.gitignore

/docs
/src
/public
```

When appropriate, repositories should also contain:

```
Architecture/
Engineering/
Releases/
Missions/
Milestones/
Images/
```

---

# Branch Strategy

## Main

```
main
```

Always represents the most stable version.

Direct commits should be avoided whenever practical.

---

## Development

```
develop
```

Primary integration branch.

Engineering work should merge here before production.

---

## Feature Branches

Naming convention:

```
feature/runtime-dashboard

feature/intelligence-pipeline

feature/organization-graph

feature/memory-foundry
```

One feature branch should represent one engineering objective.

---

## Hotfix Branches

```
hotfix/api-authentication

hotfix/runtime-crash
```

Reserved for production fixes.

---

# Commit Standards

Commits should be small, focused, and descriptive.

Preferred format:

```
type(scope): summary
```

Examples:

```
feat(runtime): add BootManager initialization sequence

feat(memory): implement Enterprise Memory Explorer

feat(graph): add Mission Relationship Graph

fix(api): prevent duplicate runtime registration

docs(engineering): add AI development standards

refactor(runtime): simplify service initialization
```

---

# Commit Types

| Type | Purpose |
|-------|----------|
| feat | New feature |
| fix | Bug fix |
| docs | Documentation |
| refactor | Internal improvement |
| test | Tests |
| chore | Maintenance |
| perf | Performance |
| style | Formatting |

---

# Pull Request Standards

Every pull request should answer:

## What changed?

Describe the implementation.

---

## Why?

Explain the engineering motivation.

---

## Impact

Identify affected systems.

Examples:

- Runtime
- Mission Intelligence
- Enterprise Graph
- Memory Foundry
- UI

---

## Testing

Document:

- manual testing
- automated tests
- validation steps

---

## Documentation

Confirm whether updates were made to:

- README
- CHANGELOG
- ADR
- Engineering Journal
- Mission documentation

---

# Documentation Rule

Documentation is required whenever engineering behavior changes.

Examples:

- new architecture
- new runtime service
- API changes
- governance changes
- engineering standards
- release behavior

---

# Repository Organization

Large repositories should group related functionality together.

Example:

```
src/

components/

runtime/

graph/

memory/

lanes/

foundries/

missions/

engineering/

docs/
```

Avoid flat directory structures as the platform grows.

---

# Naming Standards

Names should describe responsibility.

Good:

```
MissionIntelligenceEngine

EnterpriseGraphStore

ExecutiveRecommendationEngine
```

Avoid:

```
Manager

Helper

Utils

FinalVersion

Temp
```

---

# README Expectations

Every major module should include a README explaining:

- purpose
- architecture
- dependencies
- usage
- future work

Documentation should evolve with implementation.

---

# Issue Tracking

Engineering work should be traceable.

Issues should include:

- objective
- priority
- affected systems
- dependencies
- acceptance criteria

---

# Milestone Tracking

Major engineering accomplishments should be grouped into milestones.

Each milestone should summarize:

- completed missions
- architecture changes
- engineering lessons
- next objectives

---

# Release Management

Every release requires:

- CHANGELOG update
- Release Notes
- Git tag
- Version increment
- Documentation review

---

# Code Reviews

Reviews should evaluate:

- architecture
- readability
- maintainability
- testing
- documentation
- future extensibility

The goal is to improve the platform rather than simply approve changes.

---

# Engineering History

The Git history should tell the story of Cougar's evolution.

Avoid large commits containing unrelated work.

Prefer many well-documented commits over infrequent massive commits.

---

# Long-Term Objective

Create repositories that remain understandable years after their original implementation.

Engineering history should become an organizational asset rather than a record of source code alone.

---

# Guiding Principle

> Every commit should make the platform easier to understand.

GitHub is the engineering memory of Cougar.
