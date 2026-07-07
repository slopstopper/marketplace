# Founding context — the pattern analysis as it appeared (2026-07-06/07)

**Why this document exists:** the extraction program (issue #1) carries the
*decisions* from the session that founded it. This carries the *seeing* — the
full analysis as it stood in live context, written down in the founding
session's last hours because no later session can reconstruct it. Conclusions
survive in issues; this is the meeting, not the minutes.

**Provenance:** synthesized 2026-07-06 from four parallel deep-reads of the
owner's work: the Veska Index git/PR history (924 commits, 200 PRs, 5.5 weeks),
the docs corpus (specs/plans/playbook/ADRs), the `.claude/` enforcement
infrastructure, and seven sibling projects. Confidence: measured where numbers
are given; interpretive elsewhere, and labeled.

---

## 1. The shapes in the owner's thinking

**The master pattern: generated coherence is not evidence.** Veska Index
("finding no structure is a valid result"), the AI Harm Dictionary ("felt
coherence is a signal warranting examination, not confirmation"), and The Big
Idea Compressor ("do not expand, do not flatter") are one epistemic stance
pointed at celestial data, AI systems, and the owner's own ambitions
respectively. Everything else observed is downstream of this.

**Coordinate systems, compulsively.** R1–R25 rules, G1–G15 gaps, W1–W27 queue,
AD-debt, SL-logic units, defensibility tiers A–D, the Harm Dictionary's
Established/Provisional/Observed/Gap claim ladder, current/partial/mock/planned.
Cross-references use IDs, not prose. The epistemic-status taxonomy has been
independently reinvented at least three times across projects — the strongest
extraction signal found.

**A discipline → mechanism pipeline.** Every rule matures along one ladder:
stated in prose → performed as ritual → encoded as prompt (skill/subagent) →
mechanized as hook → gated in CI. The owner treats manual-discipline residue as
a bug (the 2026-06-29 plumb-line self-audit — running their own principles
against their own repo and generating a 7-branch remediation — is the clearest
evidence). Guards are genuinely engineered: pure-decision cores, test seams,
deliberate fail-open/fail-closed calculus per guard.

**Sessions chained through artifacts, not memory.** The pipeline: assessment →
gap register → lane-routed queue → owner concept session → spec →
mid-executable plan → execution → handover with inherited debts → ledger row.
Each stage leaves a document the next session reads instead of re-exploring.
"Mid-executable" (a spec a cheaper model can run without design judgment) and
"lane scarcity dominates urgency" are original scheduling economics.

**PRs as audit checkpoints, not review queues.** Median self-merge: 23 minutes.
The value is the ritual: gates green, auditors PASS, R22 block, bit-identical
baseline. Commit messages encode epistemic claims ("detection-window honesty",
"fail-loud accrual", "pure refactor").

**An extractor's instinct.** plumb-line (claim honesty) and tokenomics (model
economics) were both pulled out of Veska practice into standalone toolkits.
Method-as-deliverable (METHODOLOGY.md, WORKFLOW.md, portable-method.md) appears
in every mature project.

**Projects survive only inside the scaffold.** Szdxa0 (Obsidian vault, dead
after one note), TBIC (stalled, README never written), the 124KB Codex-era
monolith — everything outside a disciplined repo died. Everything inside
thrived. The failure mode is consistent enough to design against — this is the
finding the survival-scaffold work (recursive-spine#29) exists to answer.

## 2. Friction, measured

1. **Prose ledgers were the #1 conflict source:** 52 merge-main-into-branch
   commits (~1 per 4 PRs); CURRENT_STATUS.md and the playbook the hotspots; a
   W19 ledger row silently lost in a merge; handovers hand-predicting conflicts
   to compensate. *(Resolved: the 2026-07-07 tracking cutover.)*
2. **Doc drift recurred despite being declared a first-class bug:** CLAUDE.md
   claimed one composition-root engine (reality: three, ADR-0014) and ADRs to
   0016 (reality: 0023); a PR existed solely to fix stale status. *(Drift bugs
   fixed in the cutover; systemic fix = doc-facts lint, Veska #239.)*
3. **The core invariant had no mechanical gate:** R5/R6/R19 (provenance, mock
   containment) enforced only by opt-in subagents. *(Veska #238.)*
4. **Review-fix chains** of 3+ rounds because audits ran only pre-merge.
   *(Veska #243 — audit at task boundaries.)*
5. **Constraints hand-copied into every plan's** Global Constraints block.
   *(recursive-spine #30 — slice scaffolding from one canonical source.)*
6. **Deferral tails aged silently** (follow-ups file, W17 "top-urgency" yet
   deferred indefinitely). *(Resolved structurally: deferral-requires-a-record
   + the digest's aging report.)*
7. **Hygiene existed but wasn't scheduled:** ~57 stale merged branches; a
   117-commits-behind duplicate clone; format trailer commits from generated
   artifacts. *(Veska #240.)*
8. **The memory system double-logged** the same event 4–6× per day.
   *(Folded into #240.)*
9. **Long research runs were fragile:** the Antikythera deep-research workflow
   exhausted its budget mid-synthesis and needed manual salvage. *(Veska #245 —
   checkpointed phases.)*

## 3. The extraction targets (the program's spine)

A. **One epistemic-status taxonomy** — merge Veska's source-status vocabulary,
   the defensibility tiers, and the Harm Dictionary's claim ladder (plus its
   semver-for-claims convention) into one versioned spec owned by plumb-line.
   Written three times; write once, import everywhere. *(Veska #241.)*
B. **Tracked state as structured, queryable data** — *(became the cutover and
   recursive-spine v0.1–0.3; the part that shipped first.)*
C. **The survival-scaffold kit** — CLAUDE.md/AGENTS.md templates, guard wiring,
   ADR dir, CI, memory dir, tracking stamp: scaffolding a new idea in ~10
   minutes so TBIC-scale ideas stop dying in infancy. *(recursive-spine #29 —
   THE open design decision: grow recursive-spine-bootstrap vs an org-level
   composed scaffold.)*
D. **Slice-scaffolding** — generate spec/plan/handover docs; constraints from
   one source. Seam with tokenomics' handoff-spec unsettled. *(rs#30.)*
E. **The enforcement ladder as data** — per-rule rung table making "mechanize
   the residue" a queue, not a vibe. *(Shipped: Veska PR #246,
   docs/architecture/enforcement-ladder.{json,md}.)*

Plus, from the sibling survey: bootstrap the non-repo projects (Harm Dictionary,
TBIC) and a conversation-export pipeline for the unprocessed 60MB M-era.json
*(rs#31)*.

## 4. What the name meant (recorded interpretation, not the owner's words)

The owner named the plugin **recursive-spine** while designing what became the
tracking convention — but the session's own record shows the name was reaching
for more: the spine of the *whole practice*. The thing that holds every project
upright, applies to itself, and carries the recursion doctrine ("a discipline
too heavy to follow while building the tool that states it is a wrong
discipline") across all of it — tracking being one vertebra, the survival
scaffold, slice scaffolding, and the enforcement ladder being others. The
shipped v0.3.0 is the narrowest honest reading of the name. rs#29's open
design question — expansion vs composition — is equivalently: *does
recursive-spine become what it was named for?* That decision is the owner's,
ideally written in their own words as a concept comment on rs#29 before any
further build. This paragraph is the founding session's reading of the gap; it
must not substitute for the owner's own statement.

## 5. How the founding session went wrong, mechanically (so it isn't repeated)

The owner's opening mandate was the full extraction. Mid-session they added a
correction — retire CURRENT_STATUS.md, use issues+milestones — and that
correction became the spec's §0 concept sentence. Everything in the analysis
that didn't serve that sentence silently fell out at the spec boundary: the
session ran a preservation ledger for Veska's playbook but never for its own
report. The structural lesson, now applied: **any session consuming an
analysis this size must disposition every proposal in it (carried / filed /
retained / explicitly dropped) before narrowing to a concept sentence** — the
same gate the migrate skill enforces for prose ledgers, applied to analyses.

## 6. The one-paragraph version

The owner is a builder of instruments for honest observation, and applies the
same instinct to their own process: rules numbered, work leaving artifacts,
discipline mechanized rung by rung. Friction concentrates wherever process
state lives as prose and wherever enforcement is still at the ritual/prompt
rung. The system to build is not a new discipline — it is finishing the
ladder: state queryable, the core invariant gated, facts checkable, and a
scaffold cheap enough that every future idea starts inside the structure that
keeps this work alive.
