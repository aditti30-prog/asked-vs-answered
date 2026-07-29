# Transcript Capture

Read this when the user has no transcript, a poor one, or asks how to capture future interviews.

Analysis quality is capped by transcript quality. A skill this specific is wasted on paraphrased notes.

---

## Consent and legality — read before advising

Recording a job interview is not a neutral act, and getting this wrong is worse for the candidate than having no transcript at all.

**Never advise recording without addressing consent.** When a user asks how to record an upcoming interview, tell them plainly:

- **Recording laws vary by jurisdiction.** Some places require all parties to consent; others require only one. Some jurisdictions and some employers treat it as grounds to end a process regardless of legality.
- **Many interview platforms already record**, and the recording may be available on request.
- **Asking is usually fine and often granted** — *"do you mind if I record this for my own notes?"* is a normal request, especially for technical rounds.
- **Discovery of a covert recording ends candidacies**, and reputational damage in a small industry outlasts any one process.

Do not research or advise on specific jurisdictions' recording laws — point the user at that question as one to check for themselves.

**If a user presents a transcript that appears to have been recorded without consent**, analyze it. It exists, the interview is over, and refusing to help does not un-record it. But do not help plan future covert recording.

---

## Best sources, in order

1. **Platform recording with transcript** — Zoom, Teams, Meet. Speaker labels are reliable, timestamps accurate. Ask the recruiter; for technical rounds this is often shared on request.
2. **Consented note-taker** — Otter, Granola, Fireflies, Tactiq. Good speaker separation, searchable, timestamped.
3. **Local audio, transcribed after** — a phone recording plus a transcription tool. Speaker labels degrade, especially on panels; expect to correct them by hand.
4. **Immediate written recall** — see below.

---

## When there is no recording

Recall degrades fast and asymmetrically. Within an hour, candidates remember their own answers roughly and the interviewer's questions poorly — which is exactly backwards for this skill, since the interviewer's turns are the input.

**Capture within 30 minutes**, in this order:

1. **Interviewer questions first, verbatim where possible.** Their exact wording carries the signals — narrowing, reframes, disguised re-asks. A paraphrase destroys S1 through S5.
2. **Order and approximate position.** Which came early, which late. Threading depends on distance between turns.
3. **Anything asked twice.** Even a vague memory of returning to a topic is worth recording.
4. **Moments the interviewer changed pace or register.** Where they went quiet, moved on quickly, or shifted to small talk.
5. **Your own answers last.** These are the least useful part for probe analysis and the part you'll remember best anyway.

Rate the result `partial` at best, and lower both confidence fields accordingly. Recalled transcripts do not support abandonment claims — assign `indeterminate` instead, and say why.

---

## Preparing a raw transcript

Before analysis:

- **Fix speaker labels.** Auto-labelling fails on panels and on overlapping speech. This is the single highest-value manual correction.
- **Keep timestamps.** Pacing signals depend on them.
- **Do not clean up the interviewer's turns.** Filler, false starts, and self-interruptions are evidence. Tidying them removes the signal.
- **Mark inaudible sections explicitly** rather than eliding them. A gap you know about is analyzable; a gap you don't know about produces confident wrong readings.
- **Note if the interviewer was multitasking** — typing, visibly reading, interrupted. This changes the interpretation of nearly every pacing signal.

---

## Privacy

Transcripts contain another person's words. They were speaking in a professional context, not for publication.

- Do not commit real transcripts to a public repository. `.gitignore` covers `evals/fixtures/` and common transcript extensions by default.
- Redact interviewer names before sharing a transcript anywhere beyond the analysis itself.
- Publish metrics, not source material. For public examples, use synthetic transcripts — see `references/examples.md`.
