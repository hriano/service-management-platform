# AI Agent Instructions

## Purpose

This file defines how AI coding agents must operate within this repository.

Agents execute engineering work within approved requirements and explicit task instructions.

Agents do not own product, architecture, scope, conformance approval, or merge decisions.

Human review and technical ownership remain mandatory.

---

## 1. Required Context

Before performing implementation work, establish the task context in this order:

1. Read `docs/PROJECT.md` for stable project knowledge and engineering principles.

2. Read `docs/STATUS.md` to identify the current work and the explicit context references for the task.

3. Read the current specification referenced by `docs/STATUS.md`, when the task requires a specification.

4. Read ADRs and related specifications explicitly referenced by `docs/STATUS.md` or by the current specification.

5. Inspect existing source code and tests directly related to the requested change.

6. If implementation reveals an undocumented dependency or a potentially applicable architectural decision that is not referenced by the current context:
   - locate the repository artifact only if its path or identity can be determined from an explicit repository reference or from the directly affected code;
   - otherwise report the missing context and do not make a decision based on an unsupported assumption.

Do not scan or load all specifications, ADRs, or documentation by default.

Do not assume that conversation history contains the current source of truth.

Repository documentation and the current codebase take precedence over previous agent conversations.

---

## 2. Specification-Driven Development

Implementation work must use an approved specification when a specification is required.

### Specification Status

A specification is considered approved only when its own document explicitly declares:

`Status: Approved`

If the specification does not explicitly contain an approved status, the agent must not treat it as approved.

If `docs/STATUS.md` references a specification whose status is not `Approved`, report the inconsistency and stop implementation.

### Missing, Ambiguous, or Conflicting Requirements

If a requirement is missing, has more than one behavior consistent with its wording, contradicts another approved requirement, or conflicts with repository knowledge:

1. Do not select or invent the missing behavior.
2. Do not modify the specification.
3. Report the exact requirement or conflict.
4. Identify the implementation work affected by it.
5. State the clarification or decision required.
6. Do not implement the affected behavior until an approved clarification is provided.

The agent may continue only with portions of the task that do not depend on the unresolved requirement.

### When a Specification Is Not Required

The agent must not decide independently whether a task requires a specification.

Specification requirements are determined by the current task instructions or by `docs/STATUS.md`.

A task must be identified as:

`Specification Required: Yes`

or

`Specification Required: No`

If neither value is provided and the requested change modifies any of the following, do not implement the change and report that specification status is missing:

- Product behavior
- Domain rules
- Public API behavior or contracts
- Persistent data structures or behavior
- Authentication or authorization behavior
- Architecture

A change without a specification may be implemented only when `Specification Required: No` is explicitly provided.

---

## 3. Engineering Rules

All generated code must conform to the project's approved specifications, explicit engineering rules, applicable ADR decisions and implementation constraints, established code conventions, and explicit task instructions.

When implementing changes:

- Implement only behavior required by the approved specification or explicit task instructions.
- Prefer the implementation with fewer components, dependencies, abstractions, and execution paths when multiple implementations remain permitted by the approved context.
- Use names and control flow that expose the implemented behavior directly.
- Do not introduce a pattern, framework, package, abstraction, architectural layer, or external dependency unless it is required by the approved specification, an applicable ADR, the existing architecture, or explicit task instructions.
- Apply explicit decisions and implementation constraints from ADRs referenced by the current task context.
- Follow conventions already present in directly related code when those conventions do not conflict with approved requirements or ADRs.
- Do not introduce dance-studio-specific concepts unless required by the approved specification.
- Do not modify or refactor code unrelated to the requested behavior.
- Implement error conditions and edge cases explicitly identified by the approved specification.
- Do not introduce new security, data-integrity, concurrency, or domain rules that are absent from the approved context.
- Do not suppress compiler warnings, validation failures, or failing tests to obtain a passing result.

If implementation requires a decision affecting architecture, domain semantics, security, data integrity, public API contracts, external dependencies, or project scope and that decision is not already defined by approved context, report it and stop the affected implementation.

---

## 4. Testing and Validation

Validation requirements are defined by the approved specification or by explicit task instructions.

The agent must not independently decide which validation activities are sufficient for a feature.

### Required Validation

When a specification is required, it must contain a `Validation Requirements` section.

That section identifies the checks required for completion.

Checks may include:

- Build
- Static analysis
- Unit tests
- Integration tests
- API tests
- End-to-end tests
- Security checks
- Manual verification

Only checks explicitly marked as required by the approved specification or task instructions are mandatory.

### Test Implementation

Create or modify automated tests only when required by:

- the approved specification;
- its acceptance criteria;
- an approved technical plan;
- or explicit task instructions.

Do not remove, weaken, skip, disable, or rewrite an existing test solely to obtain a passing result.

If an existing test asserts behavior that conflicts with an approved requirement:

1. Report the conflicting test.
2. Identify the conflicting requirement.
3. Do not change the expected behavior until explicit authorization is provided.

### Validation Execution

Execute every validation check marked as required.

If a required check cannot be executed:

1. Report the exact check that was not executed.
2. Report the blocking condition or error.
3. Mark that validation check as `Not Executed`.
4. Do not substitute another validation method unless explicitly instructed.

### Validation Evidence

For each acceptance criterion assigned to the task, report:

1. The acceptance criterion identifier.
2. The implementation location that addresses it.
3. The validation evidence required by the approved specification.
4. The validation check that produced that evidence.
5. The result of that check.

The agent reports evidence of conformance.

The agent does not approve requirement conformance.

Human review determines whether the reported evidence demonstrates that the acceptance criterion has been met.

### Validation Status

Report validation status using the following rules:

`Passed`
- Every required validation check was executed and passed.
- Every acceptance criterion assigned to the task has the validation evidence explicitly required by the approved specification.

`Failed`
- At least one required validation check was executed and failed; or
- required validation evidence demonstrates behavior inconsistent with an assigned acceptance criterion.

`Incomplete`
- At least one required validation check was not executed; or
- required validation evidence for at least one assigned acceptance criterion is missing.

Do not report validation as `Passed` under any other condition.

A `Passed` validation status reports the result of the required checks. It does not constitute human approval of requirement conformance or acceptance of the implementation.

---

## 5. Documentation

The agent must not create new documentation files or documentation categories unless explicitly instructed to do so.

The repository recognizes the following documentation artifacts:

- `docs/PROJECT.md` — stable project, product, engineering, and learning context.
- `docs/STATUS.md` — current project state and routing to the context required for current work.
- `specs/<feature>/` — approved feature requirements and their execution artifacts.
- `docs/adr/` — approved architectural decisions.
- `AGENTS.md` — operational instructions for AI coding agents.
- `README.md` — repository entry point and human-facing project overview.

### Documentation Updates

The agent may update an existing documentation artifact only when:

1. The approved specification explicitly requires the update;
2. The task instructions explicitly require the update; or
3. `docs/STATUS.md` explicitly identifies the artifact as an output of the current task.

Otherwise, do not modify documentation.

### New Documentation

Do not create a new documentation file, documentation category, ADR, specification, or supporting artifact unless its creation is explicitly required by the approved specification, `docs/STATUS.md`, or the task instructions.

If implementation reveals information that is not represented in the authorized documentation and preserving that information would require a documentation change:

1. Do not create or modify documentation.
2. Report the information discovered.
3. Identify the existing artifact affected, if one is explicitly identifiable.
4. Request a human decision.

### Documentation Content

When a documentation update is authorized:

- Modify only the artifact and sections identified by the task.
- Do not copy information whose designated source of truth already exists elsewhere in the repository.
- Do not modify unrelated sections.
- Preserve existing approved decisions unless the task explicitly changes them.
- Do not introduce new product, domain, architecture, testing, or process decisions through documentation.

---

## 6. Git and Change Control

Before modifying repository files:

1. Read the current Git branch.
2. Read the current working-tree status.
3. Record any pre-existing modified, staged, or untracked files.

### Branch Protection

If the current branch is `main`:

- Do not modify repository files.
- Report that implementation is blocked because work is being attempted on `main`.

The agent must not create, switch, rename, delete, merge, or rebase branches unless explicitly instructed.

### Existing Changes

Files that were already modified, staged, or untracked before the task must not be overwritten, reverted, staged, deleted, or otherwise altered unless explicitly included in the task.

If the requested work conflicts with a pre-existing change, report the conflict and stop work on the affected file.

### Repository Changes

Modify only files required by the approved task.

Do not:

- commit;
- amend commits;
- push;
- pull;
- fetch;
- merge;
- rebase;
- reset;
- restore;
- clean;
- stash;
- create or delete tags;

unless the specific Git operation is explicitly requested.

At task completion, report every file created, modified, or deleted by the task.

---

## 7. Agent Execution Boundaries

The agent may choose an implementation detail that is not explicitly defined by the approved context only when that choice:

1. does not change required observable behavior;
2. does not change an acceptance criterion;
3. does not contradict an explicit ADR decision or implementation constraint;
4. does not establish or modify a public API contract;
5. does not establish or modify a persistent data contract;
6. does not introduce or modify a product or domain rule;
7. does not introduce a new architectural boundary, pattern, framework, package, external service, or infrastructure dependency;
8. does not establish or modify authentication, authorization, security, data-integrity, concurrency, validation, documentation, or Git policy; and
9. remains within the files and behavior authorized by the task.

If any condition above is not met, or compliance with a condition cannot be determined from the approved context, stop the affected implementation and request a human decision.

The absence of a rule does not authorize the agent to create one.

### Decisions Requiring Human Input

When a required implementation choice would establish or modify any of the following and the choice is not already defined by approved context or explicit task instructions, the agent must not make the decision:

- Product behavior
- Domain rules or terminology
- Architecture or architectural boundaries
- Authentication or authorization policy
- Security policy
- Data-integrity rules
- Persistent data contracts
- Public API contracts
- External packages, services, or infrastructure dependencies
- Project scope
- Validation requirements
- Documentation structure
- Git workflow

When such a decision is encountered:

1. Stop the affected implementation.
2. State the missing decision.
3. Identify the requirement, file, component, or contract affected.
4. Do not select an alternative.
5. Present alternatives only if explicitly requested.
6. Wait for an explicit human decision before implementing the affected behavior.

Detecting a problem does not authorize the agent to resolve a decision outside these boundaries.

---

## 8. Task Completion, Conformance Evidence, and Reporting

The agent must distinguish between:

- implementation execution;
- validation results;
- conformance evidence;
- human approval.

The agent may report the first three.

Only human review can provide the fourth.

### Implementation Status

Report one of:

`Completed`
- Every implementation item explicitly assigned to the task was performed.

`Partially Completed`
- At least one assigned implementation item was performed and at least one assigned implementation item was not performed.

`Not Completed`
- No assigned implementation item was performed.

### Validation Status

Report exactly one of the validation statuses defined in Section 4:

- `Passed`
- `Failed`
- `Incomplete`

If the task has no validation requirements, report:

`Validation Status: Not Required`

only when the approved specification or explicit task instructions explicitly establish that validation is not required.

### Conformance Evidence

The agent does not approve requirement or ADR compliance.

For each implemented task, report:

#### Acceptance Criteria

For every acceptance criterion assigned to the task:

- acceptance criterion identifier;
- implementation location;
- required validation evidence;
- validation result.

#### ADR Traceability

For every ADR referenced by the task context:

- ADR identifier;
- explicit decision or implementation constraint applicable to the change;
- implementation location where that decision or constraint was applied.

If a referenced ADR contains no decision or implementation constraint applicable to the current change, report:

`Applicable Constraint: None`

Do not infer additional ADR constraints from background, context, rationale, or consequences unless they are explicitly stated as part of the ADR decision or implementation constraints.

Human review determines whether the evidence demonstrates compliance.

### Required Final Report

At the end of every task, report:

1. `Implementation Status`
2. `Validation Status`
3. Files created
4. Files modified
5. Files deleted
6. Validation checks executed and their results
7. Acceptance-criterion evidence
8. ADR traceability
9. Assigned implementation items not completed
10. Required human decisions or clarifications

Do not commit, push, merge, declare requirement conformance approved, or declare the implementation accepted.

Human review determines whether the implementation is accepted.

