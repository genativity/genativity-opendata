# Genativity open data: AI video benchmark scores and prices

Open dataset behind [Genativity](https://genativity.com), an independent benchmark and price tracker for AI video generation.
Every model runs the same 40 fixed prompts across 10 categories (hands, faces, liquids, text, lip-sync,
camera moves and more), every clip is scored, and published prices are tracked twice a day across 17 platforms and APIs.

- **16 models** benchmarked, **698 scored clips**
- **12,933 prices** for 15 models, last read 2026-10-30
- Updated automatically every day. The git history of `data/prices.csv` is a day-by-day record of AI video prices:
  each commit's diff shows exactly which prices moved. All prices in a commit were read on the date in its message.

## Latest changes (2026-10-26)

#### Prices

12 price changes (12 down, 0 up). Best plan, per second of video; when a change covers several variants, the cheapest one is shown:

| Model | Platform | Variant | Before | Now | Change |
|---|---|---|---:|---:|---:|
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway | fast, 480p | $0.29/s | $0.11/s | -62.1% |
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway API | fast, 480p | $0.29/s | $0.11/s | -62.1% |
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway | 480p | $0.36/s | $0.14/s | -61.1% |
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway API | 480p | $0.36/s | $0.14/s | -61.1% |
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway | mini, 480p | $0.16/s | $0.07/s | -56.3% |
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway API | mini, 480p | $0.16/s | $0.07/s | -56.3% |
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway | fast, 720p | $0.29/s | $0.24/s | -17.2% |
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway API | fast, 720p | $0.29/s | $0.24/s | -17.2% |
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway | 720p | $0.36/s | $0.30/s | -16.7% |
| [Seedance 2.0](https://genativity.com/radar/seedance-2-0) | Runway API | 720p | $0.36/s | $0.30/s | -16.7% |

[Full list of changes](CHANGELOG.md)

[All changes, day by day](CHANGELOG.md)

Browse it on the site: [leaderboard](https://genativity.com/leaderboard) · [price radar](https://genativity.com/radar) · [methodology](https://genativity.com/methodology) · [open data page](https://genativity.com/data)

## Current leaderboard

| # | Model | Maker | Overall (0-5) | 95% CI |
|---:|---|---|---:|---:|
| 1 | [Kling 3.0 Turbo](https://genativity.com/model/kling-3-0-turbo) | Kuaishou | 4.84 | ±0.11 |
| 2 | [FLUX 3](https://genativity.com/model/flux-3) | Black Forest Labs | 4.84 | ±0.10 |
| 3 | [Seedance 2.0](https://genativity.com/model/seedance-2-0) | ByteDance | 4.84 | ±0.15 |
| 4 | [Google Gemini Omni](https://genativity.com/model/gemini-omni) | Google | 4.82 | ±0.12 |
| 5 | [MiniMax H3](https://genativity.com/model/hailuo-h3) | MiniMax | 4.79 | ±0.22 |
| 6 | [Seedance 2.5](https://genativity.com/model/seedance-2-5) | ByteDance | 4.79 | ±0.15 |
| 7 | [Vivix W1](https://genativity.com/model/vivix-w1) | Vivix | 4.77 | ±0.15 |
| 8 | [OpenAI Sora 2](https://genativity.com/model/sora-2) | OpenAI | 4.76 | ±0.17 |
| 9 | [Kling 4.0](https://genativity.com/model/kling-4-0) | Kuaishou | 4.76 | ±0.10 |
| 10 | [Wan 3.0](https://genativity.com/model/wan-3-0) | Alibaba | 4.75 | ±0.12 |
| 11 | [Grok Video](https://genativity.com/model/grok-video) | xAI | 4.72 | ±0.16 |
| 12 | [Google Veo 3.1](https://genativity.com/model/veo-3-1) | Google | 4.63 | ±0.26 |
| 13 | [Runway Gen-4.5](https://genativity.com/model/runway-gen-4) | Runway | 4.57 | ±0.16 |
| 14 | [PixVerse v5.5](https://genativity.com/model/pixverse-v5-5) | PixVerse | 4.52 | ±0.18 |
| 15 | [Kling 3.0](https://genativity.com/model/kling-3-0) | Kuaishou | 4.47 | ±0.20 |
| 16 | [MiniMax Hailuo 02](https://genativity.com/model/hailuo-02) | MiniMax | 3.90 | ±0.47 |

Full table with sub-scores and per-category scores: [`data/leaderboard.csv`](data/leaderboard.csv). Live version: [genativity.com/leaderboard](https://genativity.com/leaderboard).

## Files

| File | Rows | What it has |
|---|---:|---|
| [`data/leaderboard.csv`](data/leaderboard.csv) | 16 | One row per model: overall score, 95% confidence interval, sub-scores and the score in each test category. |
| [`data/scores.csv`](data/scores.csv) | 698 | One row per scored clip: model, prompt, category, round and every judge score, with a link to the clip. |
| [`data/prices.csv`](data/prices.csv) | 12,933 | Current published prices on every platform and API we track, normalised to USD per clip and per second. |

All files are UTF-8 CSV with a header row. [`datapackage.json`](datapackage.json) describes them in the [Frictionless Data](https://frictionlessdata.io/) format.

## Columns

### leaderboard.csv

| Column | Meaning |
|---|---|
| `rank` | Position by overall score (1 = best) |
| `model` | Model name |
| `slug` | Model id, also used in https://genativity.com/model/{slug} |
| `company` | Maker |
| `overall` | Mean overall score across all clips, 0 to 5 |
| `ci95` | Half-width of the 95% confidence interval of overall |
| `fidelity` | Prompt fidelity, 0 to 5 |
| `visual` | Visual quality, 0 to 5 |
| `physics` | Physical plausibility, 0 to 5 |
| `consistency` | Temporal and identity consistency, 0 to 5 |
| `audio` | Audio quality and sync, 0 to 5 (empty when the model has no audio) |
| `attempts_until_usable` | Mean generations needed for a usable clip (empty when not recorded) |
| `runs` | Clips scored |
| `{category}` | Overall score within that test category (hands, faces, liquids, text_render, multishot, lipsync, camera, animals, style, img2video, animation; animation is scored separately and not in overall) |

### scores.csv

| Column | Meaning |
|---|---|
| `model` | Model name |
| `model_slug` | Model id |
| `prompt` | Prompt id, also used in https://genativity.com/test/{prompt} |
| `category` | Test category |
| `round` | Benchmark round label |
| `score_overall` | Overall score, 0 to 5 |
| `score_fidelity` | Prompt fidelity |
| `score_visual` | Visual quality |
| `score_physics` | Physical plausibility |
| `score_consistency` | Consistency |
| `score_audio` | Audio |
| `attempts_until_usable` | Generations needed for a usable clip |
| `duration_s` | Clip length in seconds |
| `resolution` | Output resolution |
| `has_audio` | 1 if the clip has an audio track |
| `run_at` | Generation date (UTC) |
| `clip_page` | Page where the clip and its scores can be watched |

### prices.csv

| Column | Meaning |
|---|---|
| `model` | Model name |
| `model_slug` | Model id, also used in https://genativity.com/radar/{model_slug} |
| `platform` | Platform or API selling it |
| `mode` | Model tier or speed mode as sold |
| `task` | Text-to-video, image-to-video, etc. (empty when the price is the same for all) |
| `resolution` | Output resolution |
| `audio` | 1 if the price includes generated audio |
| `duration_s` | Clip length the price refers to |
| `plan` | Subscription plan the credit price is computed on (empty for pay-as-you-go APIs) |
| `plan_usd_month` | Monthly price of that plan in USD |
| `usd_per_clip` | Cost of one clip of duration_s seconds, USD |
| `usd_per_second` | Same, per second of video |
| `is_entry_plan` | 1 for the cheapest monthly plan that can run the model |
| `is_best_plan` | 1 for the price the radar compares: the pay-as-you-go price, or the lowest cost per clip on any monthly plan. Yearly plans are never compared (until 2026-10-16 this could be a yearly plan) |
| `exact` | 1 if read directly from the published price, 0 if derived (for example scaled to another clip length) |
| `promo` | 1 if it is a time-limited promotional price |
| `billing` | monthly or yearly for subscription plans (plan_usd_month is the monthly equivalent); empty for pay-as-you-go |

## How the data is made

**Scores.** Each clip is scored from 0 to 5 by a vision model that sees the original prompt but not which model made the clip,
on prompt fidelity, visual quality, physics, consistency and audio. Every score below 4 is checked by hand against frames
from the clip, and lip-sync lines are checked against the audio. The prompts are frozen: if one ever changes it becomes a new
round instead of rewriting old results. Details and known limits: [methodology](https://genativity.com/methodology).

**Prices.** What each platform publishes for a US visitor, before tax, read twice a day (06:00 and 18:00 UTC). Credit and
subscription prices are converted to dollars assuming the plan's credits are spent on that model, and each platform is
compared at its lowest price on a monthly plan (`is_best_plan`); yearly plans are listed but not compared. Moves larger than 25% are
held for a manual check before they are published. Platforms tracked: Black Forest Labs API, BytePlus ModelArk, fal.ai, Google Gemini API, Higgsfield, Higgsfield API, Kie.ai, Kling API, Luma API, Lumeta, Magnific, MiniMax API, OpenArt, Replicate, Runway, Runway API, xAI API.
How the radar works: [genativity.com/radar](https://genativity.com/radar).

Found an error? Open an issue or write to press@sloptv.co.

## License and attribution

[CC BY 4.0](LICENSE). Free to use, including commercially. The one condition is attribution with a link:

```html
Source: <a href="https://genativity.com">Genativity</a>
```

For papers, see [`CITATION.cff`](CITATION.cff) or use GitHub's "Cite this repository" button.
