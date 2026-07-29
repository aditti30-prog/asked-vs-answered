---
name: interview-analysis-dual-engine
description: Analyze a real interview transcript with two independent engines: (1) thread the interviewer's non-adjacent questions into underlying probes, detect re-asks, abandoned probes, pivots, and dropped threads; and (2) assess the candidate's answers for relevance, evidence, judgment, ownership, seniority, communication, and credibility. Then compare what the interviewer sought with what the candidate delivered and coach the top two gaps. Use whenever someone shares an interview transcript, recording, or notes and asks what the interviewer was testing, why a question returned, how well the candidate performed, what went wrong, whether an answer sounded senior enough, or how to prepare for the next round.
---

# Dual-Engine Interview Analysis

Most interview reviews make one of two mistakes: they grade answers without reconstructing what the interviewer wanted, or they infer interviewer dissatisfaction without evaluating whether the candidate's answer was actually strong.

This skill runs two independent engines:

1. **Probe Engine — interviewer side:** What evidence was the interviewer trying to collect, and did their behaviour suggest the probe closed, remained open, was abandoned, pivoted, or was dropped?
2. **Candidate Engine — candidate side:** How strong was the answer itself, independent of the interviewer's visible reaction?

The final diagnosis comes from comparing the two. A polished answer can miss the probe. A rough answer can still give the interviewer exactly what they needed.

## Epistemic boundary

This framework infers intent from observable behaviour. Behaviour is evidence, not certainty. Never claim access to the interviewer's private judgment or claim that one transcript finding caused the hiring outcome.

Keep two confidence fields separate:

- **Thread confidence:** confidence that multiple turns belong to the same underlying probe.
- **Interpretation confidence:** confidence in what the interviewer's behaviour meant.

## Run order

1. Normalize and quality-check the transcript — `references/transcript-formats.md`
2. Extract and thread interviewer probes — `references/probe-threading.md`
3. Map probes to likely rubric dimensions and interview context — `references/probe-rubrics.md`
4. Assign probe lifecycle states without using candidate scores
5. Score candidate answers independently — `references/candidate-assessment.md`
6. Compare probe demand with candidate delivery — `references/gap-synthesis.md`
7. Coach only the top two gaps — `references/followup-coaching.md`
8. Produce the output schema below

Read each reference only when its step is reached. Do not read every reference upfront unless the host environment requires it.

### Conditional steps

Run these only when their trigger is present:

| Trigger | Read |
|---|---|
| More than one interviewer, or several rounds at one company | `references/panel-analysis.md` — run alongside steps 2–4 |
| Three or more transcripts already analyzed | `references/cross-interview.md` — run after step 8, never instead of it |
| No transcript, poor transcript, or a question about recording future interviews | `references/transcript-capture.md` — read before step 1 |

`references/examples.md` holds a worked dual-engine example. Read it when the output schema needs grounding, or when a probe interpretation is genuinely ambiguous and a reference case would help.

Cross-interview analysis has a hard precondition: each transcript must be analyzed independently *before* comparison. Never carry a hypothesis from one transcript into the analysis of another.

## Before starting

Ask only when the answer is not already available:

1. **Is the hiring loop still open?** This determines whether coaching includes a repair message or only next-round preparation.
2. **Is there a known outcome or stated feedback?** Use it only after producing the independent analysis, then compare it with the findings.
3. **What role and interview type was this?** Ask only if it cannot be inferred from the transcript or surrounding context.

Do not ask the candidate what they think went wrong before analysis. Their theory can anchor the assessment.

If waiting for answers would prevent useful work, proceed with explicit assumptions and provide both open-loop and closed-loop coaching where necessary.

## Required output

```markdown
# Interview Assessment

## Executive Read
- **Transcript quality:** excellent | good | partial | poor
- **Interview context:** <tier/archetype and confidence>
- **Probe closure:** <x resolved, x partial, x abandoned, x pivoted, x dropped>
- **Candidate performance:** <overall band, not false precision>
- **Largest gap:** <one sentence>
- **Strongest evidence:** <one sentence>

## Read This First: Abandoned or High-Risk Probes
[Only high-confidence or materially important findings. Present competing explanations where necessary.]

## Probe Map

### [P#] <inferred evidence target>
- **Asked at:** turns [n, n]
- **Surface forms:** "<short quote>" → "<short quote>"
- **Reprobe type:** rephrase | narrow | hypothetical | counterexample | panel-handoff | disguised | none
- **Testing for:** <dimension> — <context/tier>
- **Importance:** 1–5
- **Lifecycle:** resolved | partial | abandoned | pivoted | dropped | indeterminate
- **Direct evidence:** <observable evidence>
- **Indirect evidence:** <supporting behavioural evidence>
- **Contradictory evidence:** <evidence against the interpretation, or none>
- **Competing explanations:** <brief alternatives>
- **Thread confidence:** high | medium | low
- **Interpretation confidence:** high | medium | low

## Candidate Scorecard

### [A#] Response to P#
- **Answer quality:** strong | adequate | weak | unscorable
- **Relevance:** 1–5
- **Evidence and specificity:** 1–5
- **Judgment and trade-offs:** 1–5
- **Ownership and attribution:** 1–5
- **Seniority / role calibration:** 1–5
- **Communication efficiency:** 1–5
- **Credibility:** 1–5
- **What worked:** <specific>
- **What weakened it:** <specific>
- **Missing evidence:** <what a stronger answer needed>
- **Confidence:** high | medium | low

## Demand–Delivery Gaps
[Compare each important probe with the candidate answer. Do not simply repeat scores.]

## What Closed Cleanly
[Name probes that closed and answers that were genuinely strong.]

## The One Thing
[Single highest-leverage change.]

## Coaching
[Top two gaps only, using the loop-open or loop-closed path. Include a 30-second and 90-second replacement answer when useful.]

## Outcome Comparison
[Only if outcome or feedback is known. State agreement, disagreement, or what the transcript cannot explain.]

## Confidence Notes
[Transcript limitations, ambiguous speaker labels, missing sections, or weak inference points.]
```

## Non-negotiable rules

**Keep the engines independent.** Do not call a probe unresolved because the answer scored poorly. Do not score an answer highly merely because the interviewer moved on.

**Lead with the highest-risk evidence, not a generic score.** Abandoned dominant-dimension probes, repeated unresolved probes, and panel handoffs come first.

**Never invent a thread.** Non-adjacent turns require two independent signals, except an explicit reframe, which can stand alone.

**Do not over-read silence.** Abandonment requires corroborating pacing or register change. Otherwise use `indeterminate` or `pivoted`.

**Do not use false precision.** Report performance as a band and dimension scores. Avoid claims such as “8.7/10” unless the user explicitly requests a numeric aggregate and the rubric supports it.

**Separate observation from verdict.** “The pricing probe remained unresolved” is supportable. “You were rejected because of pricing” usually is not.

**Show contradictory evidence.** If evidence cuts both ways, state it and lower interpretation confidence.

**Coach no more than two gaps.** The purpose is behaviour change, not exhaustive criticism.

**One transcript is one data point.** Diagnose recurring patterns only across multiple interviews — and only via `references/cross-interview.md`, which requires three. Two transcripts produce a hypothesis, not a pattern.

**Report strengths with the same rigor as gaps.** Name what closed cleanly and what scored well. An all-negative analysis is usually an artifact of looking only for negatives, and it is less useful to the candidate than an accurate one.

**Never advise covert recording.** If asked how to capture future interviews, read `references/transcript-capture.md` and address consent before method.
