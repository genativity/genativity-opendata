# Changelog

What changed in the data, day by day: price moves, new offers, new cheapest platforms, leaderboard changes and new benchmark clips. Prices are per second of video on each platform's best plan; the full detail of every change is in the commit diff.

**Last checked: 2026-10-20.** Prices are re-read twice a day; a day with no entry below is a day with no changes (nothing has moved since 2026-10-18).

By month: [2026-10](changelog/2026-10.md)

## 2026-10-18

### Prices

**New offers:**
- Seedance 2.0 on fal.ai: 12 variants, from $0.135/s ([radar](https://sloptv.co/radar/seedance-2-0))
- Seedance 2.5 on fal.ai: 9 variants, from $0.221/s ([radar](https://sloptv.co/radar/seedance-2-5))
- Google Veo 3.1 on fal.ai: 40 variants, from $0.03/s ([radar](https://sloptv.co/radar/veo-3-1))

### Leaderboard

- Kling 3.0 Turbo: up to #1, 4.89 → 4.84
- FLUX 3: up to #2, 4.83 → 4.84
- Seedance 2.0: #3, 4.87 → 4.84
- Google Gemini Omni: down to #4, 4.91 → 4.82
- MiniMax H3: up to #5, 4.81 → 4.79
- Seedance 2.5: #6, 4.82 → 4.79
- Vivix W1: down to #7, 4.82 → 4.77
- OpenAI Sora 2: #8, 4.78 → 4.76
- Grok Video: #9, 4.74 → 4.72
- Google Veo 3.1: #10, 4.67 → 4.63
- Runway Gen-4.5: #11, 4.63 → 4.57
- PixVerse v5.5: #12, 4.58 → 4.52
- Kling 3.0: #13, 4.49 → 4.47
- MiniMax Hailuo 02: #14, 3.93 → 3.90

### Benchmark clips

- Score corrected: FLUX 3 on [hands-chopping-vegetables](https://sloptv.co/test/hands-chopping-vegetables), 3.83 → 4.00
- Score corrected: FLUX 3 on [hands-counting-fingers](https://sloptv.co/test/hands-counting-fingers), 4.67 → 4.83
- Score corrected: Google Gemini Omni on [hands-chopping-vegetables](https://sloptv.co/test/hands-chopping-vegetables), 4.96 → 3.96
- Score corrected: Google Gemini Omni on [hands-counting-fingers](https://sloptv.co/test/hands-counting-fingers), 4.96 → 2.86
- Score corrected: Google Gemini Omni on [hands-playing-guitar](https://sloptv.co/test/hands-playing-guitar), 4.96 → 4.46
- Score corrected: Grok Video on [hands-chopping-vegetables](https://sloptv.co/test/hands-chopping-vegetables), 2.67 → 2.50
- Score corrected: Grok Video on [hands-counting-fingers](https://sloptv.co/test/hands-counting-fingers), 5.00 → 4.67
- Score corrected: Grok Video on [hands-playing-guitar](https://sloptv.co/test/hands-playing-guitar), 4.50 → 4.17
- Score corrected: MiniMax Hailuo 02 on [hands-chopping-vegetables](https://sloptv.co/test/hands-chopping-vegetables), 3.83 → 3.50
- Score corrected: MiniMax Hailuo 02 on [hands-counting-fingers](https://sloptv.co/test/hands-counting-fingers), 5.00 → 4.17
- And 20 more score corrections

## 2026-10-17

### Prices

13 price changes (13 down, 0 up). Best plan, per second of video; when a change covers several variants, the cheapest one is shown:

| Model | Platform | Variant | Before | Now | Change |
|---|---|---|---:|---:|---:|
| [Seedance 2.0](https://sloptv.co/radar/seedance-2-0) | fal.ai | 2 variants (480p) | $0.173/s | $0.135/s | -22.3% |
| [Seedance 2.0](https://sloptv.co/radar/seedance-2-0) | fal.ai | 2 variants (720p) | $0.37/s | $0.303/s | -18.0% |
| [Seedance 2.5](https://sloptv.co/radar/seedance-2-5) | fal.ai | 6 variants (480p and 720p) | $0.265/s | $0.221/s | -16.7% |
| [Seedance 2.5](https://sloptv.co/radar/seedance-2-5) | fal.ai | 3 variants (1080p) | $1.396/s | $1.164/s | -16.6% |

**New offers:**
- Seedance 2.0 on fal.ai: 4 variants, from $0.682/s ([radar](https://sloptv.co/radar/seedance-2-0))

**No longer listed:**
- Seedance 2.0 on fal.ai: 12 variants
- Seedance 2.5 on fal.ai: 9 variants

## 2026-10-16

### Prices

- **Method change:** each subscription platform is now compared at its lowest price on a **monthly** plan. Until today `is_best_plan` could be a yearly plan; yearly prices stay in the file, marked by the new `billing` column, but are no longer compared. Prices that look higher today on Higgsfield, Runway, Magnific, OpenArt and Lumeta come from this change, not from the platforms.

## 2026-10-15

### Prices

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
- Seedance 2.5 on Lumeta: 5 variants, from $0.0677/s ([radar](https://sloptv.co/radar/seedance-2-5))

## 2026-10-14

### Prices

- **fal.ai is now the cheapest place to run FLUX 3** at 720p and 1080p, after Black Forest Labs API stopped listing it. [Compare](https://sloptv.co/radar/flux-3)
- **Runway is now the cheapest place to run Seedance 2.0** at 1080p ($0.32/s), after Higgsfield raised its price. [Compare](https://sloptv.co/radar/seedance-2-0)

2 price changes (0 down, 2 up). Best plan, per second of video; when a change covers several variants, the cheapest one is shown:

| Model | Platform | Variant | Before | Now | Change |
|---|---|---|---:|---:|---:|
| [Seedance 2.5](https://sloptv.co/radar/seedance-2-5) | Higgsfield | 1080p | $0.36/s | $0.48/s | +33.3% (promo ended) |
| [Seedance 2.0](https://sloptv.co/radar/seedance-2-0) | Higgsfield | 1080p | $0.27/s | $0.36/s | +33.3% (promo ended) |

**New offers:**
- Seedance 2.5 on Higgsfield: 1 variant, from $0.78/s ([radar](https://sloptv.co/radar/seedance-2-5))

**No longer listed:**
- FLUX 3 on Black Forest Labs API: 4 variants

## 2026-10-13

### Prices

**No longer listed:**
- Google Veo 3.1 on fal.ai: 40 variants

### Leaderboard

- Seedance 2.0: up to #3, 4.83 → 4.87
- FLUX 3: down to #4 (4.83)
- Grok Video: #9, 4.67 → 4.74
- Kling 3.0: #13, 4.45 → 4.49

### Benchmark clips

- Score corrected: Grok Video on [hands-counting-fingers](https://sloptv.co/test/hands-counting-fingers), 2.50 → 5.00
- Score corrected: Kling 3.0 on [hands-counting-fingers](https://sloptv.co/test/hands-counting-fingers), 3.17 → 4.83
- Score corrected: Seedance 2.0 on [hands-counting-fingers](https://sloptv.co/test/hands-counting-fingers), 3.17 → 4.67

## 2026-10-12


### Leaderboard

- **New model: Vivix W1** enters at #5 with 4.82/5. [Clips and scores](https://sloptv.co/model/vivix-w1)
- Seedance 2.5: down to #6 (4.82)
- MiniMax H3: down to #7 (4.81)
- OpenAI Sora 2: down to #8 (4.78)
- Grok Video: down to #9 (4.67)
- Google Veo 3.1: down to #10 (4.67)
- Runway Gen-4.5: down to #11 (4.63)
- PixVerse v5.5: down to #12 (4.58)
- Kling 3.0: down to #13 (4.45)
- MiniMax Hailuo 02: down to #14 (3.93)

### Benchmark clips

- 40 new scored clips for Vivix W1 (round v1-vivix-2026-10)

## 2026-10-10

### Prices

- **Kie.ai is now the cheapest place to run Google Gemini Omni** at 720p ($0.063/s), ahead of OpenArt ($0.0826/s). [Compare](https://sloptv.co/radar/gemini-omni)
- **Kie.ai is now the cheapest place to run Google Gemini Omni** at 1080p ($0.063/s), ahead of Higgsfield ($0.09/s). [Compare](https://sloptv.co/radar/gemini-omni)
- **Kie.ai is now the cheapest place to run Grok Video** at 480p ($0.012/s), ahead of fal.ai ($0.05/s). [Compare](https://sloptv.co/radar/grok-video)
- **Kie.ai is now the cheapest place to run Grok Video** at 720p ($0.0225/s), ahead of OpenArt ($0.066/s). [Compare](https://sloptv.co/radar/grok-video)
- **Kie.ai is now the cheapest place to run Grok Video** at v1.5 480p ($0.012/s), ahead of Higgsfield ($0.075/s). [Compare](https://sloptv.co/radar/grok-video)
- **Kie.ai is now the cheapest place to run Grok Video** at v1.5 720p ($0.0225/s), ahead of Runway ($0.128/s). [Compare](https://sloptv.co/radar/grok-video)
- **Kie.ai is now the cheapest place to run MiniMax Hailuo 02** at 512p ($0.01/s), ahead of Replicate ($0.015/s). [Compare](https://sloptv.co/radar/hailuo-02)
- **Kie.ai is now the cheapest place to run MiniMax Hailuo 02** at 768p ($0.025/s), ahead of Higgsfield ($0.03/s). [Compare](https://sloptv.co/radar/hailuo-02)
- **Kie.ai is now the cheapest place to run MiniMax H3** at 768p ($0.04/s), ahead of fal.ai ($0.06/s). [Compare](https://sloptv.co/radar/hailuo-h3)
- **Kie.ai is now the cheapest place to run Kling 3.0** at 720p ($0.07/s), ahead of Kling API ($0.084/s). [Compare](https://sloptv.co/radar/kling-3-0)
- **Kie.ai is now the cheapest place to run Kling 3.0 Turbo** at pro 1080p ($0.113/s), ahead of Kling API ($0.14/s). [Compare](https://sloptv.co/radar/kling-3-0-turbo)
- **Kie.ai is now the cheapest place to run Google Veo 3.1** at fast 4k, fast 720p, fast 1080p, lite 720p, lite 1080p, 720p and 1080p, ahead of fal.ai. [Compare](https://sloptv.co/radar/veo-3-1)
- **Kie.ai is now the cheapest place to run Google Veo 3.1** at 4k ($0.231/s), ahead of Magnific ($0.343/s). [Compare](https://sloptv.co/radar/veo-3-1)

**New offers:**
- Google Gemini Omni on Kie.ai: 4 variants, from $0.063/s ([radar](https://sloptv.co/radar/gemini-omni))
- Grok Video on Kie.ai: 8 variants, from $0.012/s ([radar](https://sloptv.co/radar/grok-video))
- MiniMax Hailuo 02 on Kie.ai: 5 variants, from $0.01/s ([radar](https://sloptv.co/radar/hailuo-02))
- MiniMax H3 on Kie.ai: 6 variants, from $0.04/s ([radar](https://sloptv.co/radar/hailuo-h3))
- Kling 3.0 on Kie.ai: 6 variants, from $0.07/s ([radar](https://sloptv.co/radar/kling-3-0))
- Kling 3.0 Turbo on Kie.ai: 4 variants, from $0.09/s ([radar](https://sloptv.co/radar/kling-3-0-turbo))
- Seedance 2.0 on Kie.ai: 8 variants, from $0.019/s ([radar](https://sloptv.co/radar/seedance-2-0))
- Seedance 2.5 on Kie.ai: 3 variants, from $0.14/s ([radar](https://sloptv.co/radar/seedance-2-5))
- Google Veo 3.1 on Kie.ai: 24 variants, from $0.0188/s ([radar](https://sloptv.co/radar/veo-3-1))

## 2026-10-06

### Dataset

- First public release of this dataset on GitHub: 13 models, 518 scored clips and 10,111 prices from 15 platforms and APIs.

## 2026-10-04

### Leaderboard

- **New model: FLUX 3** enters at #3 with 4.83/5, level with Seedance 2.0, after 40 scored clips. It has perfect scores on on-screen text, lip-sync and multi-shot tests. [Clips and scores](https://sloptv.co/model/flux-3)

### Prices

**New offers:**
- FLUX 3 on Black Forest Labs API, the model's official API, and on fal.ai ([radar](https://sloptv.co/radar/flux-3))

## 2026-10-03

### Prices

**New sources:** the radar now also reads the model makers' own APIs, so resellers can be compared with the official price.
- Google Gemini API, Kling API, MiniMax API, Luma API, xAI API and BytePlus ModelArk (ByteDance)
- Magnific and OpenArt

## 2026-10-02

### Prices

19 price changes (13 down, 6 up). Best plan, per second of video; when a change covers several variants, the cheapest one is shown:

| Model | Platform | Variant | Before | Now | Change |
|---|---|---|---:|---:|---:|
| [MiniMax H3](https://sloptv.co/radar/hailuo-h3) | Higgsfield API | 3 variants (2k) | $0.091/s | $0.065/s | -28.6% |
| [MiniMax H3](https://sloptv.co/radar/hailuo-h3) | fal.ai | 6 variants of H3 Max (480p, 768p and 1080p) | $0.025/s | $0.03/s | +20.0% |
| [Kling 3.0](https://sloptv.co/radar/kling-3-0) | Higgsfield API | 9 variants | $0.0462/s | $0.042/s | -9.1% |
| [Kling 3.0 Turbo](https://sloptv.co/radar/kling-3-0-turbo) | Higgsfield API | 4 variants (720p and 1080p) | $0.0616/s | $0.056/s | -9.1% |

Higgsfield's API listed these models without their discounts for one day on 1 October, then settled at the lower prices above.

**No longer listed:**
- Luma Ray 2 and Ray 2 Flash on fal.ai: 4 variants (fal marks both as deprecated)
