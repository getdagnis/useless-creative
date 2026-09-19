# USELESS® — KICKSTARTER CAMPAIGN MVP STATE
## KICKSTARTER-MVP-STATE.md

> **Current state date:** 2026-09-19
>
> This document isolates the Kickstarter campaign MVP from the wider USELESS project.

---

# 1. MVP DEFINITION

The Kickstarter MVP is:

```text
ONE RED USELESS EDITION
+
ONE CORE PHYSICAL STICKER PRODUCT
+
ONE CLEAR CAMPAIGN STORY
+
ONE PARTICIPATORY VOTING SYSTEM
+
ONE STRONG VIDEO
+
CLEAR REWARDS / PRODUCTION INFORMATION
```

The campaign does not need the full long-term USELESS ecosystem.

---

# 2. WHAT THE CAMPAIGN IS SELLING

The campaign sells a curated physical collection of USELESS stickers.

The current product concept includes several packaging/reward formats but one coherent red edition.

Current working quantities:

## Large red box

```text
120 unique stickers
+
80 duplicate copies
=
200 physical stickers
```

## Small / regular box

```text
70 stickers
50 unique
```

## Soft / foil package

```text
70 stickers
50 unique
```

These are working product concepts and still require production/cost confirmation.

---

# 3. WHY THE CAMPAIGN EXISTS

The campaign is not simply:

> "Buy funny stickers."

The campaign message is:

> The world keeps optimizing humans. USELESS is a deliberate refusal to optimize everything.

The sticker collection becomes the physical manifestation of that attitude.

---

# 4. CAMPAIGN THESIS

Current core narrative:

```text
The world wants:
faster
smarter
more productive
more efficient
more optimized

↓

humans increasingly start to resemble obsolete systems

↓

USELESS chooses:
pause
glitch
inefficiency
unnecessary things
human errors
one update behind
```

Key campaign language:

- `USELESS ON PURPOSE. HUMAN ON PRINCIPLE.`
- `DOWNGRADE THE WORLD. ONE UPDATE BEHIND.`
- `WE WERE NEVER MEANT TO SCALE.`
- `THE FUTURE IS FAST. BE SLOW ON PURPOSE.`

---

# 5. CAMPAIGN HERO

A major current headline concept:

> **YOU DECIDE WHAT DESERVES TO EXIST**

This is particularly important because it connects:

```text
campaign
+
voting
+
physical selection
+
product scarcity
```

The user is not merely rating art.

The user is helping decide which stickers become physical objects.

---

# 6. CAMPAIGN VOTING MVP

The voting experience is currently the most developed interactive campaign concept.

Core loop:

```text
see sticker
↓
make decision
↓
instant next sticker
↓
repeat
```

The design should feel like a rapid judgement / survival game, not a survey.

---

# 7. VOTING CANDIDATE POOL

Target:

```text
~300 stickers
```

The pool is intentionally larger than the print selection.

Founder/editorial seed:

```text
~50–70 stickers
```

These receive a higher initial score / prior.

This provides controlled editorial influence without removing public participation.

---

# 8. CURRENT VOTING LABEL EXPLORATIONS

The sketches currently contain:

```text
SPARE IT
MUST EXIST
TERMINATE
```

Other iterations use:

```text
SPARE IT
TERMINATE
```

The exact interaction is still unresolved.

For MVP, prioritize:

```text
fast
obvious
mobile-friendly
keyboard-friendly
one decision
instant next sticker
```

Do not let the number of rating levels become a ranking-system project.

---

# 9. VOTING FEEDBACK

The voting sketches include playful post-vote messages such as:

```text
YOU SHOWED MERCY!
YOU ARE RUTHLESS!
YOU MADE THAT STICKER HAPPY
YOU MADE THAT STICKER REAL SAD
STICKER TERMINATOR STRIKES AGAIN
I'LL ASSUME THAT YOU MIS-CLICKED.
DAMN, THAT FELT SO NICE
```

This is valuable because it turns repeated voting into a game-like loop.

It should remain lightweight.

---

# 10. VOTING SCORE MODEL

The saved algorithm uses a Bayesian score.

Each sticker begins with:

```text
initial_score 0..1000
```

Then:

```text
initial_prior = initial_score / 1000
```

Live score:

```text
bayesian_score =
  (v / (v + m)) * user_average
  +
  (m / (v + m)) * initial_prior
```

Current saved baseline:

```text
m = 50
```

This is not yet implemented and should be considered a tunable setting.

---

# 11. FEED EXPLORATION

Saved feed composition:

```text
60% top
25% mid-tier random
10% low-vote
5% fully random
```

Purpose:

- winners receive exposure
- middle candidates can rise
- neglected items are seen
- new/random items are not buried

The exact percentages can be tuned after testing.

---

# 12. NEW-STICKER NEGLECT BOOST

Saved logic:

```text
votes < 10
AND
age > 7 days
```

then:

```text
candidate score × 1.10
```

This boost affects selection, not the permanent base prior.

Again: not yet implemented.

---

# 13. ELO / 1V1

A battle mode exists in the sketches:

> WHICH ONE SURVIVES?

It has:

- two stickers
- winner/loser
- score movement

The underlying algorithm uses ELO.

For Kickstarter MVP this should be considered:

**optional / non-essential.**

The first version can work entirely with single-sticker voting.

---

# 14. FINAL PRINT SELECTION

Current working rule:

```text
Top 120 → large-box unique slots

Top 50 → everywhere
```

However, the final collection should not blindly be:

```text
rank 1
rank 2
...
rank 120
```

Final editorial curation may need to balance:

- theme
- joke mechanism
- physical usability
- visual variety
- redundancy
- mockup quality
- product coherence

Voting provides evidence.

Editorial curation produces the collection.

---

# 15. CAMPAIGN PAGE

An existing complete campaign PDF exists but needs substantial redesign.

The current approach is not "polish the PDF."

It is:

```text
existing PDF
→ analyze
→ restructure
→ rebuild
→ simplify
```

The page should be treated as a long-form conversion sequence.

---

# 16. CAMPAIGN PAGE PRIORITY

The first screen should communicate:

```text
WHAT IS THIS?
+
WHY SHOULD I CARE?
+
WHAT MAKES IT DIFFERENT?
```

Then:

```text
HOW DOES VOTING WORK?
```

Then:

```text
WHAT DO I GET?
```

Then:

```text
WHY BELIEVE THIS WILL EXIST?
```

Then:

```text
WHY BACK NOW?
```

---

# 17. CAMPAIGN PAGE VISUALS

The campaign should rely heavily on:

- strong sticker mockups
- physical product shots
- packaging
- environmental placements
- red identity
- institutional typography
- concise manifesto statements

The stock mockups are not generic decorative assets.

They are part of the product proof.

---

# 18. CAMPAIGN VIDEO

Current state:

- concept exists
- production has started
- earlier master state estimated it around 30% complete

MVP requirement:

**one strong campaign video.**

It must:

- explain the premise
- establish visual world
- show product
- connect to voting
- feel credible
- reinforce the manifesto

Avoid expensive cinematic overproduction.

---

# 19. MANIFESTO DIRECTION

Current campaign manifesto structure:

```text
For years the world has tried to improve you.

Faster.
Smarter.
More productive.

Every update promises more efficiency.

We are approaching a point where
being human starts feeling like a bug.

USELESS chooses the opposite.

The glitch.
The pause.
The unnecessary.
The beautifully inefficient.

Humans 1.0.0.

In a system trying to run at 200%,
stay gloriously at 0%.
```

Exact copy is still editable.

The structure is the important part.

---

# 20. REWARDS

The reward system should make the physical product obvious before the user has to understand every conceptual layer.

Current working package hierarchy:

```text
Large red box
Regular / small red box
Soft / foil package
```

The campaign should show:

- size
- sticker counts
- unique/repeated logic where relevant
- packaging
- what becomes available at each tier

---

# 21. WEEKLY VOTER REWARD EXPLORATION

The voting sketches contain:

```text
Every week #1 voter
→ free Large Box

#2
→ free Regular Red Box

#3
→ free Foil Bag
```

This is a potentially effective participation incentive.

But it is not essential to campaign validation.

Do not build a complicated leaderboard system if a simple ranking/reward implementation cannot be done quickly.

---

# 22. USER RANKINGS

Another explored mechanic:

```text
users ranked by own score
limited daily max
+
total score of invites
```

This implies referral mechanics.

Treat as optional.

The core campaign should still function if all referral complexity is removed.

---

# 23. CAMPAIGN COUNTDOWN

The sketches include a countdown.

This can be useful as:

- urgency
- weekly ranking reset
- campaign timing

But it should remain a simple UI component.

No complex state machine is needed for MVP.

---

# 24. "WRITE YOUR OWN STICKER"

The BUILD PHASES document proposes a custom sticker idea.

Initial lightweight MVP idea:

```text
select stock image
+
place generic sticker / question prompt
+
leave a comment / idea
```

Later:

```text
type text directly into the image
```

This is strategically interesting because it can turn visitors into creators.

However:

**It is not a prerequisite for a successful campaign.**

If implementation starts competing with voting, it should be deferred.

---

# 25. MOCKUP SYSTEM

The campaign has a large stock library.

Current image categories include:

```text
AI-HIPSTER
CCTV
CLOCKS-DIGITS
DEVICE
DOOR-ENTRANCE-LOCK
ELEVATOR
FIRE-SAFETY
LIGHTS-SIGNALS
MIRRORS
Neutral
OBJECT
PHONES
PUBTRANS
SIGNS
signs-arrows
signs-exit-enter
signs-man-bike
SIGNS-STOP
STAIRWAYS
SWITCHES
URBAN-COLOR
URBAN-GOV
WC
```

This is sufficient for campaign work even before the entire 1000+ library is perfectly categorized.

---

# 26. CAMPAIGN MOCKUP QUALITY RULE

The sticker should not simply "fit the object."

It should **change the meaning of the object**.

Examples:

```text
BEWARE OF SURPRISES
→ boring waiting environment

YOU ARE BEING REPLACED
→ old analogue phone

DO NOT TOUCH THIS. IT'S ALREADY TOUCHED
→ emotionally meaningful object

THIS DEVICE DOES SOMETHING
→ obscure everyday machine
```

This should guide campaign-image selection.

---

# 27. STOCK LIBRARY STATUS

Known state:

- total library is 1000+
- roughly one-third has been manually sorted/reviewed
- sorted subset is somewhat door/sign heavy
- remaining images contain more:
  - public transport
  - old payphones
  - intercoms
  - card readers
  - CCTV
  - ticket machines
  - devices

Manual sorting can continue.

Automation is useful later but should not block campaign construction.

---

# 28. CAMPAIGN MVP DATA NEEDS

The campaign does not need the entire final metadata system to launch.

Minimum viable sticker record needs:

```text
id
text
initial/seed score
live score
status / eligibility
```

Additional metadata can support:

```text
theme
placement
targets
contexts
img_categories
pair
```

but these should only be implemented to the extent they improve actual launch workflows.

---

# 29. CAMPAIGN MVP DATABASE PRINCIPLE

Supabase is the planned backend.

The user has intentionally postponed exact database/API work until the UI sketches are complete.

That is the current preferred sequence.

The first backend should support:

```text
read sticker
submit vote
prevent/reduce duplicate voting
calculate/update score
fetch ranked candidates
```

Nothing more is required for the core loop.

---

# 30. CAMPAIGN MVP SHOULD NOT REQUIRE

No need for:

- full CMS
- advanced cache layer
- full user social system
- complex profiles
- advanced moderation UI
- creator marketplace
- ELO battles
- sophisticated referrals
- multiple editions
- black edition
- advanced custom sticker generator

unless one of these becomes unusually cheap and directly useful.

---

# 31. CAMPAIGN CONVERSION PATH

Desired visitor journey:

```text
HOOK
↓
WHAT IS USELESS?
↓
WHY DOES IT EXIST?
↓
THE STICKERS
↓
THE WORLD / VISUAL EXAMPLES
↓
YOU DECIDE WHAT DESERVES TO EXIST
↓
VOTE
↓
SEE PRODUCT / REWARDS
↓
BACK THE PROJECT
```

Voting is both an engagement mechanism and a bridge toward purchase.

---

# 32. PRIMARY CAMPAIGN STRENGTHS

The Kickstarter MVP already has:

### A distinctive concept

Not generic sticker merchandise.

### A recognizable visual system

The red institutional world is strong.

### A large product inventory

Enough material for broad selection.

### A participation story

Backers influence what becomes real.

### A strong physical-object angle

The sticker placements make the product more interesting than isolated flat graphics.

### A culturally current thesis

AI / automation / productivity anxiety creates immediate context.

---

# 33. PRIMARY CAMPAIGN RISKS

### Risk 1 — Too much explanation

The concept is smart, but the audience does not need a dissertation.

### Risk 2 — Too many stickers

The campaign should show the best, not all of them.

### Risk 3 — Voting becomes a software project

Do not overbuild the ranking system.

### Risk 4 — Mockups become literal

The environmental humor must remain.

### Risk 5 — Campaign redesign never ends

The new page needs to reach a good-enough locked state.

### Risk 6 — Production remains vague

The physical product needs credible manufacturing information.

### Risk 7 — Strong design without conversion clarity

A beautiful campaign still has to make backing obvious.

---

# 34. CAMPAIGN MVP ACCEPTANCE TEST

The MVP is ready for serious launch testing when:

```text
[ ] visitor immediately understands the concept

[ ] visitor sees the physical product

[ ] visitor sees enough sticker examples to understand quality

[ ] visitor understands voting within seconds

[ ] voting works without explanation-heavy UI

[ ] visitor can make many votes without friction

[ ] ranking is visibly meaningful but not technically distracting

[ ] reward tiers are understandable

[ ] campaign video explains the idea

[ ] campaign page presents production credibility

[ ] no critical feature depends on unfinished custom tooling

[ ] final sticker pool is clean enough for voting

[ ] mockups are varied enough to avoid visual repetition

[ ] campaign CTA is obvious
```

---

# 35. MVP CONTENT FREEZE

Before launch, freeze:

```text
edition
core visual identity
primary campaign story
reward structure
voting rules
candidate pool
campaign hero
campaign video
production assumptions
```

Do not continue rewriting the conceptual thesis while production is underway.

---

# 36. MVP SCOPE FREEZE

Explicitly postpone:

```text
BLACK EDITION
NEW MERCH
ADVANCED USER PROFILES
SOCIAL NETWORK FEATURES
FULL CUSTOM STICKER EDITOR
ELO BATTLES
COMPLEX REFERRAL SYSTEM
PERFECT IMAGE TAXONOMY
PERFECT DATA MODEL
PERFECT CMS
```

---

# 37. IMMEDIATE CAMPAIGN PRIORITIES

Based on the current state:

## Priority 1 — Finish campaign / voting UI sketches

Resolve:

- primary voting card
- controls
- result feedback
- leaderboard treatment
- reward explanation
- section hierarchy

## Priority 2 — Lock MVP interaction

Choose:

```text
single sticker
+
simple vote
+
instant next
```

and stop redesigning mechanics.

## Priority 3 — Build only required Supabase schema

Once UI is stable.

## Priority 4 — Curate campaign visuals

Use the stock library selectively.

## Priority 5 — Finish campaign page

Rebuild the PDF around the final story.

## Priority 6 — Finish video

One good video.

## Priority 7 — Finalize production

Confirm actual sticker/packaging economics.

---

# 38. CAMPAIGN NORTH STAR

The campaign should make the visitor feel:

```text
"This is strangely unnecessary."
        ↓
"That's why I like it."
        ↓
"I get the idea."
        ↓
"Let me vote."
        ↓
"I want to see what survives."
        ↓
"I want the physical thing."
```

The campaign succeeds when the visitor is not merely amused by individual stickers but becomes interested in **the USELESS world**.

---

# 39. WHAT THE MVP DOES NOT NEED TO PROVE

It does not need to prove:

- long-term community scale
- automated image classification
- advanced ranking science
- hundreds of thousands of stickers
- infinite user submissions
- multiple future editions
- a complete social identity system

It only needs to prove:

> **People care enough about USELESS to interact with it and back the physical first edition.**

---

# 40. FINAL KICKSTARTER STATE

Current campaign state:

```text
CONCEPT
████████████████████  strong

VISUAL IDENTITY
████████████████████  strong

STICKER INVENTORY
████████████████████  overbuilt

STOCK LIBRARY
████████████████████  overbuilt / partly sorted

VOTING CONCEPT
█████████████████░░░  strong / UI refinement still active

VOTING BACKEND
████░░░░░░░░░░░░░░░░  not yet built

CAMPAIGN PAGE
██████████░░░░░░░░░░  existing draft, substantial redesign needed

VIDEO
██████░░░░░░░░░░░░░░  concept + partial production

PRODUCT PRODUCTION
████████░░░░░░░░░░░░  concept established, details to finalize

LAUNCH
██░░░░░░░░░░░░░░░░░░  not yet ready
```

The bottleneck is now **execution and reduction**, not concept generation.

The best next moves are the ones that convert existing material into a launch-ready campaign without expanding the product.
