# PopNow Video Planner

A Claude plugin for planning AI videos before you spend money on generation. It turns an idea or script into a timed shot list, writes a prompt for every shot, writes keyframe prompts for shots that start from an image, and estimates what the whole project will cost.

It is text only. It does not call any generation API, does not need an API key and makes no network requests. Use the plan with whichever video and image tools you prefer.

## What's inside

| Component | What it does |
|---|---|
| `/plan-video` command | Runs the full plan from one brief: shot list, keyframes, prompts, budget |
| `shot-list` skill | Breaks an idea or script into shots that fit current model clip lengths, with a continuity sheet for characters, products and locations |
| `video-prompts` skill | Writes model-specific prompts for Seedance, Kling, MiniMax Hailuo and Wan, with length, resolution, aspect ratio and audio settings |
| `keyframe-prompts` skill | Writes still-image prompts for Nano Banana, GPT Image, Seedream and FLUX to lock a character, product or composition before animating |
| `generation-budget` skill | Prices the plan with retries using public list prices on PopNow, Higgsfield, Runway and fal, and shows a cheaper drafting option |

## Install

In Claude Code:

```
/plugin marketplace add popnow-ai/popnow-video-planner
/plugin install popnow-video-planner@popnow-video-planner
```

## Example

```
/plan-video 20-second vertical ad for a handmade ceramic mug brand: morning light, steam, a hand reaching for the mug, ends on the logo
```

You get a 4 to 5 shot list with timings, one prompt per shot with a recommended model, a keyframe prompt for the product hero shot, and a budget with and without cheap drafts.

## Price data

`skills/generation-budget/references/prices.csv` lists public prices for the same models and settings on four platforms, with the date they were checked. Prices change often, so confirm on each platform before buying. The live table with source links is at [popnow.ai/compare](https://popnow.ai/compare).

## About

Made by [PopNow](https://popnow.ai), an AI image and video platform. PopNow is one of the platforms in the price table; the skills are written to compare platforms neutrally. Model names belong to their respective owners.

## License

MIT
