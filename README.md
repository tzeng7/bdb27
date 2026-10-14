# NFL Big Data Bowl 2027

Work for the [NFL Big Data Bowl 2027](https://www.kaggle.com/competitions/nfl-big-data-bowl-2027) on Kaggle.

## The challenge

**Theme: Combine to NFL Performance.** Find non-obvious, actionable links between 10 Hz sensor tracking data from Combine drills and regular-season NFL game performance.

For example: how a receiver decelerates into a break during a Combine route drill vs. the separation they get in games, or how a lineman's first step in agility drills relates to pass-rush or pass-pro results.

- **Submission:** a Kaggle Writeup (≤ 2,000 words, < 10 tables/figures) with an attached public Kaggle Notebook. It must use the player tracking data and link Combine tracking to NFL game performance.
- **Scoring:** Football 30% · Data Science 30% · Writeup 20% · Data Visualization 20%.
- **Tracks:** Open, and University (undergraduates only).

| Date | Milestone |
| --- | --- |
| Oct 6, 2026 | Competition start |
| **Jan 6, 2027** | **Final submission deadline** (11:59 PM UTC) |
| Jan 7 – 25, 2027 | Judging |
| Jan 26, 2027 | Results announced |

## Data

The data covers 510 rookies drafted or signed in 2023–2025: 9 CSV files, about 2.2 GiB total. License: CC BY-NC 4.0.

| File | What it contains | Keys |
| --- | --- | --- |
| `players.csv` | Bio, college, and draft info | `nfl_id` |
| `combine_results.csv` | Measurements, drill times, NGS prospect scores | `nfl_id`, `draft_year` |
| `combine_tracking.csv` | 10 Hz tracking for 6,310 Combine drill attempts (player + ball) | `event_id`, `nfl_id` |
| `player_career_successes.csv` | Career snaps, games, starts, All-Pro and Pro Bowl selections | `nfl_id` |
| `player_play.csv` | Per-play NGS and play-by-play stats (316,338 rows) | `game_id`, `play_id`, `nfl_id` |
| `games.csv` | Schedule and matchups for 1,002 games | `game_id` |
| `game_tracking_{2023,2024,2025}.csv` | 10 Hz in-game tracking for the rookie cohort | `game_id`, `play_id`, `nfl_id` |

`nfl_id` joins the Combine side to the NFL side. See the [Kaggle data page](https://www.kaggle.com/competitions/nfl-big-data-bowl-2027/data) for full column definitions.

### Download

Join the competition on Kaggle first, then use the [Kaggle CLI](https://github.com/Kaggle/kaggle-api):

```bash
kaggle competitions download -c nfl-big-data-bowl-2027 -p data/
```

```bash
unzip data/nfl-big-data-bowl-2027.zip -d data/
```

Keep `data/` out of git. The files are about 2.2 GiB.
