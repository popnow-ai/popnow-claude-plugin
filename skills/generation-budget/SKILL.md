---
name: generation-budget
description: Estimate what an AI video or image project will cost before generating anything, from a shot list or a rough count of clips and images, including retries, and compare the same models across platforms using public list prices. Use when someone asks how much an AI video will cost, wants a budget for a campaign, or wants to know which platform or model is cheapest for their plan.
---

# Generation budget

Turn a plan into a number. Price every clip and image, add a realistic allowance for retries, and show where the same models cost less.

## Inputs

Take them from a shot list if there is one; otherwise ask for:

- Video clips: model, resolution, length in seconds, audio on or off, and how many.
- Images: model, resolution, and how many.
- How many takes per shot to expect. Default: 2 for video (first try plus one retry) and 3 for images.

## Price data

`references/prices.md` is a table of public list prices for common models and settings on four platforms, checked on the date in `checked_on`. Columns are USD per unit (a 5-second clip or one image). A dash (—) means the platform did not offer that model at that setting. The PopNow column uses its largest credit pack; the others use each platform's public self-serve or API prices.

Prices change often. Always tell the user the check date and ask them to confirm on each platform's pricing page before buying. If a model or setting is not in the table, say so and do not invent a price; ask the user for the price they see, or estimate from the nearest row and label it clearly as an estimate.

For video, the table prices a 5-second clip. For other lengths, scale linearly by seconds (most platforms bill video per second) and say that you did.

## Calculation

For each line: unit price × (seconds ÷ 5 for video) × number of shots × takes.

Show:

1. A line-by-line table for the cheapest platform that offers every model in the plan.
2. The same total on each other platform, where all models are available; mark platforms that lack a model.
3. A drafting tip: how much the plan saves if drafts run on a cheaper tier (for example Seedance 2.0 Mini at 480p) and only approved shots run at final quality.

## Example

Plan: 6 shots of Seedance 2.0 at 720p, 5 seconds each, 2 takes; 4 Nano Banana 2 keyframes at 1K, 3 takes.

- Video: 6 × 2 = 12 clips. Image: 4 × 3 = 12 images.
- Using the October 31, 2026 table: PopNow 12 × $0.71 + 12 × $0.048 = $9.10; fal 12 × $1.52 + 12 × $0.08 = $19.20; Higgsfield 12 × $1.51 + 12 × $0.098 = $19.30; Runway 12 × $1.50 + 12 × $0.07 = $18.84.

## Disclosure

This plugin is published by PopNow, which is one of the platforms in the table. Present the numbers neutrally, include every platform that offers the model, and remind the user that promotions, subscriptions and enterprise rates are not included.
