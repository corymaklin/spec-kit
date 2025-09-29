# [PROJECT_NAME] Constitution
<!-- Example: Spec Constitution, TaskFlow Constitution, etc. -->

## Core Principles

### [PRINCIPLE_1_NAME]
<!-- Example: I. Library-First -->
[PRINCIPLE_1_DESCRIPTION]
<!-- Example: Every feature starts as a standalone library; Libraries must be self-contained, independently testable, documented; Clear purpose required - no organizational-only libraries -->

### [PRINCIPLE_2_NAME]
<!-- Example: II. CLI Interface -->
[PRINCIPLE_2_DESCRIPTION]
<!-- Example: Every library exposes functionality via CLI; Text in/out protocol: stdin/args → stdout, errors → stderr; Support JSON + human-readable formats -->
### 
When you need to install a package. Add it to the package requirements (e.g. setup.py) before so that another dev can easily re-create the env locally.

### Separation of Concerns (Each layer of tech stack as separate packages)
Each layer of the architecture should be implemented as its own package or module. This enforces clear boundaries, reduces accidental coupling, and makes it easier to maintain, test, and replace parts of the system independently.

### Ship complete vertical slices before broadening horizontally
For every new feature, we aim to produce a working slice of functionality that covers the entire flow — from interface to persistence — for at least one concrete use case.

For example: Instead of partially building storage, UI, and event processing modules in isolation, we ship a full, usable flow such as “Add Liquidity” before moving on to “Remove Liquidity” or “Swap.”

### Fakes instead of mocks for unit tests
A fake is a lightweight, in-memory implementation of an interface that behaves like the real system but is fast and predictable.
Avoid mock objects that just record calls or verify interactions, because they often couple tests to implementation details rather than behavior.

### Atomic Commits
- Each commit should capture exactly **one logical change** (e.g., implementing a use case, fixing a bug, refactoring a module).
- A commit must leave the codebase in a **buildable, testable, and working state** (i.e. can't commit when tests are failing).

### Polymorphism / Avoiding Big Ifs
Instead of polymorphism via classes, FP typically uses algebraic data types (ADTs) and pattern matching.

Example (Elm/Scala/F# style):
```
type PaymentMethod =
    | CreditCard of CardInfo
    | PayPal of Email

let charge payment amount =
    match payment with
    | CreditCard info -> chargeCreditCard info amount
    | PayPal email    -> chargePayPal email amount
```

### [PRINCIPLE_3_NAME]
<!-- Example: III. Test-First (NON-NEGOTIABLE) -->
[PRINCIPLE_3_DESCRIPTION]
<!-- Example: TDD mandatory: Tests written → User approved → Tests fail → Then implement; Red-Green-Refactor cycle strictly enforced -->

### [PRINCIPLE_4_NAME]
<!-- Example: IV. Integration Testing -->
[PRINCIPLE_4_DESCRIPTION]
<!-- Example: Focus areas requiring integration tests: New library contract tests, Contract changes, Inter-service communication, Shared schemas -->

### [PRINCIPLE_5_NAME]
<!-- Example: V. Observability, VI. Versioning & Breaking Changes, VII. Simplicity -->
[PRINCIPLE_5_DESCRIPTION]
<!-- Example: Text I/O ensures debuggability; Structured logging required; Or: MAJOR.MINOR.BUILD format; Or: Start simple, YAGNI principles -->

## [SECTION_2_NAME]
<!-- Example: Additional Constraints, Security Requirements, Performance Standards, etc. -->

[SECTION_2_CONTENT]
<!-- Example: Technology stack requirements, compliance standards, deployment policies, etc. -->

## [SECTION_3_NAME]
<!-- Example: Development Workflow, Review Process, Quality Gates, etc. -->

[SECTION_3_CONTENT]
<!-- Example: Code review requirements, testing gates, deployment approval process, etc. -->

## Governance
<!-- Example: Constitution supersedes all other practices; Amendments require documentation, approval, migration plan -->

[GOVERNANCE_RULES]
<!-- Example: All PRs/reviews must verify compliance; Complexity must be justified; Use [GUIDANCE_FILE] for runtime development guidance -->

**Version**: [CONSTITUTION_VERSION] | **Ratified**: [RATIFICATION_DATE] | **Last Amended**: [LAST_AMENDED_DATE]
<!-- Example: Version: 2.1.1 | Ratified: 2025-06-13 | Last Amended: 2025-07-16 -->