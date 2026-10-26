# dramaturg: AI developmental editor for novels, screenplays and plays

**A Claude Code skill that critiques story structure, plot, character arcs, pacing, stakes and set-ups and payoffs in a manuscript or outline, with a quote for every finding, and never rewrites your prose.**

dramaturg works like a sharp, well-read first reader: a dramaturg in the theatre sense, or a developmental editor in publishing. It reads a plan, an outline, a chapter, a scene, an act, an episode or a whole manuscript, says what the work is actually doing, and shows where it fails its own design and why. It covers novels, short stories, plays, feature screenplays and TV series, in any language. It also runs a panel of AI beta readers and keeps a profile of your book, so it does not flag your deliberate choices as mistakes.

## Contents

- [Why dramaturg](#why-dramaturg)
- [Who it is for](#who-it-is-for)
- [Example requests](#example-requests)
- [Install](#install)
- [Quick start](#quick-start)
- [What it checks](#what-it-checks)
- [Modes](#modes)
- [How a review runs](#how-a-review-runs)
- [Reports, severity and solutions](#reports-severity-and-solutions)
- [The work profile](#the-work-profile)
- [Plans in Notion, Google Docs and other tools](#plans-in-notion-google-docs-and-other-tools)
- [Long manuscripts](#long-manuscripts)
- [AI beta reader panel](#ai-beta-reader-panel)
- [Story structures and critical lenses](#story-structures-and-critical-lenses)
- [Language](#language)
- [FAQ](#faq)
- [Files](#files)
- [Regression cases](#regression-cases)
- [Limits](#limits)
- [По-русски](#по-русски)
- [License](#license)

## Why dramaturg

- **It never writes your book.** No sample sentences, no rewritten paragraphs, no dialogue, names or titles. Fixes are described as operations: cut, move, reorder information, plant a motif, change who makes a choice. If you explicitly ask it to draft text, it first says that this leaves dramaturg mode.
- **Evidence or silence.** Every claim about the text carries a verbatim quote and its location, and every quote is checked against the current text before the answer. A claim without evidence is labelled an impression.
- **Your design, not a template.** It judges the work against its own intended shape (a spiral, a loop, a frame story, a braided or nonlinear structure, a form borrowed from music or dance) before any convention. Three-act structure, beat sheets and the hero's journey are used only when named and justified.
- **Honest feedback.** Findings are ranked by severity, which is set before any charitable reading. No compliment sandwiches, no softened findings, no padding to a round number.
- **It remembers your decisions.** A profile of the work holds your intent, deliberate devices, settled decisions and rejected options, so rejected ideas do not come back.

## Who it is for

- Novelists and short story writers revising a draft or testing an outline before drafting.
- Playwrights, screenwriters and series writers working on structure, scenes, episodes and seasons.
- Writers of literary, nonlinear, cyclic or quiet fiction, which conventional story-structure advice tends to misread.
- Genre writers who want feedback calibrated to market norms, when they ask for it.

## Example requests

Typed to Claude Code with the skill installed:

- "Where does chapter 3 sag?"
- "Does this scene actually turn anything, or is it a non-event?"
- "Is the twist in act two fair, or does it come out of nowhere?"
- "Check the set-ups and payoffs across the whole manuscript."
- "Is chapter 4 needed?"
- "Stress-test my outline before I start drafting."
- "Does the midpoint of my screenplay change anything?"
- "Run a beta reader panel on the opening chapter."
- "Does my series pilot have an engine for more episodes?"

## Install

The skill is a folder of Markdown files: no scripts, no dependencies, no network calls of its own.

With git, for all your projects:

```bash
git clone https://github.com/mira1di/dramaturg ~/.claude/skills/dramaturg
```

For one project only, clone it into `<project>/.claude/skills/dramaturg`. To update: `git -C ~/.claude/skills/dramaturg pull`.

With the [skills](https://github.com/vercel-labs/skills) CLI, for all your projects:

```bash
npx skills add mira1di/dramaturg -g -a claude-code
```

The skills CLI collects anonymous usage data; setting `DISABLE_TELEMETRY=1` turns it off.

Start a new Claude Code session; the skill appears as `/dramaturg`.

The beta reader panel runs its readers as Claude Code subagents (`general-purpose`). A plan or manuscript kept in Notion, Google Docs or a similar tool needs that tool's connector in Claude Code; the skill only reads through it.

## Quick start

```
/dramaturg unit chapters/03.md
```

On the first run in a project without a profile, the skill reads the project's notes and plan, pre-fills what it can, and asks at most six questions in one message: what the work is, what the reader should live through by the end, what is deliberately unconventional, what is settled, what worries you most, and where the materials live. Then it writes the profile and starts the review.

Claude can also start the skill without the slash command, on requests like the ones in [Example requests](#example-requests) or «разбери драматургию». Automatic start depends on the model's judgement; `/dramaturg` always works.

## What it checks

Fifteen diagnostic axes; each review picks the ones the question calls for and says which it skipped.

| Axis | What it looks for |
|---|---|
| Intent and design | whether the plan and the text carry out the design, or the design lives only in notes; meaning announced instead of enacted |
| Shape and proportion | the actual macro structure against the intended one; weight spent where it matters least |
| Event and turn | scenes and chapters that end where they began; recurring events that stop counting; key changes that happen offstage |
| Causality and necessity | "and then" chains instead of "therefore" and "but", removable units, convenient coincidences, motivation that arrives after the act: the usual sources of plot holes |
| Agency and choice | who chooses at each turning point; characters moved by the plot; fate or a system doing the choosing |
| Character | characters reduced to a plot function, voices that blur, change without pressure, stasis where change is needed |
| Stakes and pressure | stakes that stay abstract, a frame story with nothing at stake, tension released too early |
| Information economy | who knows what and when: suspense, mystery, dramatic irony, unfair or spent reveals, reader disorientation |
| Motif and image system | set-ups without payoffs, payoffs without set-ups (foreshadowing), decorative or accidental motifs, explained symbols |
| Theme and moral argument | mouthpiece characters, straw opponents, thesis endings, ambiguity that comes from not deciding |
| Time, narration and frame | fabula and syuzhet, time jumps without effect, point-of-view leaks, inert frames |
| Tempo and rhythm | pacing at every scale; stillness against stasis; delays that build tension against delays that stall |
| Openings and endings | the promise of the opening, unearned endings, circular endings where nothing has changed |
| World and rules | world-building rules that bend for the plot, exposition dumps, rules that cost nobody anything |
| Reader experience | what question pulls the reader forward; productive confusion against lost readers |

## Modes

The mode is inferred from the request; when the request is ambiguous, the skill asks once. It can also be named first: `/dramaturg <mode> <what to review>`.

| Mode | Give it | You get | Example |
|---|---|---|---|
| `plan` | an outline, framework, synopsis, treatment or step outline | a structural diagnosis of the design before the text exists | `/dramaturg plan outline.md` |
| `unit` | one chapter, scene, sequence, act or episode | a short reading of the unit, findings and questions | `/dramaturg unit chapters/03.md` |
| `whole` | a complete or nearly complete draft | ledgers and a whole-manuscript diagnosis, built pass by pass | `/dramaturg whole manuscript/` |
| `question` | one targeted question | a direct answer with evidence, no full report | `/dramaturg is chapter 4 needed?` |
| `brainstorm` | a wish for possibilities | questions and structural possibilities, each with its cost; never prose | `/dramaturg brainstorm what could the frame put at stake?` |
| `panel` | a unit or the whole, for reception testing | separate beta reader reports and their comparison | `/dramaturg panel chapters/01.md` |

## How a review runs

1. **Find the work and its profile.** The skill reads the profile and the sources it names, fresh in the same turn: a copy read earlier in the conversation counts as stale, because the author edits between messages.
2. **Choose the mode.**
3. **Describe before judging.** A reverse outline (for each unit: what happens, what turns, what information is released, which motifs appear, with an anchoring quote), a statement of meaning in two to four sentences, the actual shape against the intended one, and a table of story order against telling order when the chronology is nonlinear. A mismatch between the intended and the actual shape is usually the top finding.
4. **Choose the lenses.** Three to six critical lenses that fit this work and this question, plus the ones that would misdiagnose it and are set aside. In `plan` and `whole` modes the skill stops here, shows its description of the work and its choice of lenses, and asks the author to confirm or correct them.
5. **Diagnose.** Each finding gets a severity, axis, location, evidence, effect on the reader, mechanism, type, confidence and a question to the author. Every quote is found again in the current text before the answer; quotes that cannot be found are fixed or dropped.
6. **Report** in the chat.
7. **Handle pushback.** It re-checks the evidence and says either "I was wrong, because…" or "I keep the finding, because…". Disagreement or attachment is not evidence; new information is. When the author settles something, it proposes the exact line for the profile and adds it only with the author's agreement.

## Reports, severity and solutions

A report is written in the chat, never to a file. In a follow-up turn the skill answers what was asked and shows only what changed.

The order:
1. In `unit` mode, a short reading of the unit: what it seems to be doing and the assumptions behind the review, in a few lines with quotes. The full reverse outline comes on request.
2. **The main thing:** one paragraph with the diagnosis that matters most.
3. **Findings**, ranked by severity: a claim, a short quote with its location, and why it matters.
4. **What works:** short, with evidence, and only what the author must protect while revising.
5. **Questions for the author:** the open questions whose answers would change the diagnosis.
6. **Not checked:** first whether every quote was found again in the current text, then what was not read, which axes were skipped and which claims are tentative.

| Severity | Meaning |
|---|---|
| `critical` | breaks the work's own design: the intended effect cannot happen as built |
| `major` | substantially weakens a central effect; the reader will feel it |
| `minor` | a local weakness worth fixing during revision |
| `taste` | a judgement call; the author decides |

Each finding is also typed as a `defect` (it does not work and was not meant to be this way), a `device miscalibrated` (deliberate, but the execution misfires) or `taste`, and marked `confident` or `tentative`.

**Solutions.** By default a report is a diagnosis plus questions. Solutions come when the author asks for them, or by default when the profile's feedback format says so: one to three options per finding, each with what it costs and what it rules out, plus a stated preference. A solution is an intervention, never new wording: cut, merge, split or move a unit; reorder the release of information; plant or pay off a motif; change who chooses at a turning point or what the choice costs; turn an inner state into an action or an object; expand or compress a unit; change point of view, distance or frame; make a recurrence vary; open or close a thread; add a unit with a named function, such as a stillness scene or a mirror scene. A solution may also reorder or cut the author's own sentences, shown in full so they can be pasted.

## The work profile

A general critic knows craft but not your book. The profile carries what only the author knows, and every review reads it first.

**Where it lives:** `dramaturg/profile.md` in the project root, or wherever the project's `CLAUDE.md` says it lives: another path, or a section of a plan document in an external tool. A one-line pointer in `CLAUDE.md` is enough:

```markdown
The dramaturg profile is the last section, "For reviews", of the plan document <link>. Fetch it fresh with the plan before every review.
```

**What it holds:** the form, length, stage and language of the work; how feedback should address the author and whether it should include solutions by default; the intent, in the author's words; the intended structure, narration, time structure and world rules; deliberate devices, which are never flagged for existing; locked decisions; rejected options, which are never proposed again; the lenses that fit and those set aside; the sources of truth; the current focus.

**How it changes:** the author owns it. The skill proposes exact lines and writes them only after the author agrees. A locked decision may be challenged at most once, only at critical severity and with strong evidence. "Let's not decide now" is a deferral, not a decision: nothing is recorded.

## Plans in Notion, Google Docs and other tools

Many writers keep the outline or series bible in Notion, Google Docs or a similar tool, often read-only for the assistant. The skill fetches the current pages through the tool's connector before each claim about them. When the connector is unavailable, it says so and limits its claims to what it can read.

Every change it proposes to such a plan can be pasted without guessing: the location (chapter, section, bullet), the current line verbatim and the full new line, or the whole replacement section for several changes; blocks in a flat code fence with a note on which lines to indent; every old sentence checked to still be present unless removing it is the change. After the author pastes, it fetches the page again and reports what landed, what is missing and what broke.

## Long manuscripts

A whole novel is reviewed unit by unit, never from one pass or from memory. The skill builds ledgers of the outline, events, motifs, information and characters, and updates them after each unit, so later passes read the ledgers plus targeted excerpts.

- Ledgers are files in `dramaturg/ledgers/`, unless the profile or the project's `CLAUDE.md` says the work keeps no ledger files; then they exist only in the session's scratch space.
- Each ledger section names its source and the date it was built from, and is rebuilt when the source has changed since.
- Motifs, names and objects are tracked by search across the files; in inflected languages the search uses word stems.
- For parallel outlining, each subagent gets the profile and one unit, and every quote it returns is checked before use.

## AI beta reader panel

One critic in one context drifts towards agreement and towards its own first reading. The panel runs separate AI beta readers in separate contexts, in parallel:

| Reader | Gets | Reads for |
|---|---|---|
| cold | the text only: no profile, no notes, no plan | a first-time reader's path, moment by moment: orientation, predictions, confusion, where attention drops |
| hostile | the text and the profile's work and intent sections | the weakest points, especially where the work fails its own intent |
| sympathetic | the same as the hostile reader | what the work is trying to do, where it already succeeds, and where the intent is not yet realised |
| form specialist (optional) | the text and the full profile | what one tradition knows best: a literary-fiction editor, a theatre director, a script reader, a genre reader |

Every reader quotes the text for every claim and suggests no fixes. Readers get file paths; text from an external tool is saved for them first, and each reader ends its report with the list of what it opened. The dramaturg checks every returned quote, treats a problem named by both the hostile and the sympathetic reader as a strong finding, sorts the cold reader's confusion into productive and failed, and reports disagreements as they are, without averaging. Each reader is a full extra read, so by default the panel runs on one unit or a few.

## Story structures and critical lenses

The reference files load on demand, never all at once.

| File | Covers |
|---|---|
| `references/shapes.md` | macro structures: linear arc, episodic and picaresque, journey, spiral, loop, refrain, mirror and ring composition, frame story and nested frames, analytic drama, radial, countdown, braided multi-strand, mosaic, reverse chronology, mise en abyme, kishōtenketsu, stillness; forms borrowed from music, ballet and ritual: sonata form, theme and variations, rondo, fugue, symphony, suite, grand pas de deux, rite of passage, calendar |
| `references/lenses-literary.md` | Jane Alison, Gérard Genette, E. M. Forster, Peter Brooks, Charles Baxter, Percy Lubbock, James Wood, Ursula K. Le Guin, John Gardner, John Truby, Milan Kundera |
| `references/lenses-russian.md` | Lotman and Schmid on events, Tomashevsky on motifs, Shklovsky on fabula, syuzhet and estrangement, Propp, Bakhtin on polyphony and chronotope, Vygotsky, Stanislavsky, Knebel and Tovstonogov's event analysis, Michael Chekhov, Chekhov's gun |
| `references/lenses-classical.md` | Aristotle, Hegel, Lajos Egri, Freytag's pyramid, kishōtenketsu, jo-ha-kyū |
| `references/lenses-commercial.md` | Robert McKee, Story Grid, Save the Cat, the hero's journey, Dan Harmon's story circle, Syd Field and the sequence approach, scene and sequel, the MICE quotient, try-fail cycles, promises and payoffs, character arcs, the story spine |
| `references/stage-and-screen.md` | plays, feature screenplays, TV series (pilot, engine, A/B/C stories, season arcs) and adaptation between prose, stage and screen |
| `references/axes.md` | the fifteen diagnostic axes, with questions for plans and for text |
| `references/integrity.md` | severity and type scales, evidence and honesty rules, the allowed interventions |
| `references/outputs.md` | formats of findings, reverse outlines, ledgers, reports and options |
| `references/profile.md` | the intake questions and the profile template |
| `references/reader-panel.md` | the beta reader panel |

Commercial models such as beat sheets, the hero's journey and genre obligations are never applied silently. When a finding rests on one, the skill names it and says why it applies; for literary, nonlinear, cyclic or situation-driven work it uses only their scene-level tools.

## Language

The skill answers in the author's language and follows the form of address set in the profile, for example the grammatical gender used for the author in Russian. It uses the critical vocabulary native to that language; for Russian: событие, фабула и сюжет, мотив, остранение, сверхзадача, сквозное действие, исходное событие, хронотоп, полифония.

## FAQ

**Will it rewrite my manuscript?**
No. It describes what a fix must do and leaves the words to you. The one exception is reordering or cutting your own sentences, shown in full. If you explicitly ask it to draft text, it says first that this leaves dramaturg mode.

**Is it a line editor or a proofreader?**
No. It works on structure, events, characters and design. Grammar, style and sentence-level editing need a line-editing tool.

**Does it force three-act structure or Save the Cat on my book?**
No. It identifies the structure your work actually has and tests it by that structure's own logic. Beat sheets and genre conventions are used only when you ask for market calibration or the work declares them, and the skill names them when it does.

**Can it review a whole novel?**
Yes, in `whole` mode: unit by unit, with ledgers, and a checkpoint where you confirm its picture of the book before it diagnoses anything. Expect it to use many tokens; start with one chapter.

**Can it find plot holes?**
It looks for their causes: missing causal links, convenient coincidences, motivations that arrive after the act, world rules that bend for the plot, payoffs with no set-up. Each finding comes with the quotes it rests on.

**Does it work with an outline in Notion or Google Docs?**
Yes, through that tool's connector in Claude Code, read-only. Changes to the outline come as exact, paste-ready blocks.

**Which languages does it support?**
It answers in the language of the author and the work. The critical lenses include the Russian and Soviet tradition alongside English-language craft books.

**Does it work outside Claude Code?**
It is written for Claude Code. Other agents that read `SKILL.md` folders get the instructions, but the beta reader panel depends on Claude Code subagents, and `argument-hint` is read only by Claude Code and VS Code.

**Is my text sent anywhere?**
The skill has no scripts and makes no network calls of its own. Your text is processed by Claude the way it is in any Claude Code conversation.

## Files

```
dramaturg/
├── SKILL.md            the core: hard rules, workflow, gotchas
├── evals.md            regression cases, run by hand; not loaded by the skill
├── README.md
└── references/
    ├── axes.md
    ├── integrity.md
    ├── outputs.md
    ├── profile.md
    ├── reader-panel.md
    ├── shapes.md
    ├── lenses-russian.md
    ├── lenses-literary.md
    ├── lenses-classical.md
    ├── lenses-commercial.md
    └── stage-and-screen.md
```

## Regression cases

`evals.md` holds 14 cases to run by hand after editing the skill. Eight cover behaviour: comparisons backed by a check of the whole range, deferral is not rejection, open findings in a session wrap-up, the report stays in the chat, a fresh read after the author's edits, exact plan-edit blocks, where the lens choice is shown, and the shape of reports and follow-ups. Six cover triggering: three requests that should start the skill and three near misses that should not. Run each in a fresh session with a short invented chapter and a profile, and check the listed expectations.

## Limits

- The skill judges against the intent it is given. Without a profile, findings that depend on unknown intent are marked `tentative`.
- A whole-manuscript review and a beta reader panel read the text many times and use many tokens.
- Automatic start is not guaranteed; the `/dramaturg` command always works.

## По-русски

**dramaturg** — ИИ-драматург и редактор структуры для Claude Code: разбирает драматургию романа, рассказа, пьесы, сценария или сериала и никогда не пишет текст за автора. Он проверяет сюжет и фабулу, события и повороты, причинность, мотивировки, арки персонажей, ставки, экономию информации, мотивы, «ружья» и их выстрелы, тему, время, рамку и темп. Работает с планом, каркасом, главой, сценой, актом или всей рукописью. Каждое замечание подкреплено цитатой, тяжесть замечаний честная, без комплиментов. Кроме того, скилл собирает панель ИИ-читателей (холодный, придирчивый, доброжелательный) и ведёт профиль книги, чтобы не принимать задуманные приёмы за ошибки.

Его можно вызвать командой `/dramaturg` или фразами вроде «разбери драматургию», «что не так со структурой», «проверь главу», «проверь план», «где провисает», «работает ли это событие». Отвечает на языке автора; в профиле можно задать обращение, например род.

## License

[MIT](LICENSE)
