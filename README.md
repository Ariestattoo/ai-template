Here’s a basic `README.md` you can drop into the template repo.

# Project Template

Reusable repository template for projects that use ChatGPT for architectural discussion and Codex for implementation.

The goal is to keep project knowledge in the repository so it can be used consistently from different machines and development environments.

## Structure

```text
.
├── AGENTS.md
├── README.md
└── docs/
    ├── architecture.md
    ├── constraints.md
    ├── conventions.md
    └── decisions/
        └── README.md
```

## Files

### `AGENTS.md`

Defines the operating rules Codex should follow when working in the repository.

Keep this file relatively short. It should describe how Codex should behave, not contain the full architecture of the project.

### `docs/architecture.md`

Describes the current architecture of the system.

Typical content includes:

- major components
- responsibilities
- data flow
- service boundaries
- APIs and interfaces
- deployment model
- persistence
- external integrations

This document should describe the current intended state of the system.

### `docs/constraints.md`

Contains technical or business constraints that should not be changed casually.

Examples:

- hardware limitations
- required protocols
- deployment restrictions
- supported platforms
- compatibility requirements
- network assumptions
- security requirements

### `docs/conventions.md`

Contains project-specific development conventions.

Examples:

- directory structure
- naming
- API patterns
- error handling
- logging
- testing
- dependency policy
- configuration patterns

### `docs/decisions/`

Contains Architecture Decision Records (ADRs).

Use an ADR when a decision has long-term architectural consequences or when future developers will benefit from understanding why a particular approach was chosen.

Examples:

- database selection
- communication protocol
- framework selection
- service boundaries
- deployment strategy
- major dependency changes

## Creating a new project

This repository should be configured as a GitHub Template Repository.

To create a project:

1. Open this repository on GitHub.
2. Select **Use this template**.
3. Select **Create a new repository**.
4. Clone the new repository.
5. Replace this README with the project's actual README when appropriate.
6. Populate the files under `docs/` with project-specific information.

## Initial project setup

For a new project, complete the documentation in roughly this order:

1. `docs/architecture.md`
2. `docs/constraints.md`
3. `docs/conventions.md`
4. any initial ADRs under `docs/decisions/`

`AGENTS.md` should generally require little modification.

## Using ChatGPT

Use the ChatGPT Project for:

- architecture discussions
- design exploration
- troubleshooting
- planning
- reviewing alternatives
- documenting decisions

When a discussion produces durable project knowledge, extract the final conclusions and add them to the repository.

Do not copy entire conversations into the repository.

Instead, capture:

- final decisions
- architectural reasoning
- constraints
- conventions
- unresolved questions

## Using Codex

Codex should treat the repository documentation as authoritative project context.

Before substantial architectural or cross-cutting changes, Codex should review:

```text
docs/architecture.md
docs/constraints.md
docs/conventions.md
docs/decisions/
```

Implementation changes that modify documented architecture should update the relevant documentation in the same change.

## Knowledge workflow

The intended workflow is:

```text
ChatGPT discussion
        |
        v
distilled architectural knowledge
        |
        v
repository documentation
        |
        v
Codex implementation
        |
        v
Git commit
```

Git is the authoritative synchronization point for both source code and durable project knowledge.

## General rule

Conversations are temporary working context.

The repository contains the durable state of the project.

This version is deliberately generic enough to stay in the template itself.