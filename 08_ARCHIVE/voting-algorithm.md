# Useless Stickers Voting Algorithm

## Goal

Rank stickers fairly while still allowing strong entries to win, weak entries to fall, and new/initially low seeded entries to get exposure.

sticker schema:

- id: string
- text: string
- theme: 'ai_vs_human' | 'productivity' | 'signage' | 'existential' | 'absurd' | 'meta'
- initial_score: number
- vote_count: number
- unique_votes: number
- vote_sum: number
- bayesian_score: number
- top_score: number
- top_score_date: date
- created_at: date
- updated_at: date
- status: 'draft' | 'active' | 'archived' | 'printed' | 'banned'
- author: string // user id

## 1 - Base Score (Editorial Prior)

Each sticker starts with:

- `initial_score` in `0..1000`

Interpretation:

- editorial prior
- launch bias
- fallback quality estimate before enough votes exist

Normalize once for formulas:

- `initial_prior = initial_score / 1000` (range `0..1`)

## 2 - Live Ranking (Bayesian Average)

Do **not** use raw average only (`total_points / total_votes`).

Use:

```txt
bayesian_score =
  (v / (v + m)) * user_average
  +
  (m / (v + m)) * initial_prior
```

Where:

- `v` = number of votes
- `m` = prior weight / minimum vote threshold (recommended: `50`)
- `user_average` = normalized user vote average (`0..1`)

Why:

- prevents tiny-sample dominance
- prevents permanent burial
- stabilizes early rankings

## 3 - Exploration Injection (Feed Composition)

On each page load, compose the list by buckets:

- `60%` = highest `bayesian_score`
- `25%` = random from mid-tier (weighted)
- `10%` = random from low-vote items
- `5%` = fully random

Why:

- discovery for new/underrated stickers
- less stagnation
- better long-term vote quality

## 4 - Neglect Boost (Cold Start Rescue)

If both are true:

- `votes < 10`
- `age_days > 7`

Apply temporary boost:

```txt
boosted_score = bayesian_score * 1.10
```

Use this boost only in candidate selection/ranking output, not as permanent stored score.

## 5 - Optional 1v1 Battle Mode (ELO)

For pairwise votes, maintain ELO:

```txt
expected = 1 / (1 + 10 ^ ((opponent_rating - rating) / 400))
new_rating = old_rating + K * (result - expected)
```

- `result`: `1` win, `0` loss, `0.5` tie
- `K` suggested: `16..32`

Normalize ELO to `0..1` before mixing with Bayesian.

Combined score:

```txt
final_score = 0.6 * bayesian_score + 0.4 * elo_score
```

If battle mode is disabled, use:

- `final_score = bayesian_score`

## 6 - Recommended Defaults

- `m = 20`
- `neglect_votes_threshold = 10`
- `neglect_age_days = 7`
- `neglect_multiplier = 1.07`
- feed split: `55/25/15/5`

## 7 - Implementation Notes (For Future Me)

- Keep all internal ranking values as floats in `0..1`.
- Store `initial_score` as integer `0..1000`; derive `initial_prior` at read time.
- Recompute scores incrementally after each vote if possible.
- Keep deterministic tie-breakers (example: newer vote timestamp, then sticker id).
- Log bucket source (`top`, `mid_random`, `low_vote`, `full_random`) for analytics.
- Do not mutate base priors during runtime experiments.
- Run A/B tests on:
  - `m`
  - exploration percentages
  - ELO mix ratio (`0.6/0.4`)

## 8 - Product Outcome

This model is designed so:

- good stickers rise
- great stickers dominate
- underrated stickers still get chances
- users feel their votes matter
- curation remains controllable via `initial_score`

## 9 - Per-user vote session

We should store per-user vote session to prevent users to spam votes. Simple solution:

votes:
id
sticker_id
session_id
vote
created_at

session_id = random UUID stored in localStorage.

Then enforce: one vote per sticker per session
