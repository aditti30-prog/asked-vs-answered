# Dual-Engine Interview Analysis

**Reads an interview transcript from both sides at once.** One engine reconstructs
what the interviewer was trying to get. A second scores what the candidate
actually said. The diagnosis comes from where the two disagree.

Every other interview tool grades your answers. None of them grade their
questions.

---

## The problem

An interviewer asks about pricing at minute six. They don't get what they
wanted. At minute twenty-two they come back — disguised as *"what would your
first ninety days look like?"*

Nobody catches it. The two questions share no vocabulary. Three turns of your
own talking sit between them. Read one at a time, both look fine.

The worse case leaves no trace at all. An interviewer spends four turns building
to a question, doesn't get the answer, and **never asks again**. No re-ask, no
friction, nothing at that spot that looks like anything. That silence is
frequently what decided the loop.

And the case that fools everyone: **an articulate answer that misses the
question.** Single-engine analysis can't represent it. If the interviewer nodded,
the answer looks fine. If the answer was polished, the probe looks closed. You
need both engines, kept independent, to see that the candidate performed well and
still didn't deliver the evidence.

## What it does

- **Threads probes across the transcript** — seven detection signals, with a
  two-signal rule so it doesn't invent connections
- **Six lifecycle states** — resolved, partial, abandoned, pivoted, dropped,
  indeterminate. Not everything is a pass or a fail
- **Competing hypotheses required** on every abandonment claim, with
  contradictory evidence stated
- **Scores answers independently** on seven dimensions, never inferring quality
  from the interviewer's reaction
- **Synthesises the gap** between what was sought and what was delivered
- **Coaches two things** — not nine
- **Cross-interview patterns** across three or more transcripts, separating a
  real capability gap from a tier-fit problem
- **Panel and loop dynamics** — handoffs, forward-carried probes, and the
  rapport-versus-assessment split that makes executive rounds so easy to misread

## What it won't do

**It won't tell you why you were rejected.** Loops turn on internal candidates,
headcount, scope, and competing profiles — none of which appear in a transcript.
An unresolved probe is a finding, not a verdict, and the skill is written to hold
that line.

**It won't diagnose you from one interview.** Three transcripts with the same
target unresolved is a finding. Once is noise.

**It won't help you record covertly.** Consent comes before method — see
`references/transcript-capture.md`.

## Install

```bash
git clone https://github.com/<you>/interview-analysis-skill.git
cd interview-analysis-skill
mv SKILL.md CLAUDE.md
```

Open the folder in Claude Code and paste a transcript. Works with output from
Zoom, Teams, Meet, and the common note-takers, or plain text. Using Codex
instead: `mv SKILL.md AGENTS.md`.

## Layout

```
SKILL.md                          entry point, run order, output schema
references/
  transcript-formats.md           normalization and quality rating
  transcript-capture.md           getting a usable transcript; consent
  probe-threading.md              interviewer-side lifecycle engine
  probe-rubrics.md                surface question -> evidence target, by tier
  candidate-assessment.md         candidate-side scoring engine
  gap-synthesis.md                demand vs delivery
  panel-analysis.md               multi-interviewer and multi-round loops
  cross-interview.md              patterns across three or more transcripts
  followup-coaching.md            repair vs carry-forward
  examples.md                     worked dual-engine example
evals/                            methodology for testing this properly
```

## On evaluating it

`evals/` doesn't claim a model can't do this unaided. Sometimes it can. The
claim is that unaided analysis is inconsistent run to run, blind to
abandonment, contaminated across the two engines, and unstable when you push
back — and that all four are measurable.

## Privacy

Interview transcripts contain another person's words. `.gitignore` excludes
fixtures and common transcript formats by default. Don't commit real ones.


