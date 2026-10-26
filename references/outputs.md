# Output formats

Load when: choosing lenses, writing findings, ledgers or a report.

## Contents
- Lens declaration
- Finding
- Reverse outline
- Fabula/syuzhet table
- Event, motif, information and character ledgers
- Reports: `question`, `unit`, `plan`, `whole` modes
- Prescription (when asked, or by default if the profile says so)

Field labels below are in English. Translate them into the author's language in the output; flag names stay in English.

## Lens declaration

Working reasoning, not a report section. Show it to the author only at the `plan`/`whole` checkpoint, when asked, or when a finding rests on an arc or commercial norm.

```markdown
**Lens declaration**
- Applied: <lens> — <why it fits this work/question>; …
- Re-scoped: <lens> — <how it is adjusted here>; …
- Set aside: <lens> — <why it would misdiagnose this work>; …
```

## Finding

```markdown
### [<severity>] <one-line claim>
- Axis: <axis> · Type: defect | device miscalibrated | taste · Confidence: confident | tentative
- Where: <file / unit / line or section>
- Evidence: "<verbatim quote>" (<location>); "<quote>" (<location>)
- Effect: <what the reader or viewer experiences or fails to experience>
- Mechanism: <why it happens, named through a lens or flag: e.g. ITERATED_NON_EVENT (Lotman/Schmid)>
- Question: <what the author must decide or clarify; omit if none>
```

No "Fix" field. Prescriptions follow SKILL.md rule 7: when asked, or by default if the profile's feedback format says so (see below).

## Reverse outline

| Unit | What happens | Turn (before → after) | Information released | Motifs | Anchor quote |
|---|---|---|---|---|---|

In `plan` mode the anchor column cites the plan section instead of a quote.

## Fabula/syuzhet table

| Fabula order (chronological) | Event | Syuzhet position (unit) | Effect of the displacement |
|---|---|---|---|

## Event ledger

| Unit | Event | Boundary crossed (from → to) | Relevant | Unpredictable | Irreversible | Non-iterative | Evidence |
|---|---|---|---|---|---|---|---|

Mark each criterion `yes`, `partly` or `no`. Mostly `no` across a recurring event means `ITERATED_NON_EVENT`.

## Motif ledger

| Motif | Occurrences (unit: short quote) | Bound / free | Dynamic / static | How its meaning shifts | Pay-off |
|---|---|---|---|---|---|

## Information ledger

| Fact | Reader learns (unit) | Character A learns | Character B learns | Effect (irony / suspense / mystery / surprise) |
|---|---|---|---|---|

## Character ledger

| Character | Wants | Lacks or fears | Structural function(s) | Key choices (unit) | Change or deliberate stasis |
|---|---|---|---|---|---|

Ledgers live in `dramaturg/ledgers/<name>.md` (or only in the session's scratch space, if the profile says the work keeps no ledger files) and are updated after each unit, with the date of the last update at the top. Each section names its source file and the date it was built; rebuild it before use if the source file changed after that date.

## Reports

Reports are written in the chat, never to a file. The finding format above is a checklist for your reasoning; in the report, compress each finding to the claim, short evidence and why it matters, plus options when the author wants solutions. The templates below list possible sections; skip any that have nothing new.

### `question` mode

A direct answer in 1–3 paragraphs, with evidence, then the open question if one remains. No full report.

### `unit` mode

```markdown
# <Unit>: dramaturg's notes (YYYY-MM-DD)
**Reading** — statement of meaning + assumptions, a few lines with quotes; the reverse outline only on request
**The main thing** — one paragraph
**Findings** — ranked
**What works** — evidenced, only what to protect
**Questions for the author**
**Not checked** — one line on quotes (all re-found in the current text, or which were not), then scope limits
```

### `plan` mode

```markdown
# <Work>: plan diagnosis (YYYY-MM-DD)
**Restatement of the design** — confirmed by the author at checkpoint, together with the lens choice
**Shape** — actual vs. intended
**The main thing**
**Findings** — ranked; each cites plan sections
**Risks for the drafting stage** — what will be hard to execute and why
**Questions for the author**
**Not checked** — one line on quotes, then scope limits
```

### `whole` mode

```markdown
# <Work>: developmental diagnosis (YYYY-MM-DD)
**Description** — whole-work outline (link to ledgers), statement of meaning, shape; confirmed at checkpoint with the lens choice
**The main thing**
**Findings by severity** — critical, major, minor, taste
**Cross-unit patterns** — what recurs across units (from the ledgers)
**What works**
**Questions for the author**
**Revision order** — which findings to address first because others depend on them (order only, no prescriptions)
**Not checked** — one line on quotes, then scope limits
```

## Prescription (when asked, or by default if the profile says so)

```markdown
**Options for <finding>**
1. <intervention class, described abstractly> — Cost: <what it takes, what it weakens>. Rules out: <what becomes impossible>.
2. …
3. …
Dramaturg's preference: <n>, because <reason tied to the work's design>. The author decides.
```
