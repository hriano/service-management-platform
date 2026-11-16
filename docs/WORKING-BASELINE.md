# SMP — Working Baseline

**Status:** Active — Initial checkpoint
**Purpose:** Shared, temporary conversational progress between authoritative repository checkpoints.
**Official baseline:** `main:docs/STATUS.md` (read at initialization; blob SHA `5128eb9f015df9ac7f72db13cf59c4400f50af7b`).
**Authority:** This file does not replace or override `docs/STATUS.md`, `docs/PROJECT.md`, approved specifications, or ADRs.

## Official Starting Position
- Phase: Phase 1 — Product Definition & Requirements.
- Current Work: Identify high-level operational problems and prepare the initial Product Backlog for the Operational MVP.
- Official Next Step: Identify those problems, create and prioritize the initial Product Backlog, then plan the first Sprint.
- Source: `main:docs/STATUS.md`. These are references to the official state, not changes to it.

## Approved Working Decisions — Context Management
- GitHub is the shared location for discovering the latest **published** Working Baseline.
- Publish the Working Baseline automatically when an explicitly approved, unambiguous change is identified, subject to available tool access and verification.
- Use a dedicated branch: `context/working-baseline`; keep the Working Baseline separate from official `STATUS.md`.
- Working Baseline records intermediate conversational progress toward a smaller task or an official project checkpoint; it must not silently conflict with official repository state.
- A working session reads the official repository state and the latest published Working Baseline, checks compatibility, and continues from their valid combination.
- Before publishing, re-read the shared baseline and check its current blob SHA; on concurrent changes, reconcile or stop rather than overwrite.
- After a successful publication, report the new Git reference and a short summary.
- Human approval remains necessary for material product and engineering decisions. Automatic publication records approved decisions; it does not grant the assistant authority to approve them.
- Ambiguous approvals or unresolved conflicts require human clarification.
- Official repository changes continue through the established review and PR process. Automatic baseline publication is limited to this dedicated branch and artifact.
- Automatic publication is experimental; its reliability will be evaluated and the approach may be revised.


## Approved Working Decisions — Learning & Session Practice (2026-11-11)
- Primary learning objective: develop an **AI-Native End-to-End Software Engineering** profile capable of discovering business problems, designing justified solutions, orchestrating an AI-assisted software factory, assuring code quality, product quality and agreed scope, and delivering verifiable working software.
- Organize SMP learning sessions around those end-to-end capabilities and real product problems, rather than around learning tools in isolation. Learn technologies and tools as needed to solve actual problems; retain technical understanding and human review of generated code.
- Incorporate automated code quality, appropriate tests, independent review and evidence-based quality gates progressively as cross-cutting learning and engineering concerns; specific tooling and implementation require their own decisions and authorization.
- At the end of each working session, prepare the next day's plan with a 7:00–9:00 a.m. timetable, objectives, concrete tasks, expected deliverable, preparation and a copy-ready prompt for the appropriate Context View.
- These are approved learning and session-practice decisions, not changes to the official MVP, Current Work, Sprint, architecture, or permission to design, implement, create branches, open PRs or merge. Respect Context View transitions and separate authorizations.


## Approved Working Decision — Reusable Agentic Software Factory (2026-11-16)
- Add a third, complementary long-term objective: build a **reusable agentic software factory** as a professional asset for future own products and independent client projects, alongside (1) developing an AI-native end-to-end engineering profile and (2) delivering SMP as a real, quality product.
- Develop and validate the factory incrementally through real SMP delivery needs, then extract reusable project-agnostic workflows, agent roles, skills, templates, quality gates and delivery/evaluation practices; avoid premature complex multi-agent infrastructure.
- Aim for provider portability where practical and separation of reusable factory configuration from each project's business context, code, secrets and client data.
- This approval is strategic only. Factory architecture, repository placement, tooling, implementation, project changes, branches, PRs and merges remain undecided and require their respective authorization and Context View transitions.


## Approved Working Decision — Interview-Ready Evidence (2026-11-16)
- Treat technical interview preparation and credible professional storytelling as a continuous part of the AI-native engineering learning objective, alongside SMP and the reusable agentic factory.
- Each significant delivery should aim to yield three outcomes: working software, improved reusable factory capability, and defensible professional evidence of engineering decisions and outcomes.
- Build interview narratives from actual problems, solution rationale, AI-agent orchestration, quality assurance and measured impact; preserve authentic artifacts such as code reviews, tests, CI results and decisions where useful and safe.
- Practice structured technical explanations in English, including probing follow-up questions and the ability to defend trade-offs and limitations. Do not invent professional experience, results or metrics.
- Keep factory practices informed by relevant current engineering and hiring expectations, evaluating them against demonstrated engineering value rather than tool popularity; no specific tool, architecture, repository change or implementation is approved by this decision.


## Approved Working Decision — Local Read-Only Discovery Map (2026-11-17)
- Adopt a navigable, interactive Discovery Map as a proposed supporting view for quickly understanding SMP capabilities, needs, business rules, scenarios, approved decisions, and open questions, starting with Participant Management.
- Initial access is local on the user's development computer; cross-device access may be revisited later. No public hosting, GitHub Pages deployment, or custom login is needed for this initial scope.
- The map is read-only: it does not edit requirements, approve decisions, or become a competing source of truth. Updates must follow the authorized requirements/documentation workflow, and the view should reflect valid definitions from the appropriate authoritative sources.
- Jira remains responsible for backlog and Sprint work management; the map is for product discovery comprehension and traceability, not a replacement for Jira.
- Architecture, technology choice, repository placement, data format, implementation, branch creation, PRs, and merge remain undecided and require separate approval and authorization in the appropriate Context Views.


## Approved Working Decision — Automatically Generated Discovery Map (2026-11-17)
- The Discovery Map will be an automatically generated, derived view rather than a manually maintained map.
- Chat-assisted Discovery work will identify a structured change describing the affected concept, type, status, relationships, and authoritative source reference; the human retains approval authority for material decisions.
- Approved definitions remain in their authorized sources. The map may contain regenerable navigation metadata and clearly identified derived summaries, but it must not become a competing source of truth.
- A lightweight generator should rebuild the local map from authorized sources and relevant classified working context within seconds, avoiding manual creation, connection, coloring, or reorganization of nodes.
- Approved, pending, and unverified information must remain visibly distinguishable and must preserve provenance. Automation must not promote pending or unverified information to approved status.
- This decision establishes the feeding and update model only. Viewer technology, generator implementation, repository placement, data schema, file changes, branches, Pull Requests, and merge remain undecided and unauthorized.

## Pending Implementation / Verification
- Validate cross-chat discovery and update behavior in practice; ChatGPT does not guarantee execution of tools on every turn.
- Confirm whether future baseline updates consistently capture all relevant approved decisions.
- Decide whether the proposed working rules need formal incorporation into the official engineering workflow through its existing approval process.

## Checkpoint Scope
- This initial checkpoint records only the explicitly approved context-management decisions above.
- It does **not** assert that all earlier SMP product decisions from other conversations have been recovered.
- No change to official Current Work, Next Step, Sprint status, or product specifications is asserted here.

## Publication Protocol
1. Read `main:docs/STATUS.md` and this file from `context/working-baseline`.
2. Establish the effective working position, respecting official authority and explicit human approvals.
3. Before updating, re-fetch this file and use its current blob SHA for the write.
4. On mismatch or unresolved semantic conflict, do not overwrite; reconcile or request clarification.
5. After publishing, retain the returned commit SHA and the new file blob SHA as verifiable references.
