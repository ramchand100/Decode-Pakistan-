# Script Structure

## Sections

1. **Hook** (0:00-0:15) — one of the patterns from `hook-patterns.md`, verbatim as spoken.
   Optionally preceded by a vox-pop/news-montage or cryptic-quote cold open if real footage or
   a genuinely disorienting quote exists for this story.
2. **Context** (0:15-1:30) — the minimum background a viewer needs to feel the stakes of what's
   coming. Not a full history — only what's load-bearing for the story. If a fact doesn't change
   how the viewer understands the payoff, cut it. End context with a **question stack**: 2-4
   direct questions, said out loud, that the rest of the video will answer in order ("How did
   this actually happen? Who benefited? And what does it mean for you?"). This works as a
   spoken table of contents — it tells the viewer explicitly what they're staying for, which
   reduces drop-off in the middle of a long explainer. If the episode is sponsored, the natural
   slot is right here — after the question stack, before the real explaining starts — framed as
   a personal problem/solution story rather than a hard ad break. Mark it as
   `[SPONSOR SLOT]` in the draft and leave it for the user to fill in or skip.
3. **Escalating narrative** (the bulk of the video) — broken into beats, each one raising the
   stakes or resolving a question the previous beat raised. Mark each beat with a short heading
   for the writer/editor's reference (these aren't spoken on camera). A beat that could be
   deleted or reordered without breaking the logic is a sign the section is a list, not a
   narrative — restructure it. Three techniques worth reaching for in this section:
   - **Chain-of-mechanism escalation.** For a topic with several dependent causes (A enables B
     enables C), don't explain them all at once — treat each link as its own mini-beat with a
     small hook and payoff of its own, so the narrative climbs a staircase instead of dumping a
     diagram. This is the natural shape for economic and policy topics especially.
   - **Historical-pattern-then-exception.** State what has reliably happened in similar past
     situations (briefly, 2-3 examples), then pivot to how this time broke the pattern. The
     established pattern makes the exception feel significant instead of arbitrary.
   - **Mystery-reveal beat.** Mid-narrative, pose a question the viewer wouldn't have thought to
     ask on their own ("but someone has to be on the other side of this trade — who?"), then
     answer it with a specific, sourced figure. Use sparingly — one strong reveal beat per script
     is usually enough; more than that and it stops feeling like a discovery.
   - **Before/after recompute.** When explaining a change to a rate, margin, or ratio, set up
     one simple formula with baseline numbers first, then rerun the *same* formula with a single
     changed input after the inciting event. Watching one number move through a formula the
     viewer already understands makes an abstract shift (a margin compressing, a ratio blowing
     out) concrete in a way that just stating "it dropped from X% to Y%" doesn't.
   - **Comfort-range framing.** For a metric that has an official or expected safe range (a
     regulator's target, an industry norm), state that range explicitly before giving the actual
     number, so the viewer can place the figure as clearly fine, clearly alarming, or recovering
     — rather than having to guess whether a number is good or bad in isolation.
   - **Numbered root-cause structure.** For a story with several genuinely independent causes
     feeding one outcome, name and count them up front ("three things went wrong here") and give
     each its own mini-arc — its own mechanism explainer, its own worked example — before
     converging them in the payoff. This is the right shape when the causes are parallel rather
     than sequential (unlike chain-of-mechanism escalation, where each cause enables the next).
   - **Persona translation.** After explaining a mechanism abstractly (with invented names and
     round numbers, see "Worked numeric examples" below), retell the consequence through one
     relatable illustrative persona actually living through it — a saver, a small business
     owner, a commuter. The abstract mechanism becomes a stake the viewer can feel. Keep this
     persona clearly hypothetical/illustrative, distinct from real named people in the story.
4. **Payoff/insight** (near the end) — the point of the whole video, stated directly. This is
   the line a viewer would quote back if summarizing the video to a friend. If you can't state
   it in one or two sentences, the narrative probably hasn't actually built to anything yet. A
   **synthesis-contrast line** — naming what two different actors did and why, in parallel
   structure ("Group A did X because [reason]; Group B did Y because [different reason]") — is
   often the cleanest way to land this, because it turns the whole video into one quotable
   sentence. If the topic has genuine, unresolved disagreement about what happens next (e.g. two
   analysts or institutions with different forecasts), name both positions rather than picking a
   winner, then let the payoff be the *mechanism* the viewer now understands, not a prediction.
   For a numbered-root-cause script, the natural alternative is a **convergence payoff**:
   naming how the separate causes compound into one abstract consequence (a trust problem, a
   structural squeeze), paired with a short line on why that abstraction matters more than any
   single cause on its own.
5. **CTA** (last 10-15 seconds) — a short, consistent sign-off (thanking the viewer, a like/
   subscribe ask, a one-line description of what kind of episode this channel makes) is a
   perfectly normal default and doesn't need to be reinvented every episode. Use an
   episode-specific CTA (pointing to a related past or upcoming video) when there's a natural
   one available, but don't force it — a plain, consistent sign-off is what most channels in
   this genre actually use most of the time.

## Worked numeric examples

When a beat explains a mechanism rather than a specific real event (how bond yields move, how
a subsidy gets passed through a supply chain), it's often clearer to walk through one small,
round, invented example than to use real figures — real numbers carry decimal noise that
obscures the mechanism, and round numbers are easier to hold in your head while listening.
Give the illustrative actors names so pronouns stay unambiguous, and mark the example clearly
so it's never mistaken for a real cited figure, e.g. a spoken "let's say" framing plus an
on-screen note like "for illustration only." Switch back to real, sourced numbers as soon as
the mechanism is established and you're back to describing the actual event. Once the
mechanism is set up this way, consider a **persona translation** beat right after it (see the
escalating-narrative techniques above) to carry the abstraction into a felt consequence.

## Citations

Every non-obvious factual claim gets an inline bracketed source right after the sentence, e.g.
`[Dawn, 12 Jan 2023]`, `[SBP Annual Report 2022]`, `[company 10-K]`. If a claim can't be
verified, mark it `[NEEDS SOURCE]` instead of dropping it or inventing a citation — the user
needs to see exactly what still needs checking before recording.

## Formatting

Write scripts in markdown with section headings, spoken lines as plain paragraphs, and beat
headings as `###` subheadings so they're visually distinct from what's actually read aloud.

## Worked example (short, illustrative)

```markdown
# Episode: How One Contract Nearly Broke Pakistan's Textile Industry

## Hook
On a Tuesday morning in October 2008, the founder of one of Pakistan's largest textile
groups signed a single contract that would wipe out three family fortunes within eighteen
months. This is how it happened — and what it reveals about an industry nobody saw coming.

## Context
Pakistan's textile sector was, at the time, the country's largest export earner, built on
decades of cheap cotton and cheap labor [NEEDS SOURCE: export share figure]. But by 2008,
a handful of large mills had started doing something the sector hadn't done before: betting
on cotton prices directly through futures contracts, rather than just processing whatever
cotton cost that season.

## Escalating narrative

### The bet
[beat content — what the contract was, why it looked smart at signing]

### The turn
[beat content — what changed in global cotton markets, and why it hit fast]

### The unraveling
[beat content — the specific mechanism that turned a bad quarter into a collapse]

## Payoff/insight
The mills didn't fail because they took a risk — they failed because they took a risk that
was invisible to everyone *outside* the finance department, including their own boards. That
gap between who takes the risk and who understands it is still how Pakistani industrial
groups get blindsided today.

## CTA
If you want to see how this same blind spot played out in banking, not textiles — that's
next week's episode.
```
