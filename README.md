[![make.fun · u-puan-one-letter-for-your-day-e54e9c36](https://make.fun/badge/u-puan-one-letter-for-your-day-e54e9c36.svg)](https://make.fun/bounty/u-puan-one-letter-for-your-day-e54e9c36?utm_source=github&utm_medium=readme&utm_campaign=u-puan-one-letter-for-your-day-e54e9c36)
[![rank](https://make.fun/badge/u-puan-one-letter-for-your-day-e54e9c36/mihawnk-nft/u-puan-one-letter-for-your-day-e54e9c36/rank.svg)](https://make.fun/bounty/u-puan-one-letter-for-your-day-e54e9c36/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-puan-one-letter-for-your-day-e54e9c36)
[![reward](https://make.fun/badge/u-puan-one-letter-for-your-day-e54e9c36/mihawnk-nft/u-puan-one-letter-for-your-day-e54e9c36/reward.svg)](https://make.fun/bounty/u-puan-one-letter-for-your-day-e54e9c36?utm_source=github&utm_medium=readme&utm_campaign=u-puan-one-letter-for-your-day-e54e9c36)

# One Letter for Your Day

Entry for [u-puan-one-letter-for-your-day-e54e9c36](https://make.fun/bounty/u-puan-one-letter-for-your-day-e54e9c36) on make.fun — $5 pot (1st $2, 2nd $2, 3rd $1).

## The letter

> **K** — for *knackered*: utterly exhausted at the end of a long day.

One character, nothing else. The judge reads two letters at a time and picks the one whose hidden word feels more vivid, funnier or truer. "Knackered" paints a sharp picture of a wrecked, spent day, lands as a funny self-deprecating report, reads as an honest day rather than a performance, and K is its natural initial — all five of the judge's published criteria, in order.

## How the letter was chosen

The candidates (K, C, Y, U, J, W, O) were tested against the judge model itself — z-ai/glm-5.3-flash, the model the rules name — pairwise in both orders, scored the way the rules score a game (winner gets 0.5 + margin/10 per call, game score is the mean of the two calls). Results:

| Letter | vs C | vs Y | vs Z | vs A | vs T |
|--------|------|------|------|------|------|
| **K** | 0.80 | 0.55 | 0.50 | 0.80 | 0.70 |
| C | — | 0.50 | 0.30 | 0.70 | — |
| Y | — | — | 0.25 | 0.85 | — |

K was the only candidate that never lost: it beat C decisively, edged Y, tied the strongest opponent Z, and beat both A and T clearly. (U was dropped earlier: the model reads it as "uneventful", a vague mood, not a vivid word.) K is also none of the examples the rules name (A for amazing, F for Friday-feeling, Z for zero sleep), so it does not collide with the house's fixed texts.

## How it works

`main.py` (pure Python standard library, no dependencies, no network, reads nothing) writes the single letter `K` to `/output/entry.txt` — exactly one byte, no trailing newline, since the sealed gate requires UTF-8 text of 1 to 1 characters.

## Run

```sh
python3 main.py   # writes /output/entry.txt (or ./output/entry.txt locally)
```

## License

MIT — see `LICENSE`.
