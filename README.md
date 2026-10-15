# SlopTV open data: AI video benchmark scores and prices

Open dataset behind [SlopTV](https://sloptv.co), an independent benchmark and price tracker for AI video generation.
Every model runs the same 40 fixed prompts across 10 categories (hands, faces, liquids, text, lip-sync,
camera moves and more), every clip is scored, and published prices are tracked twice a day across 17 platforms and APIs.

- **14 models** benchmarked, **558 scored clips**
- **11,541 prices** for 14 models, last read 2026-10-15
- Updated automatically every day. The git history of `data/prices.csv` is a day-by-day record of AI video prices:
  each commit's diff shows exactly which prices moved. All prices in a commit were read on the date in its message.

## Latest changes (2026-10-15)

#### Prices

- **Black Forest Labs API is now the cheapest place to run FLUX 3** at 720p and 1080p, ahead of fal.ai. [Compare](https://sloptv.co/radar/flux-3)
- **Lumeta is now the cheapest place to run MiniMax H3** at 480p ($0.0165/s), ahead of fal.ai ($0.05/s). [Compare](https://sloptv.co/radar/hailuo-h3)
- **Lumeta is now the cheapest place to run MiniMax H3** at 768p ($0.0264/s), ahead of Kie.ai ($0.04/s). [Compare](https://sloptv.co/radar/hailuo-h3)
- **Lumeta is now the cheapest place to run Seedance 2.0** at 1080p ($0.243/s), ahead of Runway ($0.32/s). [Compare](https://sloptv.co/radar/seedance-2-0)
- **Lumeta is now the cheapest place to run Seedance 2.0** at 480p ($0.0487/s), ahead of BytePlus ModelArk ($0.0673/s). [Compare](https://sloptv.co/radar/seedance-2-0)
- **Lumeta is now the cheapest place to run Seedance 2.0** at 4k ($0.545/s), ahead of Higgsfield ($0.66/s). [Compare](https://sloptv.co/radar/seedance-2-0)
- **Lumeta is now the cheapest place to run Seedance 2.0** at 720p ($0.0974/s), ahead of OpenArt ($0.132/s). [Compare](https://sloptv.co/radar/seedance-2-0)
- **Lumeta is now the cheapest place to run Seedance 2.5** at 480p, 720p and 1080p, ahead of Higgsfield. [Compare](https://sloptv.co/radar/seedance-2-5)

**New offers:**
- FLUX 3 on Black Forest Labs API: 4 variants, from $0.15/s ([radar](https://sloptv.co/radar/flux-3))
- MiniMax Hailuo 02 on Lumeta: 3 variants, from $0.011/s ([radar](https://sloptv.co/radar/hailuo-02))
- MiniMax H3 on Lumeta: 3 variants, from $0.0165/s ([radar](https://sloptv.co/radar/hailuo-h3))
- Seedance 2.0 on Lumeta: 8 variants, from $0.0256/s ([radar](https://sloptv.co/radar/seedance-2-0))

[Full list of changes](CHANGELOG.md)

[All changes, day by day](CHANGELOG.md)

Browse it on the site: [leaderboard](https://sloptv.co/leaderboard) · [price radar](https://sloptv.co/radar) · [methodology](https://sloptv.co/methodology) · [open data page](https://sloptv.co/data)

## Current leaderboard

| # | Model | Maker | Overall (0-5) | 95% CI |
|---:|---|---|---:|---:|
| 1 | [Google Gemini Omni](https://sloptv.co/model/gemini-omni) | Google | 4.91 | ±0.04 |
| 2 | [Kling 3.0 Turbo](https://sloptv.co/model/kling-3-0-turbo) | Kuaishou | 4.89 | ±0.07 |
| 3 | [Seedance 2.0](https://sloptv.co/model/seedance-2-0) | ByteDance | 4.87 | ±0.14 |
| 4 | [FLUX 3](https://sloptv.co/model/flux-3) | Black Forest Labs | 4.83 | ±0.11 |
| 5 | [Vivix W1](https://sloptv.co/model/vivix-w1) | Vivix | 4.82 | ±0.11 |
| 6 | [Seedance 2.5](https://sloptv.co/model/seedance-2-5) | ByteDance | 4.82 | ±0.15 |
| 7 | [MiniMax H3](https://sloptv.co/model/hailuo-h3) | MiniMax | 4.81 | ±0.22 |
| 8 | [OpenAI Sora 2](https://sloptv.co/model/sora-2) | OpenAI | 4.78 | ±0.17 |
| 9 | [Grok Video](https://sloptv.co/model/grok-video) | xAI | 4.74 | ±0.15 |
| 10 | [Google Veo 3.1](https://sloptv.co/model/veo-3-1) | Google | 4.67 | ±0.25 |
| 11 | [Runway Gen-4.5](https://sloptv.co/model/runway-gen-4) | Runway | 4.63 | ±0.14 |
| 12 | [PixVerse v5.5](https://sloptv.co/model/pixverse-v5-5) | PixVerse | 4.58 | ±0.16 |
| 13 | [Kling 3.0](https://sloptv.co/model/kling-3-0) | Kuaishou | 4.49 | ±0.19 |
| 14 | [MiniMax Hailuo 02](https://sloptv.co/model/hailuo-02) | MiniMax | 3.93 | ±0.47 |

Full table with sub-scores and per-category scores: [`data/leaderboard.csv`](data/leaderboard.csv). Live version: [sloptv.co/leaderboard](https://sloptv.co/leaderboard).

## Files

| File | Rows | What it has |
|---|---:|---|
| [`data/leaderboard.csv`](data/leaderboard.csv) | 14 | One row per model: overall score, 95% confidence interval, sub-scores and the score in each test category. |
| [`data/scores.csv`](data/scores.csv) | 558 | One row per scored clip: model, prompt, category, round and every judge score, with a link to the clip. |
| [`data/prices.csv`](data/prices.csv) | 11,541 | Current published prices on every platform and API we track, normalised to USD per clip and per second. |

All files are UTF-8 CSV with a header row. [`datapackage.json`](datapackage.json) describes them in the [Frictionless Data](https://frictionlessdata.io/) format.

## Columns

### leaderboard.csv

| Column | Meaning |
|---|---|
| `rank` | Position by overall score (1 = best) |
| `model` | Model name |
| `slug` | Model id, also used in https://sloptv.co/model/{slug} |
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
| `{category}` | Overall score within that test category (hands, faces, liquids, text_render, multishot, lipsync, camera, animals, style, img2video) |

### scores.csv

| Column | Meaning |
|---|---|
| `model` | Model name |
| `model_slug` | Model id |
| `prompt` | Prompt id, also used in https://sloptv.co/test/{prompt} |
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
| `model_slug` | Model id, also used in https://sloptv.co/radar/{model_slug} |
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
| `is_entry_plan` | 1 for the cheapest plan that can run the model |
| `is_best_plan` | 1 for the plan with the lowest cost per clip |
| `exact` | 1 if read directly from the published price, 0 if derived (for example scaled to another clip length) |
| `promo` | 1 if it is a time-limited promotional price |

## How the data is made

**Scores.** Each clip is scored from 0 to 5 by a vision model that sees the original prompt but not which model made the clip,
on prompt fidelity, visual quality, physics, consistency and audio. Every score below 4 is checked by hand against frames
from the clip, and lip-sync lines are checked against the audio. The prompts are frozen: if one ever changes it becomes a new
round instead of rewriting old results. Details and known limits: [methodology](https://sloptv.co/methodology).

**Prices.** What each platform publishes for a US visitor, before tax, read twice a day (06:00 and 18:00 UTC). Credit and
subscription prices are converted to dollars assuming the plan's credits are spent on that model. Moves larger than 25% are
held for a manual check before they are published. Platforms tracked: Black Forest Labs API, BytePlus ModelArk, fal.ai, Google Gemini API, Higgsfield, Higgsfield API, Kie.ai, Kling API, Luma API, Lumeta, Magnific, MiniMax API, OpenArt, Replicate, Runway, Runway API, xAI API.
How the radar works: [sloptv.co/radar](https://sloptv.co/radar).

Found an error? Open an issue or write to press@sloptv.co.

## License and attribution

[CC BY 4.0](LICENSE). Free to use, including commercially. The one condition is attribution with a link:

```html
Source: <a href="https://sloptv.co">SlopTV</a>
```

For papers, see [`CITATION.cff`](CITATION.cff) or use GitHub's "Cite this repository" button.
