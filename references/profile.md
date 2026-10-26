# Work profile and intake

Load when: there is no profile (no `dramaturg/profile.md` and no profile section the project's CLAUDE.md points to), the profile looks stale, or the author asks to update it.

## Why a profile

A universal dramaturg knows craft but not the book. The profile carries what only the author knows: the intent, the deliberate devices, the decisions already made. Without it you will flag the work's design as its defects. Every diagnosis reads the profile first.

## Where it lives

- `dramaturg/profile.md` in the project root, unless the project's CLAUDE.md names another place: another path, or a section of the plan document (for example a section of a plan kept in an external tool). A profile kept in the plan is read with the plan, and changes to it go to the author as paste-ready blocks.
- Ledgers: `dramaturg/ledgers/`, unless the profile or the project's CLAUDE.md says the work keeps no ledger files (then they live only in the session's scratch space). Reports are never files: they go in the chat, in full.
- The author owns the profile. You propose changes inline as exact lines; you write them only after the author agrees.

## Intake

1. **Pre-fill first.** Read the project's CLAUDE.md, notes and any plan or framework files. Fill every field you can and mark those fields `inferred — confirm`. Do not invent intent; if the docs don't say, leave the field empty.
2. **Ask at most 6 questions in one message**, in the author's language, showing what you pre-filled. Core questions (skip any the docs already answer):
   1. What is it: form and medium, approximate length, and stage (plan, partial draft, full draft, revision)?
   2. By the end, what should the reader or viewer have lived through or understood? Intent, not plot.
   3. What is deliberately unconventional here (time order, unresolved ending, slow stretches, unreliable narration, missing explanations, genre mixing)? These become the false-flag list.
   4. What is fixed and not up for discussion? What have you already tried and rejected?
   5. What worries you most right now?
   6. Where do the materials live, and which source wins when they disagree?
3. **Follow-ups only if relevant:** audience or market (only for commercial work or submission), works this one is in dialogue with, how the feedback should address the author (language, grammatical gender) and what form it takes (diagnosis only or solutions by default, how long a report), anything the critique must understand before judging (a metaphysics, a world system, a formal constraint).
4. **Write the profile** from the template below, show a short summary, and start the requested work.

Intake must stay short. If the author wants to skip it, write a minimal profile (form, stage, intent if known, sources) and mark the rest `unknown`. Findings that depend on unknown fields are then marked `tentative`.

## Template

```markdown
# Dramaturg profile: <title>
Updated: YYYY-MM-DD

## Work
- Form and medium:
- Length and units (chapters / acts / episodes):
- Stage: plan | partial draft | full draft | revision
- Language of the work:
- Feedback language and address:
- Feedback format (diagnosis only or solutions by default; report length):

## Intent (author's words, quoted if possible)
- 

## Design
- Intended macro shape(s) (see shapes.md):
- Designing principle, one sentence if known:
- Narration, point of view, frame:
- Time structure (fabula vs. syuzhet):
- World rules or metaphysics the critique must understand first:
- Unit naming or borrowed form (if titles carry structure):

## Deliberate devices
Not flagged for existing; their execution and calibration are fair game.
- 

## Locked decisions
- 

## Rejected options (never re-propose)
- 

## Lenses
- Relevant:
- Set aside, and why:

## Sources of truth
- Plan or framework:
- Draft text:
- Notes:
- Which wins on conflict:

## Current focus and open questions
- 
```

## Maintenance

- After a session in which the author settled something, propose the exact lines for `Locked decisions` or `Rejected options`.
- Update `Stage` when it changes; findings calibrated for a plan are not valid for a full draft.
- If the profile contradicts the sources (the plan has moved on), say so and ask which is current before diagnosing.
- Never move something into `Locked decisions` on your own inference.
