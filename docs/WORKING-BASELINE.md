# SMP — Working Baseline

**Status:** Active — Shared working checkpoint
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


## Approved Working Decision — Structured Discovery Projection Pipeline (2026-11-18)
- Feed the Discovery Map through incremental structured changes produced by chat-assisted Discovery work rather than by repeatedly reinterpreting the complete source set.
- Before an item enters the map, it must be represented in a persisted, classified source: an authoritative source for authoritative knowledge, or an authorized working-context record such as the Working Baseline for approved-but-unpersisted, pending, or unverified information.
- A deterministic validator will check the structured change's schema, stable identity, provenance, classification/status, permitted state transition, source reference, and relationships. It must not interpret requirements or make approval decisions.
- After validation, apply the change to a derived, regenerable index optimized for map navigation. The index has no independent authority and must preserve links and revisions for its contributing sources.
- The viewer consumes the derived index and remains separated from the source-ingestion and validation mechanism, allowing the viewer or index storage technology to evolve independently.
- This decision approves the conceptual pipeline only. Node and relationship taxonomy, storage format (including JSON or SQLite), viewer, generator technology, repository placement, local synchronization mechanism, implementation, files, branches, Pull Requests, and merge remain undecided and unauthorized.


## Approved Working Decision — Simplified Functionality-Centered Discovery View (2026-11-19)
- Use **Functionality** as the only primary navigation element in the initial Discovery Map. The system view will list all SMP functionalities with a concise description, source reference, and summary of defined rules and outstanding work.
- Selecting a functionality will show two simple bullet collections: **Business Rules** and **Pending Items**. Do not represent capabilities, problems, domain concepts, scenarios, decisions, Stories, or semantic relationships as first-class visual nodes in the initial view.
- Display Business Rules with only two user-facing authority states: **Approved Working** for a rule explicitly approved in chat and persisted as working context but not yet incorporated into its designated official source; and **Authoritative** for a rule incorporated into the current official source.
- Use **Pending Items** as one deliberately broad collection for needs, questions, ambiguities, and matters requiring deeper review. Do not introduce additional visible pending-item taxonomies unless demonstrated usage requires them.
- Keep description, source, rule state, and pending-item provenance sufficient to preserve traceability without turning the view into another source of truth.
- This decision refines the earlier Discovery Map concept toward a lightweight functionality catalog rather than a connected semantic graph. The automatic generation and structured projection pipeline remain applicable, but their derived index and viewer should be correspondingly minimal.
- This decision does not choose the storage format, viewer technology, generator technology, repository placement, synchronization mechanism, visual styling, implementation, files, branches, Pull Requests, or merge; those remain undecided and unauthorized.


## Approved Working Decision — Minimal Discovery Projection Contract (2026-11-19)
- Define the derived projection around `Functionality` records containing only a stable identifier, name, concise description, source reference, Business Rules, and Pending Items.
- Define each `BusinessRule` with a stable identifier, text, authority state, and source. Permit only two user-facing rule states: **Approved Working** (explicitly approved and persisted in the Working Baseline, but not yet incorporated into its designated official source) and **Authoritative** (incorporated into the current official repository source).
- Define each `PendingItem` with a stable identifier, text, reason, origin, and source. Permit the initial reasons **Needs Definition**, **Needs Approval**, and **Needs Verification**; keep them in one visible pending collection rather than separate taxonomies.
- Treat a conversation as an item's origin, never as its sole recoverable source. Automatically persist every map-visible pending item or approved working rule in the Working Baseline and verify that publication before reporting the map update as successful. Recording an item as pending does not approve its content.
- Use only **Working Baseline** and **Official Repository** as initial recoverable source kinds. A source reference contains only kind and location. Do not include a per-item revision in the projection; regenerate the small derived index from current sources to maintain freshness. This refines and supersedes the earlier per-item revision-preservation expectation in the Structured Discovery Projection Pipeline.
- Keep Jira outside the projection contract and outside the source kinds. Jira manages Epics, Stories, tasks, priorities, Sprints, assignees, blockers, and delivery progress; it may link to definitions but does not replace their designated sources.
- Derive rule and pending counts at view time. Keep visual styling, layout, history, users, comments, Stories, Sprints, capabilities, problems, domain concepts, scenarios, Acceptance Criteria, and semantic graph relationships outside the initial projection.
- Show only the current effective view. Git, Jira, and conversation systems retain their own history; the Discovery Map does not duplicate it.
- This decision establishes the minimum conceptual data contract only. Storage format, viewer technology, generator implementation, repository placement, synchronization implementation, files, branches, Pull Requests, and merge remain undecided and unauthorized.


## Approved Working Decision — Single-File JSON Discovery Projection (2026-11-20)
- Store the complete initial Discovery Map derived index in one generated JSON file containing all Functionality records and their Business Rules and Pending Items, following the approved Minimal Discovery Projection Contract.
- Treat this JSON as a disposable, regenerable projection optimized for the local read-only viewer. It has no independent authority and must not be edited as a source of product definitions.
- On a relevant source change, rebuild the complete projection from the current Working Baseline and official repository sources, validate the complete result deterministically, and replace the previous JSON atomically only after successful validation.
- Keep the viewer separate from generation and validation. The viewer reads the generated JSON and derives presentation-only values such as rule and pending-item counts.
- Do not initially divide the projection into one JSON file per functionality. That alternative adds catalog coordination, multi-file loading, and orphan or partial-update risks without a demonstrated need at the expected SMP scale.
- Do not initially use SQLite. Its tables, queries, schema migrations, access library, and browser integration add maintenance without a current requirement for transactional writes, complex queries, concurrent access, or partial loading.
- Reconsider partitioned JSON or SQLite only when measured behavior across the complete SMP map demonstrates a concrete limitation, such as unacceptable generation or loading time, memory use, file size, inspection difficulty, or a newly approved query or concurrency requirement.
- This decision selects the conceptual initial storage format only. It does not approve a JSON schema implementation, file or repository location, viewer or generator technology, synchronization mechanism, code, files, development branches, Pull Requests, or merge.


## Approved Working Decision — Discovery Session Closure Integrity Review (2026-11-20)
- Perform an integrity review of the active Discovery working conversation when the user explicitly requests session closure, even when the session produced no approved decision.
- During that review, identify any explicitly approved decision not yet published, map-relevant pending item needed to resume the work, and contradiction or matter requiring verification that would otherwise remain only in the conversation.
- Persist relevant pending items in the Working Baseline using the approved Pending Item classification. Recording a pending item preserves it for follow-up and does not approve its proposed content, alternatives, or outcome.
- Do not copy the complete conversation or preserve casual ideas, discarded alternatives, repetition, or other material that is not needed to understand the system or resume the work.
- If the review finds a relevant change, publish it to the Working Baseline and verify the resulting repository version before reporting the session as safely captured. If it finds no relevant change, do not create a baseline update.
- Continue publishing explicitly approved decisions during the session when they occur; the closure review is a final integrity safeguard, not a reason to delay known publications.
- Do not rely on passive detection that a conversation has ended. The closure review is triggered by an explicit user instruction such as “finalicemos la sesión.”
- This decision establishes a conceptual session-continuity rule only. It does not authorize changes outside the Working Baseline, automatic access to past conversations, implementation, code, files, development branches, Pull Requests, or merge.


## Approved Working Decision — Minimal Local Static Discovery Viewer (2026-11-20)
- Use a minimal local static web viewer for the initial Discovery Map, implemented conceptually with HTML, CSS, and a small amount of browser JavaScript.
- Do not initially use React, TypeScript, React Flow, a custom backend, authentication, or a database for the viewer. The approved functionality-centered projection does not currently require a component framework, graph rendering, server-side behavior, or transactional storage.
- Keep the viewer separate from the generated single-file JSON projection. The viewer reads the projection without interpreting, approving, or modifying requirements.
- Provide a system-level functionality list or search and a selected-functionality detail view showing its name, concise description, source, Business Rules, authority states, Pending Items, and pending reasons.
- Use a simple local static-file server to make the viewer and JSON available to the browser, avoiding browser restrictions associated with loading JSON directly through `file://`. Selection of the concrete local server mechanism remains an implementation decision.
- Preserve the ability to replace the viewer technology later without changing the authoritative sources or the approved projection contract. Any future access from other devices requires a separate decision covering hosting, network exposure, privacy, and access control.
- This decision selects the conceptual initial viewer approach only. It does not authorize implementation, code, files, repository placement, visual design, concrete server tooling, cross-device access, development branches, Pull Requests, or merge.

## Approved Working Context — Participant Management (2026-11-20)

**Authority classification:** Approved but unpersisted working context, now recorded in the Working Baseline. It is not yet an authoritative product specification or Product Backlog item.

**Identifier note:** The `PM-*` identifiers below are stable working references for this baseline and the Discovery Map projection. They are not official Story, Acceptance Criterion, Jira, or specification identifiers.

### Operational Problem

#### PM-OP-01 — Inconsistent and unreliable participant registration

> El registro de nuevos participantes no tiene un proceso definido que garantice datos consistentes, búsquedas efectivas e información fidedigna. Los datos almacenados pueden estar incompletos, no se puede identificar fácilmente si pertenecen a un participante específico, lo que genera desconfianza en la información. Se necesita invertir en tiempos largos para reconfirmar la información y aun así se pueden generar errores, como solicitud de información a personas equivocadas. Se hacen uso de reprocesos de verificación para determinar la fidelidad de un dato y participan diferentes personas del staff quienes no siguen un procedimiento estándar, adicionalmente se almacenan los datos en diferentes fuentes, no existe una fuente de verdad consolidada.

- Origin: Product & Requirements working conversation.
- Status: Approved Working.
- Related functionality: `PM-FN-01` and the pending participant-search definition.

### Functionality

#### PM-FN-01 — Registro mínimo de un participante nuevo

> El operador registra un nuevo participante con los siguientes datos obligatorios: nombre y apellido del participante y al menos un medio de contacto (teléfono o email). Si el participante no tiene contacto, se registra un contacto diferente con los siguientes datos obligatorios: nombre y apellido y al menos un medio de contacto (teléfono o email). Los datos quedan almacenados y estos pueden ser consultados inmediatamente, obteniendo los datos del participante y/o del contacto cuando corresponda.

- Status: Approved Working.
- Current boundary: participant search is considered important and must be included in the product work, but its behavior is still pending definition. The functionality is therefore not ready to be treated as a complete Story or approved specification.

### Business Rules

#### PM-BR-01 — Minimum participant data
- A valid registration requires the participant's first name and last name, plus at least one contact method: email or phone.
- Status: Approved Working.
- Related functionality: `PM-FN-01`.

#### PM-BR-02 — Different contact person when the participant has no contact
- If the participant has no contact, a different contact person is registered with first name, last name, and at least one contact method: email or phone.
- Status: Approved Working.
- Related functionality: `PM-FN-01`.
- Preserved ambiguity: the meaning of “contact” must still be clarified so it cannot be confused with “contact method.”

#### PM-BR-03 — Contact ownership and identification
- When the contact details belong to a person different from the participant, that person's first name and last name must be registered and the person must be identified as the contact.
- Status: Approved Working.
- Related functionality: `PM-FN-01`.
- Preserved ambiguity: the statement that the participant registration must indicate “si es el participante” still requires clarification.

#### PM-BR-04 — Nonblank contact method
- A phone or email is considered provided only when it contains at least one non-whitespace character.
- Status: Approved Working.
- Related functionality: `PM-FN-01`.

#### PM-BR-05 — Storage and immediate consultation
- The registration data is stored and can be consulted immediately, returning participant data and contact-person data when applicable.
- Status: Approved Working.
- Related functionality: `PM-FN-01`.
- Preserved boundary: immediate consultation does not yet define the behavior of general participant search.

### Approved Scope Exclusions

#### PM-SE-01 — Phone format validation
- Phone-format validation is not included for now.
- Status: Approved Working scope exclusion.
- Related functionality: `PM-FN-01`.

#### PM-SE-02 — Email format validation
- Email-format validation is not included for now.
- Status: Approved Working scope exclusion.
- Related functionality: `PM-FN-01`.

#### PM-SE-03 — Relationship type
- The relationship type between the participant and a different contact person is not included for now.
- Status: Approved Working scope exclusion.
- Related functionality: `PM-FN-01`.

### Pending Items

#### PM-Q-01 — Search fields
- Text: Define which participant or contact-person data may be used to search.
- Reason: Needs Definition.
- Affects: participant search and the boundary of `PM-FN-01`.
- Discussed but unapproved alternatives: participant first name, participant last name, participant phone, participant email, contact-person phone, and contact-person email. Search by date or service has no approved definition.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-02 — Search matching
- Text: Define whether each search field uses exact, partial, or another matching behavior.
- Reason: Needs Definition.
- Affects: participant search.
- Discussed but unapproved alternatives: exact and partial matching.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-03 — Case and accent handling
- Text: Define whether searches ignore letter case and diacritics.
- Reason: Needs Definition.
- Affects: participant search.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-04 — Multiple matches
- Text: Define the behavior when a search returns more than one participant.
- Reason: Needs Definition.
- Affects: participant search.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-05 — Search-result content
- Text: Define which participant and contact-person data is shown in search results.
- Reason: Needs Definition.
- Affects: participant search and `PM-BR-05`.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-06 — No-result behavior
- Text: Define the behavior when no participant matches the search.
- Reason: Needs Definition.
- Affects: participant search.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-07 — Shared contact data
- Text: Define the expected behavior when the same phone or email is associated with more than one participant or contact person.
- Reason: Needs Definition.
- Affects: participant search, identification, and possible duplicate handling.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-08 — Immediate consultation versus general search
- Text: Clarify whether immediate consultation after registration and later participant search are the same product behavior or separate behaviors.
- Reason: Needs Definition.
- Affects: `PM-BR-05` and participant search.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-09 — “Contact” terminology
- Text: Distinguish unambiguously between a contact method and a different contact person.
- Reason: Needs Definition.
- Affects: `PM-FN-01`, `PM-BR-02`, `PM-BR-03`, scenarios, and Acceptance Criteria.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-10 — Cardinality
- Text: Define how many contact methods and different contact persons a participant registration may contain within this slice.
- Reason: Needs Definition.
- Affects: `PM-FN-01`, business rules, and scenarios.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-11 — Duplicate handling
- Text: Define whether and how a new participant registration is checked against existing participant data.
- Reason: Needs Definition.
- Affects: registration reliability, search, and the operational problem in `PM-OP-01`.
- Source: Working Baseline; origin is the Product & Requirements conversation.

#### PM-Q-12 — Final scenarios and Acceptance Criteria
- Text: Reconcile and explicitly approve the scenarios and verifiable Acceptance Criteria after the search behavior and remaining terminology are defined.
- Reason: Needs Approval.
- Affects: readiness of `PM-FN-01` as a Story or specification.
- Source: Working Baseline; origin is the Product & Requirements conversation.

### Unverified Scenario Work

The following examples were explored during the learning exercise but were not explicitly approved as final scenarios or Acceptance Criteria:

- `PM-SC-01`: successful registration using participant name, last name, and email.
- `PM-SC-02`: successful registration using participant name, last name, and phone, followed by later consultation.
- `PM-SC-03`: successful registration when a participant without their own phone or email has a complete different contact person.
- `PM-SC-04`: rejection when the different contact person's last name is missing.
- `PM-SC-05`: rejection when neither the participant nor the different contact person provides a phone or email.
- The early incomplete example containing only “Claudia” and a phone did not establish a complete expected outcome.

These examples must not be treated as approved behavior until Product & Requirements explicitly reconciles and approves them.

### Conflict Requiring Preservation

#### PM-CF-01 — Phone containing letters
- An exploratory scenario proposed rejecting phone `2451 A25568` because it contains a letter.
- That scenario was not explicitly approved and conflicts with the later approved exclusion `PM-SE-01`, which places phone-format validation outside the current scope.
- Effective working position: do not use the letter-rejection scenario as current behavior or Acceptance Criteria. Any future change requires an explicit Product & Requirements decision.

### Current Product Working Position

- Sufficiently defined: the operational problem, the minimum registration functionality, required participant data, the alternative different contact person, nonblank presence of phone or email, storage and immediate consultation, and current scope exclusions.
- Still pending: complete participant-search behavior, terminology, cardinality, duplicate handling, final scenarios, Acceptance Criteria, and Story consolidation.
- Not usable as approved requirements: the unverified scenarios, phone-letter rejection, unapproved search fields or matching semantics, search by date or service, and simulated interview details.
- Next Product & Requirements step: define participant search one decision at a time, beginning with the permitted search fields; then reconcile scenarios and approve verifiable Acceptance Criteria.
- This working position does not authorize Architecture, implementation, code changes, Jira changes, branches, Pull Requests, or merge.


## Pending Implementation / Verification
- Validate cross-chat discovery and update behavior in practice; ChatGPT does not guarantee execution of tools on every turn.
- Confirm whether future baseline updates consistently capture all relevant approved decisions.
- Decide whether the proposed working rules need formal incorporation into the official engineering workflow through its existing approval process.

## Checkpoint Scope
- This checkpoint records the explicitly approved working decisions above and the classified Participant Management working context recovered from the current Product & Requirements conversation.
- It does **not** assert that product decisions from other conversations have been recovered.
- Participant Management entries remain working context until incorporated into their designated official repository source through the authorized workflow.
- No change to official Current Work, Next Step, Sprint status, Jira, or product specifications is asserted here.

## Publication Protocol
1. Read `main:docs/STATUS.md` and this file from `context/working-baseline`.
2. Establish the effective working position, respecting official authority and explicit human approvals.
3. Before updating, re-fetch this file and use its current blob SHA for the write.
4. On mismatch or unresolved semantic conflict, do not overwrite; reconcile or request clarification.
5. After publishing, retain the returned commit SHA and the new file blob SHA as verifiable references.
