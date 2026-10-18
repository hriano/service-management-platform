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
