# Stage, screen and series

Load when: the work (or a planned adaptation) is a play, a feature screenplay, a series/serial, or the author is moving material between prose and a performed medium. The universal axes (see `axes.md`) still apply; this file adds what changes with the medium. Russian theatre method (Stanislavsky, action analysis, event series, M. Chekhov) lives in `lenses-russian.md`; McKee, Story Grid, Save the Cat, Swain, MICE live in `lenses-commercial.md`; analytic/retrospective shapes in `shapes.md`. Cross-reference, don't restate.

## Index
- Medium switch — what moves when the medium changes
- Stage (plays) — action, subtext, entrances/exits, offstage, address, unities, Ibsen, Chekhov, Brecht, postdramatic, stage directions, casting, staging, length
- Screen (feature screenplays) — image, scene economy, sequences, page ≈ minute, setups/payoffs, montage, VO/flashback, dialogue, information economy, format
- Series — pilot, engine, A/B/C, act-outs, episode vs season, forms, cold open, arcs, bible
- Adaptation — prose ↔ stage/screen
- Plan-mode vs text-mode — what a treatment can and cannot show

---

## Medium switch

| | Prose | Stage | Screen (feature) | Series |
|---|---|---|---|---|
| Where interiority lives | Narration, free indirect speech, commentary | Deed, spoken text vs. subtext, the actor's body, address to audience | Image, cut, performance in close-up, sound; VO as exception | Same as screen, plus accumulated time with the character across episodes |
| Unit of structure | Chapter / section / scene | Act / scene / French scene (entrance-to-exit unit) | Scene / sequence / act (if any) | Cold open / act-out / episode / season |
| Time handling | Free: summary, pause, flashback, prolepsis at any speed | Present tense of the performance; past arrives through speech, memory scenes or staging devices; real time inside a scene | Elastic through cutting; ellipsis is cheap; flashback is a visible device | Real gaps between episodes/seasons; viewer memory is unreliable; recaps exist |
| What the audience cannot do | — (reader can re-read, slow down, skip) | Re-hear a line, pause, look back; they see the whole stage at once and choose where to look | Re-watch (in cinema), slow down; they see only what the frame shows | Control order if streamed out of sequence; they may skip, binge or drop |
| What the dramaturg must ask for | Chapter map, POV plan | Cast list with doubling, stage directions, set/location plan, intended running time | Page count, scene headings, intended running time, VO/flashback plan | Format (episode length, number, ad breaks or not), season plan, bible |

Ask:
- Which medium is the work written *for*, and which medium is it secretly written *in*? (Novelistic screenplay, cinematic play, play-like novel.)
- Where in this medium does the interior life of the main figures become visible or audible?
- What does the audience lose by not being able to re-read, and does the structure compensate (repetition, clear entrances, recurring images)?

Flags:
- `MEDIUM_MISMATCH` — the text relies on tools its medium lacks (narratorial comment in a screenplay, internal monologue as stage direction, simultaneous action in a play with no staging solution).
- `UNSTAGED_INTERIORITY` — key turns happen only inside a character's head and nothing playable or visible carries them.
- `NO_FORMAT_FACTS` — diagnosis requested without length, running time or format; ask before judging pace.

---

## Stage (plays)

**Action through dialogue and deed**
- On stage, speech is action: every line should do something to someone (persuade, wound, hide, test, seduce, stall). Information-only lines are dead weight unless the act of telling is itself the action.
- Track what each figure *does* with words, not what they *say*. A scene where everyone explains and nobody acts on anyone is a reading, not a scene.
- Through-line per role and the supertask: see `lenses-russian.md` (Stanislavsky). For plays, check that every role with lines has its own through-line, not only the protagonist.
- Event analysis (event series, the initial/main/central/final event): see `lenses-russian.md` (action analysis). On stage this is the primary structural map; build it before any act-level judgement.

**Text and subtext**
- Subtext: what the figure wants or fears that the line does not say. The gap between text and subtext is where the actor works.
- Two failure modes: subtext stated aloud (characters say exactly what they feel), and subtext with no traceable want (the gap is empty, so the scene is vague, not deep).

Ask:
- In this scene, what does each figure want from the other, and which line is the nearest they come to saying it?
- Where does a line say the subtext outright? What would be lost if it stayed unsaid?

**French scenes, entrances and exits**
- A French scene runs from one entrance or exit to the next. Every entrance or exit changes the configuration: who can speak freely, who is watched, who is outnumbered, what can no longer be said.
- Map the play as a sequence of configurations. Static configurations held too long, and entrances that change nothing, are structural problems.
- Exits matter as much as entrances: who leaves, why now, and what the remaining figures can now do.

Ask:
- What does each entrance make impossible or newly possible?
- Is any figure brought on only to deliver information and leave?
- Who is on stage silent, and what does their silence do to the scene?

**Offstage events and reported action**
- Greek tragedy routinely reports the decisive violence through a messenger. Reported action is a choice, not a failure: it can be more terrible imagined than shown, it shifts focus to the listener's reaction, and it keeps the stage in the aftermath.
- Telling beats showing on stage when: the event is unstageable without diminishing it; the reaction of the listener is the real drama; the teller's bias is the point.
- Showing beats telling when the audience must witness a choice being made.

Ask:
- Which crucial events happen offstage, and is the reaction to them dramatized?
- Is the narrated event filtered through a teller with a stake in how it is told?

**Monologue, soliloquy, aside, direct address**
- Monologue: a long speech to someone present, still an action on them. Soliloquy: speech alone, thought made audible. Aside: a line the other figures do not hear. Direct address: the audience is acknowledged as present.
- Each sets a contract with the audience; mixing contracts without intent confuses the convention.
- A soliloquy should move: the figure ends in a different place from where they began (a decision, a self-deception, a reversal).

Ask:
- What convention of address has the play established, and does it hold or break deliberately?
- Does each long speech change the speaker or the listener?

**Unities and their modern use**
- Aristotle insisted on unity of action; unities of time and place were codified later by Renaissance and neoclassical critics. Treat them as tools.
- Compression into one place and one stretch of time raises pressure and makes every entrance count; breaking them buys scope at the cost of pressure.

Ask:
- What does the chosen time span and number of places cost or buy here?
- If the play spans years, what holds the action together instead of continuous pressure?

**Ibsen's retrospective technique**
- The decisive events happened before the curtain; the play is the uncovering of the past and its present consequences (analytic drama; see `shapes.md`).
- Risk: exposition dumped as backstory. Strength: each revelation is an action someone performs on someone, at a cost.

Ask:
- Who reveals each piece of the past, to whom, why now, and what does it cost them?
- Does each revelation change the present balance, or only inform the audience?

**Chekhovian undercurrent and indirect action**
- Подводное течение (undercurrent): the drama runs beneath ordinary talk and routine; the Moscow Art Theatre term is usually credited to Nemirovich-Danchenko (attribution uncertain).
- Decisive events tend to happen offstage or between acts; the stage shows waiting, everyday business and its cracks. Chekhov is reported to have said that on stage people should simply dine while their happiness is made or broken (attribution uncertain).
- Indirect action still needs pressure: the undercurrent must be traceable, otherwise it is mood without drama.

Ask:
- What is happening beneath the surface talk, and where does it break through?
- If the main events are offstage, how does the audience learn their weight?

**Brecht: epic theatre as a valid alternative**
- Epic theatre aims at the spectator's critical judgement rather than identification and catharsis. Verfremdungseffekt (estrangement): making the familiar strange so its social causes become visible (compare Shklovsky's ostranenie in `lenses-russian.md`).
- Gestus: the attitude or social relation made visible in a gesture or way of speaking.
- Brecht contrasted dramatic theatre, where one scene grows out of another, with epic theatre, where each scene stands for itself; interruptions (songs, titles, direct address) break identification on purpose.
- Do not diagnose episodic structure as a fault in a Brechtian work; diagnose whether each episode demonstrates something and whether the interruptions sharpen judgement.

Ask:
- Does the play want identification, judgement, or a deliberate alternation of both?
- What does each interruption make the audience notice that immersion would hide?

**Postdramatic and devised work** (brief)
- Lehmann's term for theatre in which the dramatic text is no longer the dominant element; image, body, space, time and presence carry the work. Plot and character axes may not apply; ask what organizes the experience instead (rhythm, repetition, image, duration, the audience's position).

Ask: If not plot, what is the governing principle of sequence, and is it consistent?

**Stage directions as dramaturgy**
- Directions are instructions to a production. Playable: what can be done, seen or heard. Unplayable: inner states, backstory, authorial commentary, metaphors no actor or designer can perform.
- Some playwrights write long literary directions on purpose (as reading text or as a style); note it rather than flagging it automatically, and check the profile.

Ask:
- Which directions carry meaning that the dialogue does not, and can a production realise them?
- Where does a direction do the actor's work (prescribing feeling) instead of setting a situation?

**Casting and doubling as meaning**
- Doubling (one actor, several roles) and cross-casting can create meaning: a production doubling Theseus/Oberon and Hippolyta/Titania links the two worlds; Caryl Churchill's *Cloud Nine* specifies cross-gender casting as part of its argument.
- Cast size is also a practical constraint; check it against the profile's target (studio, mainstream, school, radio).

Ask:
- Is the cast size intentional and producible for the intended stage?
- Could any doubling express the work's central idea?

**Staging constraints as dramaturgical choices**
- Number of locations, scene changes, simultaneous spaces, time jumps: each is a production cost and a rhythm decision. Many short scenes with set changes stall a stage play unless the staging style absorbs them.

Ask: How does the play get from one place or time to the next on stage, and does that transition carry meaning?

**Length and running time**
- Ask for the intended running time and interval placement. Pacing judgements without it are guesses. The interval is a structural point: what question carries the audience back in?

Flags (stage):
- `TALKING_HEADS` — figures explain and exchange information but do not act on each other.
- `SUBTEXT_STATED` — figures announce exactly what they feel or want; nothing left for the actor.
- `EMPTY_SUBTEXT` — the gap between line and want is untraceable; vagueness passing as depth.
- `DEAD_ENTRANCE` — an entrance or exit changes nothing in the configuration.
- `MESSENGER_FIGURE` — a figure exists only to deliver information.
- `UNDRAMATIZED_OFFSTAGE` — a decisive offstage event lands with no dramatized reaction.
- `CONVENTION_DRIFT` — address conventions (aside, direct address, soliloquy) shift without intent.
- `STATIC_SOLILOQUY` — a long solo speech ends where it began.
- `EXPOSITION_AS_BACKSTORY` — the past is narrated for the audience, not used as an action between figures.
- `UNPLAYABLE_DIRECTION` — a stage direction prescribes an inner state, backstory or commentary that no production can perform.
- `ACTOR_PRESCRIBED` — directions dictate feelings and line readings instead of situations.
- `STAGING_STALL` — location or time changes would stop the performance without a staging solution or a reason.
- `UNPRODUCIBLE_SCALE` — cast or set demands contradict the intended venue in the profile.

---

## Screen (feature screenplays)

**Visual storytelling**
- The script can only promise what the camera and microphone can record. Thoughts, memories and motives must be externalized in behaviour, image, sound or juxtaposition.
- The Kuleshov effect: an actor's neutral face reads differently depending on the adjacent shot. Meaning on screen is often made by the cut, not by the face.

Ask:
- For each key turn, what will the viewer actually see or hear that tells them it happened?
- Which action lines describe something unfilmable?

**Scene economy**
- Common screenwriting maxim: enter a scene as late as possible and leave as early as possible. Test each scene for what can be cut at the top and the tail.
- Each scene should change something; scenes that only re-establish what the viewer already knows are candidates for cutting or merging.

**Sequence approach** (optional lens)
- Frank Daniel's teaching, set out by Paul Gulino, treats a feature as roughly eight sequences, each with its own tension and resolution. Use it as a diagnostic of momentum, not as a template; skip it for works that do not build on accumulating tension.

**Page ≈ minute**
- In standard screenplay format one page plays roughly one minute. It is an approximation: dense action and sparse dialogue diverge. Use it for rough running-time estimates only.

**Setups and payoffs**
- Track every planted object, line, skill or image and where it pays off; on screen a payoff without a visible setup reads as cheating, and a setup without payoff reads as a lie the film told. See `axes.md` (axis 9) and the motif ledger in `outputs.md`.

**Montage, cross-cutting and transitions as meaning**
- Eisenstein argued for montage as collision: two shots in conflict produce a third meaning neither contains; his earlier "montage of attractions" (from theatre) built sequences out of strong shocks aimed at the audience.
- Cross-cutting creates comparison, simultaneity or suspense; a match cut asserts a link between two things. Ask what each transition claims.

Ask:
- Where does the juxtaposition of two scenes make a meaning the dialogue never states?
- Is any cross-cutting merely alternating, without comparison or pressure?

**Voice-over and flashback**
- VO is a tool when it contradicts, ironizes or adds a perspective the image cannot; it is a risk when it duplicates the image or explains what the scene already shows.
- Flashback is a tool when it changes how the present is read or arrives at the moment the present demands it; it is a risk when it stalls a present-tense line that has momentum or delivers backstory the present doesn't need.

Ask:
- Remove the VO: what does the viewer lose?
- Does each flashback change the present's meaning, or only explain it?

**Dialogue economy and subtext**
- Screen dialogue competes with the image; it tends to be shorter than stage dialogue. Subtext rules from the stage section apply, but on screen a close-up can carry what a line would on stage.

**Information economy: camera knows vs. character knows**
- Map at every point who knows what: the viewer, each character, the camera. Dramatic irony (viewer knows more) produces suspense; withheld information produces mystery and surprise.
- Hitchcock's bomb under the table (from his interviews with Truffaut): if the audience does not know about the bomb, the explosion gives a moment of surprise; if they are shown it first, the ordinary conversation above it becomes long suspense.

Ask:
- At this scene, what does the viewer know that the character doesn't, and vice versa?
- Is a surprise bought at the cost of suspense that would have served the work better?

**Format conventions** (only where they affect dramaturgy)
- Scene headings define units of place and time; a run of headings shows rhythm on the page. "We see" and camera directions are signs the writer is directing; flag only when they replace story content.

Flags (screen):
- `UNFILMABLE_INTERIOR` — a turn exists only as thought in action lines.
- `LATE_EXIT` / `EARLY_ENTRY_PADDING` — a scene runs past its change or starts long before it.
- `REDUNDANT_SCENE` — the scene re-establishes known information without change.
- `VO_DUPLICATES_IMAGE` — narration states what the image already shows.
- `FLASHBACK_STALL` — a flashback interrupts present momentum and changes nothing in it.
- `ORPHAN_SETUP` / `UNPLANTED_PAYOFF` — planted elements without payoff, or payoffs without setup.
- `MEANINGLESS_CROSSCUT` — alternation without comparison or tension.
- `SURPRISE_OVER_SUSPENSE` — information is withheld where showing it would create stronger tension (judge against the profile's intent).
- `DIRECTING_ON_PAGE` — camera instructions replace story content.
- `RUNTIME_MISMATCH` — page count far from the intended running time.

---

## Series

**Pilot obligations**
- Establish the world and its rules, the engine, the central figures, and a question that can renew itself rather than be answered once.
- Premise pilot (shows how the situation begins) vs. non-premise pilot (drops the viewer into a typical episode): ask which and why.

**Engine**
- The engine is what generates episodes: a case per week, a recurring conflict, a place that brings new people, an unresolved relationship, a mystery with layers.
- Test: can the engine produce many more episodes without repeating the same episode? If the engine is a single question, how long can it be withheld honestly?

**A/B/C stories**
- Typical episodes braid a main story with secondary ones. Check that the B and C stories comment on, mirror or complicate the A story, not merely fill time.

**Act-outs and cliffhangers**
- In ad-supported TV, act breaks sit at commercial breaks and end on a turn or question (act-outs). Streaming often drops them, but episode endings still need a reason to continue.
- Cliffhangers that are reversed cheaply at the start of the next episode erode trust.

**Episode vs. season arcs**
- Each episode should be satisfying alone and advance the season. Map what each episode closes and what it opens.
- Season arcs need midpoints that change the engine or the question, or the season sags.

**Serialized vs. procedural vs. anthology**
- Serialized: continuous story; risk of stalling and padding. Procedural: self-contained cases; risk of static characters. Anthology: new story per season/episode with a shared theme or form; the unifying principle carries the identity.

**Cold open**
- A pre-credits scene that hooks or sets the episode's question. Ask whether it is integrated with the episode or a detachable stunt.

**Character arcs over time**
- Long forms need arcs that stretch, loop or deepen without exhausting the character. A figure who completes their change in season one may have nowhere to go.
- Repetition can be intentional (the character keeps failing the same test) if each failure costs or reveals something new.

**Bible**
- A series bible typically holds: logline and engine, world rules, characters and relationships, tone, season arcs, episode templates, future seasons. Use the profile (see `profile.md`) for these fields and check the work against them.

Ask (series):
- What is the engine in one sentence, and how many distinct episodes can it generate?
- What does each episode close, and what question does it leave open?
- Which character can still change in season three?

Flags (series):
- `NO_ENGINE` — the pilot sets up a situation but nothing that generates further episodes.
- `SINGLE_USE_QUESTION` — the central question cannot be withheld honestly for the planned length.
- `FILLER_SUBPLOT` — B/C stories do not relate to the A story.
- `CHEAP_CLIFFHANGER` — act-outs or episode endings reversed without cost.
- `SEASON_SAG` — the middle of a season does not change the engine or the question.
- `EXHAUSTED_ARC` — a central figure's change is complete too early for the format.
- `DETACHED_COLD_OPEN` — the cold open has no link to the episode.
- `BIBLE_DRIFT` — episodes contradict the bible's rules without intent.

---

## Adaptation

**Prose → stage / screen**
- Externalize: narration, inner monologue and summary must become action, image, sound or speech. Each novelistic interior turn needs a playable or visible equivalent.
- Gain: simultaneity (several actions in one frame or on one stage), the actor's body and voice, image and montage, live presence.
- Cut: subplots, digressions and time spans the medium cannot hold at its length; merge minor figures.
- Fidelity check: judge against the work's designing principle and central question (see `profile.md`), not against the list of plot events. An adaptation that keeps every event but loses the principle is less faithful than one that changes events and keeps it.

**Stage / screen → prose**
- Gain: interiority, free handling of time, narratorial voice. Risk: transcribed dialogue and stage-like scenes that waste prose's tools.

Ask:
- What is the source work's designing principle, and how does the new medium carry it?
- Which source moments live only in narration, and what is their equivalent here?
- What does this medium allow that the source could not do?

Flags:
- `EVENT_FIDELITY_ONLY` — events preserved, governing principle lost.
- `UNTRANSLATED_NARRATION` — source narration carried over as VO or stage commentary without a medium-specific solution.
- `SOURCE_OVERLOAD` — more plot than the medium's length can hold.
- `TRANSCRIBED_SCRIPT` — prose adaptation of a script that keeps the script's limits.

---

## Plan-mode vs text-mode

**From a treatment, step outline, beat sheet or scene breakdown you can diagnose:**
- causality and the event series; the engine (series);
- information economy: who knows what when;
- configuration and use of figures; setups and payoffs at the plot level;
- structure and proportion (with stated page counts or running time);
- adaptation choices.

**You cannot reliably diagnose from a plan:**
- subtext, playability of lines and directions, dialogue rhythm;
- actual running time and pacing; scene economy at the level of entries and exits;
- whether interiority is externalized in practice;
- tone.

State the mode in the output. Mark plan-based judgements on these points as provisional and say what text would confirm them.

Flags:
- `PLAN_OVERREACH` — a finding about subtext, dialogue or pacing made from a plan alone.
