# AGENTS.md

## Purpose

This repository contains the authoritative source code and technical documentation for this project.

Before making non-trivial changes, understand the relevant architecture, constraints, and existing decisions.

## Required reading

For architectural or cross-cutting changes, read:

- `docs/architecture.md`
- `docs/constraints.md`
- `docs/conventions.md`
- relevant records under `docs/decisions/`

## Working rules

- Preserve established architecture unless the requested change explicitly requires modifying it.
- Do not silently override documented constraints.
- Prefer existing project patterns over introducing new frameworks, libraries, or abstractions.
- Keep changes focused on the requested scope.
- Identify architectural implications before making cross-cutting changes.
- When implementation and documentation disagree, flag the discrepancy rather than assuming which is correct.

## Architectural decisions

Significant architectural decisions should be recorded under:

`docs/decisions/`

Use the existing ADR format.

Examples include:

- introducing or removing a major dependency
- changing service boundaries
- changing persistence strategy
- changing communication protocols
- changing deployment architecture
- changing public APIs or interfaces
- changing security boundaries

## Documentation maintenance

If a change modifies the documented architecture, constraints, or conventions, update the corresponding documentation as part of the same change.

Do not update documentation solely to make it agree with an implementation that appears accidental or incorrect.