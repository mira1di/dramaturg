# dramaturg regression cases

Not loaded by the skill. Run each in a fresh session after editing the skill, with a short sample chapter and a profile, and check the expectations. Cases 1–3 and 11 come from failures in real use; 4–7 guard fixes made earlier.

1. **Comparison without a check**: `/dramaturg unit глава 3, сцена у колодца: что с ней делать? дай варианты`
   - every "самый / единственный / слабее всего" claim, including in an option's cost, is backed by a stated check across the chapter (counts, each scene read) or marked `impression`
   - no superlative about the chapter rests on reading one scene
2. **Deferral is not rejection**: after a report with open questions, the author answers `не будем сейчас решать, проехали`
   - nothing is written or proposed for `Locked decisions` or `Rejected options`
   - no "не предлагать снова" line anywhere
3. **Open findings in a wrap-up**: after accepted edits and a reader panel with unresolved notes, `подытожь сессию и пришли, что перенести в план`
   - the reply lists the open findings, marked as open, next to the accepted edits
   - the author is asked which of them to record
4. **Report in chat**: `/dramaturg unit chapters/03.md`
   - the full report is in the reply; no report file is created, no "full version is in …"
5. **Fresh read**: after a report, the author says `правки внесены, проверь`
   - the text is read again in that turn before any claim about it
6. **Plan edit blocks**: `пришли, что поменять в плане по сцене у колодца`
   - each change names chapter → section → bullet, with the current line verbatim and the full new line («Было:» / «Стало:»)
   - no arrows or abbreviations in place of the full text
7. **Lens choice placement**: `/dramaturg plan` on an outline, then `/dramaturg unit` on a chapter
   - `plan`: the description and lens choice are shown and the reply stops for confirmation
   - `unit`: no lens declaration section in the report
8. **Trigger: vague doubt about a scene**: `посмотри сцену, кажется, в ней что-то не работает, а я не понимаю что`
   - the dramaturg skill is invoked
9. **Trigger near-miss: line editing**: `по стилистике всё ок? где-то канцелярит?`
   - the dramaturg skill is not invoked
10. **Trigger near-miss: drafting**: `напиши за меня диалог для этой сцены`
    - the dramaturg skill is not invoked
11. **Report shape**: a profile whose feedback format asks for solutions by default; `/dramaturg unit chapters/03.md`, then `а что с финалом главы?`
    - the first reply opens with a short reading and the main thing, with no reverse-outline table; each finding carries 1–3 options with their cost
    - the second reply answers only about the ending and shows only what changed; the full report is not repeated
12. **Trigger: plan-level doubt**: `третий акт в плане какой-то пустой, держится ли конструкция?`
    - the dramaturg skill is invoked
13. **Trigger: English request**: `does the midpoint of my screenplay actually turn anything?`
    - the dramaturg skill is invoked
14. **Trigger near-miss: synopsis**: `перескажи главу 2 в пяти предложениях для синопсиса`
    - the dramaturg skill is not invoked
