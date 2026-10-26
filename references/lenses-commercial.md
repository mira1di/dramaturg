# Commercial & screen-derived lenses

Load when: the profile marks the work as genre or commercial fiction, a screenplay or series written to industry norms, or the author explicitly asks for one of these models; also when scene-level turn analysis is needed in any work (McKee's scene turn and Swain's scene/sequel are usable at scene level even in literary work).

**Warning. These models encode the norms of commercial cinema and genre publishing: a single goal-driven protagonist, escalating conflict, beats at fixed positions, a climax near the end. Large language models already drift toward this shape (Tian et al., EMNLP 2024: homogeneously positive arcs, early climaxes, "Man in Hole" overused). Any norm from this file must be named to the author (at the checkpoint or in the finding that uses it) before use, and must never be applied silently to literary, non-linear, cyclic or situation-driven work. Beat positions are located questions ("what happens around here, and is that a choice?"), never violations.**

## Index

- McKee — *Story* · Story Grid — Coyne · Save the Cat — Snyder / Brody · Hero's Journey — Campbell / Vogler · Story circle — Harmon · Paradigm & sequence approach — Field / Gulino · Scene & sequel — Swain · MICE quotient — Card / Kowal · Try-fail cycles & yes-but / no-and · Promises, progress, payoff — Sanderson · Character arcs — Weiland · Story spine — Adams
- Combining

---

### Scene turn, gap, controlling idea — Robert McKee, *Story* (1997)
- **Core:** every scene should turn a value-charged condition (life/death, love/hate, freedom/slavery) from positive to negative or the reverse; a scene that does not turn is a non-event. Story advances through the gap between what a character expects an action to produce and what the world returns. The controlling idea states the value at stake plus its cause, in one sentence. The story triangle distinguishes archplot (active single protagonist, causality, closed ending), miniplot (internal conflict, multiple protagonists, open ending) and antiplot (coincidence, non-linear time, inconsistency) — this triangle is useful for literary work as a way to place the work, not to correct it.
- **Ask (plan):** Which value is at stake in each unit, and what is its charge at entry and exit? Where on the arch/mini/anti triangle does this work sit — and does the plan honour that position consistently? Can the controlling idea be stated in a sentence, and is ambiguity intended?
- **Ask (text):** Quote the moment where the value flips; if none, is the scene a non-event or a deliberate stillness? Quote the expectation and the result that splits from it. Where does a scene end with the same charge it began with?
- **Flags:** `NON_TURNING_SCENE` — value charge unchanged with no stillness intent. `NO_GAP` — results match expectations; nothing surprises the character. `TRIANGLE_DRIFT` — the work wobbles between archplot and antiplot without design.
- **Use when / set aside when:** use for scene-level turn analysis in any form; set aside the one-sentence controlling idea when the profile declares sustained ambiguity.

### Five commandments, value shift — Shawn Coyne, *The Story Grid* (2015)
- **Core:** each unit of story (beat, scene, sequence, act, whole) should contain an inciting incident, progressive complications culminating in a turning point, a crisis (a dilemma: best bad choice or irreconcilable goods), a climax (the choice made) and a resolution. Each unit shifts a value. Global genre determines obligatory scenes and conventions.
- **Ask (plan):** For each chapter or act: what dilemma does someone face, and what do they choose? Which genre does the author claim, and which obligatory scenes does that genre's reader expect?
- **Ask (text):** Quote the crisis question (or show it is implicit). Quote the choice. Where does a turning point come from coincidence rather than action or revelation?
- **Flags:** `NO_CRISIS` — no real dilemma; the choice is obvious. `MISSING_OBLIGATORY_SCENE` — only when the profile accepts the genre contract. `GENRE_FIRST_DISTORTION` — the analysis forces a genre onto a work that does not claim one.
- **Use when / set aside when:** use the five commandments as a scene-level check in commercial and genre work; set aside genre-first diagnosis for literary or hybrid works unless the author names a genre.

### 15 beats — Blake Snyder, *Save the Cat!* (2005); Jessica Brody, *Save the Cat! Writes a Novel* (2018)
- **Core:** fifteen beats at approximate positions: opening image, theme stated, set-up, catalyst, debate, break into two, B story, fun and games, midpoint, bad guys close in, all is lost, dark night of the soul, break into three, finale, final image. Built for commercial feature film; Brody's adaptation extends it to novels with ten story genres.
- **Ask (plan):** Only if the author asked for this lens: around each beat position, what happens, and is it a choice or a placeholder? Is the midpoint a real shift (false victory / false defeat) or a calendar mark?
- **Ask (text):** Quote the catalyst and the protagonist's decision to act. Quote the "all is lost" moment and what dies there (literal or metaphorical).
- **Flags:** `BEAT_SHEET_FLATTENING` — the analysis is pushing a non-arc work into these beats. `PLACEHOLDER_BEAT` — a beat exists because the template wants it, not because the story needs it.
- **Use when / set aside when:** use for commercial screenplays and genre novels when the author wants market-norm feedback; set aside for literary, non-linear, ensemble, cyclic or situation-driven work, and never report beat-position deviations as defects there.

### Hero's journey — Joseph Campbell, *The Hero with a Thousand Faces* (1949); Christopher Vogler, *The Writer's Journey* (1992)
- **Core:** Campbell's monomyth: departure, initiation, return. Vogler's 12 stages for screenwriters: ordinary world, call to adventure, refusal, meeting the mentor, crossing the threshold, tests/allies/enemies, approach to the inmost cave, ordeal, reward, road back, resurrection, return with the elixir; plus archetypal functions (mentor, threshold guardian, herald, shapeshifter, shadow, trickster).
- **Ask (plan):** Is there a threshold between two worlds, and is crossing it costly? Which archetypal functions are present, and which character carries each — does one character carry several, or one function pass between characters?
- **Ask (text):** Quote the threshold crossing. Quote what is brought back (the "elixir") and show whether it changes the ordinary world.
- **Flags:** `MONOMYTH_CHECKLIST` — stages ticked without dramatic function. `FREE_THRESHOLD` — crossing costs nothing.
- **Use when / set aside when:** use for quest, adventure and mythic fantasy, or to analyse archetypal functions in any work; set aside as a sequence template for non-quest work.

### Story circle — Dan Harmon (2000s, online and in talks)
- **Core:** eight steps on a circle: a character in a zone of comfort, wants something, enters an unfamiliar situation, adapts, gets what they wanted, pays a heavy price, returns to the familiar, having changed. Designed for episodic TV; the circle's upper half is the familiar world, the lower half the unfamiliar.
- **Ask (plan):** For each episode, what is wanted and what is the price of getting it? Does the return show change, or is the series deliberately resetting?
- **Ask (text):** Quote the price paid. Quote the evidence of change on return.
- **Flags:** `NO_PRICE` — want satisfied without cost. `UNMARKED_RESET` — episodic reset that erases change without the series intending it.
- **Use when / set aside when:** use for episodic series and short fiction with a single protagonist; set aside for serialized arcs where change spans many episodes.

### Paradigm & sequence approach — Syd Field, *Screenplay* (1979); Paul Gulino, *Screenwriting: The Sequence Approach* (2004)
- **Core:** Field's paradigm: set-up, confrontation, resolution, joined by plot points that turn the action, with Act I and III roughly a quarter each. Gulino, building on Frank Daniel's teaching, divides a feature into about eight sequences of 10–15 minutes, each with its own tension and resolution.
- **Ask (plan):** What turns the story at the end of the set-up, and what launches the resolution? If thinking in sequences: what is each sequence's local question, and does its answer open the next?
- **Ask (text):** Quote the plot points. Mark each sequence's local question and where it resolves.
- **Flags:** `SAGGING_MIDDLE` — a long stretch with no sequence-level question (diagnose only when the work promises forward drive). `PLOT_POINT_NOT_TURN` — the "plot point" doesn't change direction.
- **Use when / set aside when:** use for feature screenplays to industry norms (see stage-and-screen for format); set aside for theatre, literary prose and non-linear work.

### Scene & sequel — Dwight V. Swain, *Techniques of the Selling Writer* (1965)
- **Core:** a scene runs goal, conflict, disaster; a sequel runs reaction, dilemma, decision, which sets the next goal. Alternating scenes and sequels controls tempo. At the smallest scale, motivation-reaction units order stimulus before response.
- **Ask (plan):** Where does the plan alternate action and processing, and where are sequels missing (no reaction) or bloated (no decision)?
- **Ask (text):** Quote the goal, the disaster, and the decision. Quote any place where a reaction precedes its stimulus or a stimulus has no reaction.
- **Flags:** `MISSING_SEQUEL` — consequences never processed. `SEQUEL_WITHOUT_DECISION` — reflection that leads nowhere. `MRU_ORDER` — reaction shown before its cause, unintentionally.
- **Use when / set aside when:** use for pacing inside goal-driven episodes; set aside where interiority is the main action or the work is situation-driven.

### MICE quotient — Orson Scott Card (*How to Write Science Fiction and Fantasy*, 1990, attribution uncertain); nesting developed by Mary Robinette Kowal
- **Core:** four kinds of story threads: Milieu (enter and leave a place), Inquiry (a question asked and answered), Character (dissatisfaction with identity, resolved or not), Event (the world's order disrupted and restored or re-made). Kowal's extension: threads open and close in nested order — first opened, last closed.
- **Ask (plan):** Which threads does the opening open, in what order? Does the ending close them in reverse order? Which thread is the spine, and does the ending close that one last?
- **Ask (text):** Quote where each thread opens and where it closes. Mark threads that never close.
- **Flags:** `UNCLOSED_THREAD` — opened, never closed, without intent. `NESTING_CROSSED` — threads close out of order, muddying the ending. `WRONG_ENDING_THREAD` — the ending resolves a thread other than the one promised.
- **Use when / set aside when:** use for frame narratives and multi-thread works as bookkeeping (any form); set aside the nesting rule when the work deliberately leaves threads open.

### Try-fail cycles & yes-but / no-and — Brandon Sanderson's lectures; Writing Excuses (attribution uncertain)
- **Core:** a character attempts, fails, and tries again with escalating cost; attempt outcomes are best as "yes, but" (success with a complication) or "no, and" (failure that worsens things), avoiding flat "yes" or flat "no".
- **Ask (plan):** For each major attempt, what is the outcome type? Where does a flat success remove pressure too early?
- **Ask (text):** Quote the attempt and its result; label it yes-but, no-and, flat yes, flat no.
- **Flags:** `FLAT_YES` — success without complication. `FLAT_NO` — failure without consequence.
- **Use when / set aside when:** use for goal-driven protagonists; set aside where agency is suspended by design (stillness, fatalism shown as theme).

### Promises, progress, payoff — Brandon Sanderson's lectures (BYU creative writing course, recorded 2020)
- **Core:** the opening promises a kind of story (tone, genre, questions); the middle must show measurable progress on those promises; the ending must pay off what was promised, not something else.
- **Ask (plan):** What does the first chapter or scene promise? How does the reader know progress is being made? Does the ending pay off that promise?
- **Ask (text):** Quote the opening promise. Quote the payoff. Where does the work break a promise without converting it into a deliberate subversion?
- **Flags:** `BROKEN_PROMISE` — the opening promises one story and the ending delivers another, unintentionally. `INVISIBLE_PROGRESS` — reader cannot measure movement.
- **Use when / set aside when:** use in any form as a promise audit (it is genre-neutral as stated); set aside the "progress bar" metaphor where the work's engine is pattern rather than goal.

### Character arcs — K. M. Weiland, *Creating Character Arcs* (2016)
- **Core:** three arc types. Positive: the character abandons a Lie for the Truth. Flat: the character already holds the Truth and changes the world around them. Negative: the character fails to reach the Truth, chooses a worse Lie or loses a Truth they had. Want (conscious goal) is distinguished from Need (the Truth).
- **Ask (plan):** For each major character: what Lie, what Truth, what Want, what Need — or is the character deliberately outside this scheme? Which arc type does the plan promise?
- **Ask (text):** Quote the moment the Lie is shown working, and the moment it is tested. Quote the choice that marks the arc's outcome.
- **Flags:** `UNTESTED_LIE` — the Lie is stated but never put under pressure. `ARC_TYPE_DRIFT` — a promised positive arc turns negative or flat without design.
- **Use when / set aside when:** use in character-driven work with a stated arc; set aside where the work's design rejects psychological arcs (types, functions, polyphony, cycles) — see lenses-russian and lenses-literary.

### Story spine — Kenn Adams (improv)
- **Core:** a skeleton: "Once upon a time... Every day... One day... Because of that... Because of that... Until finally... And ever since then..." — routine, disruption, causal chain, climax, new routine.
- **Ask (plan):** Can the plan be told through this spine? Where does "because of that" become "and then"?
- **Ask (text):** n/a — plan-level tool.
- **Flags:** `BROKEN_BECAUSE` — causal chain breaks.
- **Use when / set aside when:** use as a fast causality check on a plan; set aside for non-causal shapes.

---

## Combining

- Use at most two lenses from this file per diagnosis, declared up front; pair one structure lens (McKee, Story Grid, Field) with one bookkeeping lens (MICE, promises/payoff).
- For literary or non-linear work, use only scene-level tools from here (McKee's scene turn, Swain's scene/sequel, MICE nesting, promises/payoff) and take the whole-work shape from shapes.md.
- When a commercial norm and a declared shape disagree, the declared shape wins; report the commercial-norm deviation only as information, labelled as such.
- Never stack beat sheets (Save the Cat + Hero's journey + Field): they say the same thing in different words and multiply false positives.
