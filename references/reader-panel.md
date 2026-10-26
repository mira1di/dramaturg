# Reader panel

Load when: `panel` mode, or the author wants to know how a unit or the whole work lands with readers or viewers.

## Why a panel

One critic in one context drifts toward agreement and toward its own first reading. Separate readers in separate contexts disagree honestly. Agreement between readers who start from opposite stances is a strong signal; disagreement is information, not noise to average away.

## Cost

Each reader is a full extra read. Run the panel on one unit or a few units by default. Run it on a whole work only when asked, and say the cost first.

## Personas

Run each as a separate subagent (Agent tool, `general-purpose`), in parallel, in one message. Pass file paths, not your own opinions or findings. If the text lives in an external tool, save this turn's fetch to scratch space and pass that path. Each reader reads only the paths given, fetches nothing else, and ends its report with the list of files and pages it opened; a cold reader that opened anything else is rerun. Every reader must quote the text for every claim and must not suggest fixes or write prose.

1. **Cold reader.** Gets only the unit text: no profile, no notes, no plan. Simulates a first-time reader or viewer. Reports moment by moment: where they are oriented or lost, what they predict, what they want to know, where attention drops, what they feel. Finishes with: what the unit was about, in their words.
2. **Hostile reader.** Gets the text and the profile's `Work` and `Intent` sections. Stance: a sharp, informed critic looking for the weakest points, especially where the work fails its own intent. No praise.
3. **Sympathetic reader.** Gets the same as the hostile reader. Stance: reads for what the work is trying to do and where it already succeeds. Must also name where the intent is not yet realized. No flattery: every claim quoted.
4. **Form specialist** (optional): a reader of this tradition, such as a literary-fiction editor, a theatre director reading for playability, a script reader, or a genre reader if the work is genre. Gets the text and the full profile. Reads only for what their tradition knows best.

## Prompt skeleton

Adapt per persona; write it in English; ask for the report in the author's language.

```
You are a <persona> reading <unit name> of a <form> in <language>.
Read: <absolute file paths>. <For hostile/sympathetic/specialist: also read <profile path>, sections ...>
Rules: quote the text (verbatim, with location) for every claim. Do not suggest fixes. Do not write or rewrite any text of the work. If you are unsure, say so.
Report:
- <persona-specific sections, see Personas>
- The three moments that mattered most to you, with quotes.
- One question you would ask the author.
Length: under <N> words.
```

## Aggregation

1. **Verify quotes.** Grep every quote the readers return; discard claims whose quotes don't match.
2. **Convergence.** A problem flagged by both the hostile and the sympathetic reader is a strong finding. A strength named by both is reliable.
3. **Confusion.** For each confusion point from the cold reader, check the profile:
   - deliberate ambiguity and the reader keeps carrying the question → productive, keep it;
   - the reader cannot tell who, where or when, or stops caring → `ORIENTATION_FAILURE`, even if the ambiguity was intended.
4. **Divergence.** Report it as such: "the hostile reader reads X as …, the sympathetic as …; the text supports both because …". Do not average.
5. **Fold into the diagnosis.** Panel results become evidence for findings in the normal format (`outputs.md`), each labelled with its source reader. The final judgement and the severity are yours, made under `integrity.md`.

## Output

```markdown
# Panel: <unit> (YYYY-MM-DD)
**Readers run** — personas and what each received
**Convergent findings** — with quotes
**Divergences** — with quotes and what the text supports
**Cold reader's map** — orientation / confusion (productive or not) / attention drops
**Dramaturg's synthesis** — findings in standard format
**Not checked**
```
