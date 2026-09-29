# Lions Keep Project Constitution

## Core Principles

### I. Build the Game in Vertical Slices
Prioritize a small, playable tactical RPG MVP over broad engine expansion. Deliver features as
end-to-end slices that can be demonstrated and verified. Reuse existing engine capabilities when
they meet the feature's needs; add abstractions only when a spec demonstrates a concrete need.

### II. Create an Original Game Identity
Lions Keep may use broad tactical-RPG concepts such as grid-based battles, turn order, elevation,
and character classes. Define their rules and implementation for Lions Keep. All shipped art,
characters, maps, names, story, audio, animation, UI composition, and other expressive presentation
MUST be original or properly licensed. Do not extract or reproduce Final Fantasy Tactics assets or
distinctive expressive designs. The reference game is inspiration, not a feature specification.

### III. Keep Issues and Specs Authoritative
Every feature MUST trace to a GitHub issue that explains the problem, player value, and motivation.
Its feature spec defines scope, behavior, acceptance criteria, assumptions, and exclusions. Plans
and tasks MUST derive from that spec and MUST NOT silently change its scope. When implementation,
plan, tasks, or existing code conflict with the spec, stop and resolve the discrepancy with the
project owner before proceeding.

### IV. Make Tactical Rules Explicit and Verifiable
Gameplay rules MUST be stated in observable, testable terms, including relevant boundaries such as
movement range, turn eligibility, elevation, targeting, and defeat. Core battle outcomes MUST be
deterministic for the same initial state and inputs unless a feature spec explicitly requires
randomness and defines how it is controlled. Tests MUST cover meaningful rule boundaries and
regressions.

### V. Match Validation to Risk
Every feature MUST have acceptance checks derived from its user scenarios. Add automated tests for
gameplay rules and shared engine behavior where practical; verify visual or interaction behavior
with a focused manual check when it cannot be covered automatically. Do not claim a feature is
complete while its required checks are unrun or failing.

## Product and Technical Constraints

- The product goal is a playable MVP of Lions Keep, an original tactical RPG, built in this
	repository's existing C++23/CMake framework.
- Keep the MVP scope explicit in its GitHub issue and spec. Campaigns, editors, multiplayer, large
	progression systems, and other deferred ideas remain out of scope until separately prioritized
	and specified.
- Follow repository build, formatting, resource-lifetime, and generated-file constraints in
	`AGENTS.md`. Do not modify third-party or generated content unless a task explicitly requires it.
- Specs and plans MUST record unresolved assumptions and dependencies that materially affect
	player experience, architecture, or scope. Agents MUST ask rather than invent a decision when no
	safe default exists.

## Specification-Driven Workflow

1. Start with a GitHub issue describing why the feature matters and who benefits.
2. Create or update one feature spec from that issue. Include player scenarios, testable
	 acceptance criteria, success measures, assumptions, and out-of-scope items.
3. Review and approve the spec before planning. The plan records how the approved scope fits the
	 existing codebase and identifies risks; tasks are dependency-ordered work to satisfy the spec.
4. During implementation, agents MUST consult this constitution, `AGENTS.md`, the linked issue,
	 and the active feature artifacts. Surface contradictions before changing scope.
5. Update the spec and obtain approval before implementing newly discovered requirements. Do not
	 smuggle deferred roadmap ideas into the current feature's tasks.

## Governance

This constitution governs cross-feature product and engineering decisions. `AGENTS.md` provides
repository operating details; a feature issue and its approved spec provide feature-specific intent
and scope. When these sources appear to conflict, agents MUST pause and ask the project owner to
resolve the conflict rather than choosing silently. Amendments require project-owner approval,
an updated rationale, and a semantic version increment: MAJOR for incompatible principle changes,
MINOR for new or materially expanded principles, and PATCH for clarifications that do not change
policy. Feature plans and reviews MUST check compliance with this constitution.

**Version**: 1.0.0 | **Ratified**: 2026-09-29 | **Last Amended**: 2026-09-29
