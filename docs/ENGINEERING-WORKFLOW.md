# Engineering Workflow

## Purpose

Define the minimum workflow used to coordinate human decisions,
ChatGPT reasoning, Codex execution, repository knowledge, and
Git/GitHub integration.

The workflow must preserve project knowledge and engineering
control without creating unnecessary process overhead.

## Core Principles

1. The repository is the authoritative source of persisted project knowledge.
2. Persist useful project knowledge, not conversation history.
3. Significant product and engineering decisions remain under human authority.
4. AI agents execute within authorized boundaries and provide verifiable evidence.
5. Process and review depth must remain proportional to risk, complexity,
   and learning value.

## Context Views

### Project & Engineering Workflow

**Owns:** The engineering operating model, tooling workflow, repository
knowledge structure, Context Bootstrap / Session Handoff, SDD,
Git/GitHub/Jira workflow, and AI-agent governance.

**Does Not Own:** Work assigned to another Context View.

**Boundary / Escalation:** It may identify and recommend work belonging to
another Context View, but must not silently assume that role or execute the
subsequent stage without explicit human direction.

### Product & Requirements

**Owns:** Product intent, operational problems, Product Backlog from the
product perspective, Epics/Stories, prioritization/refinement, business needs,
expected behavior, business rules, Acceptance Criteria, functional scope,
product clarification, and `spec.md` when justified.

**Does Not Own:** Technical design, implementation, Codex execution, branch
creation for implementation, or integration.

**Boundary / Escalation:** Approval of a Story or `spec.md` approves product
intent only and never implicitly authorizes technical design, branch creation,
Codex execution, implementation, or integration.

### Architecture & Technical Design

**Owns:** The technical HOW for approved product intent, including
architecture, boundaries, APIs/contracts, persistence, security, concurrency,
transactions, patterns, technical dependencies, `plan.md` when justified,
ADRs when justified, and technical trade-offs.

**Does Not Own:** Material product decisions or implementation authorization.

**Boundary / Escalation:** It must not invent or silently change material
product decisions. Material product ambiguity returns to Product &
Requirements. Approved technical design may be declared Ready for
Implementation, but this does not authorize implementation or Codex execution.

### Implementation & Code Review

**Owns:** Implementation in C#/.NET, authorized Codex execution, code review,
debugging, scoped refactoring, verification against approved product and
technical intent, and preparation of changes for review.

**Does Not Own:** Scope changes, architecture redesign, integration, or merge.

**Boundary / Escalation:** It may make local implementation decisions within
established boundaries. Material product decisions return to Product &
Requirements. Material architecture decisions return to Architecture &
Technical Design. Authorization to implement does not authorize scope changes,
architecture redesign, integration, or merge. Human review remains required
before integration.

### Quality & SDET

**Owns:** Quality strategy, unit/integration/API/E2E test design and
automation, testability, risk-based coverage, regression, quality gates, CI
testing, defect analysis, and verification against approved expectations.

**Does Not Own:** Product behavior or architecture.

**Boundary / Escalation:** It may derive test scenarios from approved
requirements and identify defects, risks, and ambiguities. It must not silently
redefine product behavior or architecture. Material product questions return
to Product & Requirements. Material technical-design questions return to
Architecture & Technical Design. Quality participates throughout delivery
rather than only after implementation.

### Transversal Rule

A Context View may recommend the next Context View but must not silently assume
it. Completion or approval of work in one Context View never implicitly
authorizes the next stage. The human retains authority over transitions between
Context Views and final integration.

## Context Bootstrap

A new working session reconstructs the Minimum Effective Context
from authoritative repository sources.

As part of the Minimum Effective Context:

1. Identify the current chat's Context View.
2. Load that Context View's responsibility boundary from this document.
3. Continue using `docs/PROJECT.md`, `AGENTS.md`, and `docs/STATUS.md`
   according to the bootstrap rules below, then retrieve the shared Working
   Baseline from `context/working-baseline:docs/WORKING-BASELINE.md`.
4. Load only the responsibility context needed for the current Context View
   rather than all Context Views, unless additional boundaries are needed for
   a transition.

Start the repository context with:

1. `docs/PROJECT.md`
2. `AGENTS.md`
3. `docs/STATUS.md`

### Shared Working Baseline

After reading the authoritative repository context on `main`, read the latest
`docs/WORKING-BASELINE.md` from the dedicated
`context/working-baseline` branch. Always resolve this stable branch/path;
a checkpoint SHA remembered by a chat may be outdated.

The Working Baseline is an intermediate, cross-chat record of conversational
progress toward the current task and the next official checkpoint. It is not
a second `STATUS.md`, and cannot silently override official project state.
Use only relevant, verified entries to establish the effective working
position. If the official state has changed, reconcile the baseline before
relying on it; unresolved conflicts require human clarification.

When the human explicitly approves an unambiguous, relevant decision, or
another meaningful intermediate working-state change is verified, update the
Working Baseline automatically where GitHub access permits, under the
standing authorization limited to that branch and file. Do not treat agent
proposals, silence, or inferred agreement as approvals. Mark proposals or
uncertainties as pending or unverified, not approved. Avoid redundant writes.

For each publication:
1. Fetch the latest Working Baseline and its blob SHA from the dedicated
   branch; consult current official context as needed.
2. Reconcile new information with the published baseline and authoritative
   repository state. Stop and request clarification for unresolved conflicts.
3. Update only `docs/WORKING-BASELINE.md` on
   `context/working-baseline`, passing the current blob SHA to prevent
   overwriting concurrent changes. If the write is rejected, re-read and
   reconcile before retrying.
4. Confirm the published commit/file SHA and report a concise change summary.
   If publication was not completed, report that explicitly.

This is an experimental, best-effort ChatGPT-assisted process, not a
guaranteed trigger on every message. It grants no authority to modify
`main`, official specifications, product knowledge, sprint state, or
implementation branches. Those changes retain the existing authorization,
review, and PR/merge requirements. When intermediate decisions are officially
persisted, reconcile the Working Baseline to avoid stale duplication.

### Repository and Conversation Authority

Context Bootstrap establishes the persisted project state from the
repository before evaluating conversation history as supplementary
working context.

Knowledge must be classified according to the following rules.

#### 1. Authoritative Persisted State

Knowledge is authoritative when it is recorded in the repository
Source of Truth responsible for that knowledge and is currently
valid, rather than draft, proposed, or superseded.

`STATUS.md` defines the persisted Current Work and Next Step.

Conversation history must not be presented as persisted repository
state or silently replace its authoritative contents.

#### 2. Approved but Unpersisted Working Context

A conversational decision qualifies only when all conditions hold:

- The human explicitly approved the specific decision.
- The approval occurred after the relevant persisted checkpoint,
  and this ordering can be established.
- No later applicable decision supersedes it.
- No newer authoritative persisted knowledge contradicts it.

Agent proposals, continued discussion, inferred agreement,
absence of objection, and requests for clarification do not
constitute human approval.

A later explicitly approved decision may supersede an earlier
decision without automatically modifying the repository.

Valid approved working context may represent progress or a change
beyond the persisted checkpoint. It may be used to continue work
without repeating completed decisions, provided its unpersisted
status remains explicit.

A superseded decision must not be treated as current.

#### 3. Unverified Working Context

Conversation-derived knowledge that cannot satisfy the conditions
for Approved but Unpersisted Working Context is unverified.

This includes unapproved proposals, exploratory discussions,
uncertain approval or temporal ordering, unresolved conflicts,
and potentially superseded decisions whose validity cannot
be established.

Report unverified context when it is relevant to the current work
or could cause an incorrect decision. Do not include irrelevant
historical discussions.

Unverified context must not be used to advance project state
or establish authoritative decisions.

When conflicting decisions cannot be reliably ordered or
reconciled, request human clarification rather than selecting
a decision by inference.

#### 4. Continuation, Persistence and Authorization

Context Bootstrap must distinguish:

- Authoritative Persisted State;
- Approved but Unpersisted Working Context;
- Unverified Working Context requiring human reconciliation.

Report the persisted Current Work and Next Step separately from
any effective working position established by valid, explicitly
approved, unpersisted decisions.

Before a material transition, evaluate whether relevant
unpersisted knowledge should be persisted.

Approval of a decision does not automatically authorize
repository modifications, Jira operations, branch creation,
implementation, integration, or transitions between Context Views,
except for the narrowly scoped, standing authorization to record verified
working context in the dedicated Working Baseline as defined above.

The human retains authority over unresolved decisions,
state-changing actions, and transitions.

Use `STATUS.md` to identify any additional context required, such as active
specifications or referenced ADRs.

Load additional documentation only when it is relevant to the
current task.

## Session Handoff

Use a Session Handoff only when unfinished working context must
move to another ChatGPT session and cannot be reconstructed
completely from the repository.

A Handoff is a temporary delta over Context Bootstrap, not a
project Source of Truth.

Include only what is necessary to resume:

- Work Context
- Relevant unpersisted working conclusions
- Unresolved decisions
- Current position
- Next action

Do not duplicate repository knowledge or conversation history.

The receiving session performs Context Bootstrap first, validates
the Handoff against repository context, and continues from the
remaining valid delta.

A Session Handoff is single-use. If another transfer is required,
generate a new Handoff from the current working state.

## Codex Execution

Prefer a simple direct Codex instruction when it provides sufficient
execution context.

Use a more explicit Codex Handoff only when Codex requires
authorized information that cannot be obtained completely and
unambiguously from the repository.

When a task requires repository modifications that cannot be performed
on the current branch, the task instruction must explicitly authorize
Codex to create or switch to a working branch, or explicitly identify
the branch to use. Codex must not create or select a working branch
without that authorization.

A Codex task may define, when necessary:

- Task objective
- Authorized scope
- Required context
- Approved constraints or decisions
- Required validation
- Expected reporting

Only include sections that add information required for the task.

The Codex Handoff must contain the minimum context that removes
material ambiguity for the task. Brevity must never take priority
over preserving approved decisions correctly.

Any approved behavior, rule, structure, constraint, or other
material semantic decision required by the task must either be
stated explicitly in the Codex instruction or referenced
unambiguously from an authoritative repository source.

Codex may infer low-level execution and implementation mechanics
within established boundaries. Codex must not infer or redesign
approved intent, semantics, requirements, scope, or material
project decisions.

When approved semantics are defined but implementation or wording
remains delegable, the instruction must explicitly provide those
semantics.

When the approved content itself must be preserved, the instruction
must provide or reference that exact content and prohibit
unauthorized summarization, reinterpretation, or extension.

Codex may make low-level implementation choices within established
boundaries but must not expand scope or make unresolved material
product, domain, architecture, security, persistence, or contract
decisions.

Codex executes and validates work but does not approve its own work.

## Review and Integration

Review depth is proportional to risk, complexity, and learning value.

Before integration, establish sufficient confidence in:

- authorized scope;
- correctness;
- required validation;
- technical understanding of material implementation decisions.

Once accepted, the mechanical operations required to stage, commit,
push, and prepare a Pull Request may be grouped into one authorized
workflow step.

Persistent changes enter `main` through Pull Requests.

Before merge, verify that the Pull Request still represents the
approved change and contains no unexpected scope or unresolved
material issues.

Merge into `main` requires explicit human approval.

Use the established Squash & Merge strategy.

After merge, synchronize local `main`, verify repository state,
and safely remove the merged working branch.

## Knowledge Persistence

Documentation is updated at meaningful checkpoints rather than
after every individual decision.

Persist knowledge when it has future product, engineering,
operational, or decision value.

Each piece of persisted knowledge should have one authoritative
home. Prefer existing project artifacts over creating new ones.

ChatGPT helps identify and consolidate persist-worthy knowledge.
The human approves the intended change.
Codex materializes only the authorized repository update.

A checkpoint does not automatically require documentation changes.
If no valuable new knowledge needs persistence, continue working.
