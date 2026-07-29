# Panel and Loop Analysis

Read this when a transcript has more than one interviewer, or when several rounds from one company are analyzed together.

A loop is not a set of independent interviews. Interviewers talk to each other before, during, and after. Probes get passed forward. Treating each room as isolated loses the strongest signals available.

## Within a panel

**Thread probes across speakers, not only within them.** Tag each probe with every interviewer who pursued it.

### Handoff

Interviewer B takes up an evidence target A already pursued. The strongest dissatisfaction signal in any transcript: A did not get what they needed, and B is taking a turn.

Requires care. Two interviewers asking about the same *topic* is not a handoff — panels routinely cover overlapping ground by design. A handoff needs the same **evidence target**, and ideally a marker that B knows A already asked (*"coming back to something Sarah raised"*, *"I want to push on that a bit more"*).

Assign `reprobe_type: panel-handoff`, importance +1, and raise interpretation confidence when an explicit marker is present.

### Declined handoff

B explicitly steps away from A's territory — *"I won't go over what you already covered"*. Evidence that A's probe resolved. Under-used and worth recording, because it is one of the few positive signals a transcript offers.

### Divergence

A and B reach visibly different readings of the same answer. Do not average them. Record both, and note that the debrief will have to reconcile them — which means the candidate's outcome may turn on which interviewer is more senior or more trusted, not on the answer.

### Role asymmetry

Panel members are rarely equal. Where inferable, note who is the hiring manager, who the skip-level, who the peer, and who the bar-raiser equivalent. An unresolved probe from the hiring manager weighs more than the same probe from a peer interviewer. Where it is not inferable, say so rather than guessing.

## Across rounds

When several rounds at one company are available, analyze each independently first, then compare.

### Forward-carried probes

A target unresolved in round 1 that reappears in round 2 was almost certainly passed forward in the debrief. This is the clearest evidence a transcript set can provide that an earlier answer did not land, and it upgrades the round-1 state from `indeterminate` to `partial` or `abandoned` retrospectively.

Say so explicitly: the later round is evidence about the earlier one.

### Escalation

Later rounds probe harder and at higher altitude. A probe unresolved in a final round is not comparable to the same probe unresolved in a screen. Weight by round, and do not read rising unresolved counts as declining performance without checking difficulty.

### Absent probes

A target pursued hard in round 1 and never raised again may mean it was resolved and marked closed — or that the loop had already decided it and stopped collecting evidence. Both are plausible; state both. In a loop that ended in rejection, the second reading deserves more weight than it usually gets.

## Tier C loops specifically

Executive rounds in a loop are often not scored against the same rubric as the earlier rounds. The MD or business head is frequently answering one question — *do I want this person in front of my clients* — while the earlier rounds tested craft.

Consequence: a Tier C round can be passed on rapport while the assessed commercial probe went unresolved, and the candidate will read the warmth as a pass. When a Tier C transcript shows high rapport and an unresolved dominant-dimension probe, name that split plainly. It is the single most common misreading candidates make of their own executive rounds.

## Output additions

Add to the Probe Map for panel or loop analysis:

```markdown
- **Pursued by:** I1, I2 (roles where inferable)
- **Handoff:** none | handoff at turn n | declined at turn n
- **Carried forward:** not applicable | from round n | to round n
- **Interviewer divergence:** none | <describe>
```

And a section:

```markdown
## Loop Dynamics
- Probes carried between rounds, with what that implies about the earlier round
- Handoffs and declined handoffs
- Where interviewers diverged
- Rapport-vs-assessment split, if present
```

## Rules

**Do not infer seniority from talk time.** Executives talk more; so do nervous junior interviewers. Use introductions, deference patterns, and who controls the agenda.

**Do not assume the debrief was accurate.** Forward-carried probes tell you what was passed on, not whether it was passed on fairly. An interviewer can mis-report a good answer.

**A single interviewer having a bad day is not a loop signal.** One distracted, multitasking, or underprepared interviewer degrades one room. Say that, and do not let it contaminate the read on the rest.
