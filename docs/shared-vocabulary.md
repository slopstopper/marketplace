# Shared vocabulary — the seams, pinned

Three plugins, three disjoint concerns. Where their words touch, this
doc is the tiebreaker. Each term has exactly one owner; the others
defer or alias.

## Ownership

| concern | owner | the others |
|---|---|---|
| Whether claims are honest (provenance, confidence, laundering) | **plumb-line** | consume; never redefine |
| Which model does the work (lanes, tiers, routing, handoff specs) | **tokenomics** | spine stamps `lane:<tier>` labels using tokenomics-named tiers; never ships default lane names |
| Where tracked state lives (issues, milestones, deferral records) | **recursive-spine** | plumb-line's repo aliases the deferral label as `audit-deferral` — aliasing is the sanctioned pattern |

## The homographs (deliberate, disambiguated)

- **handover** (recursive-spine): a finished unit filing its debt issues
  before its own issue closes. About *state*.
- **handoff** (tokenomics): a down-tier work spec a cheaper model can
  execute without re-derivation. About *economics*.
- **handoff** (plumb-line): the skill-to-skill baton pass
  (method → bootstrap → audit → remediate). About *flow inside one
  plugin*; never crosses a plugin boundary.
- **spine** (plumb-line, internal): null-result expressibility — "we
  found nothing" must be a first-class, shippable outcome. Unrelated to
  the recursive-spine plugin, which is named for a different spine
  (the one that holds the work upright). Yes, we noticed. No, neither
  is renaming.

## The patterns worth copying

- **Aliasing over forking** (deferral labels): the convention names a
  default, an adopting repo may alias it, and the alias is recorded in
  that repo's dialect note. One concept, local dialects, no drift.
- **Interview over defaults** (lane names): where a concept's *values*
  are the builder's own (their model tiers), the tool asks and stamps
  exactly what it hears. Ship the pattern, never the answer.
- **Offers over requirements** (cross-plugin wiring): a skill may
  detect a sibling and offer its bootstrap; absence is never an error,
  and declining is recorded, not retried.
