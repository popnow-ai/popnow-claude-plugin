---
name: generation-budget
description: Estimate what an AI video or image project will cost before generating anything, from a shot list or a rough count of clips and images, including retries, using the prices the user provides. Use when someone asks how much an AI video will cost, wants a budget for a campaign, or wants to compare the cost of a plan at different models or rates.
---

# Generation budget

Turn a plan into a number. Price every clip and image, add a realistic allowance for retries, and show what a cheaper drafting pass would save.

## Inputs

Take them from a shot list if there is one; otherwise ask for:

- Video clips: model, resolution, length in seconds, audio on or off, and how many.
- Images: model, resolution, and how many.
- How many takes per shot to expect. Default: 2 for video (first try plus one retry) and 3 for images.
- The current price of each model and setting, from the pricing page of the service the user plans to use.

## Prices

This skill ships no price list, because prices change often. Do not recall or invent a price. If a price is missing, ask for it, or leave that line unpriced and say so.

If a video price is quoted for a fixed clip length, scale it by seconds only when the service bills per second, and say that you did.

## Calculation

For each line: price per second × seconds × shots × takes for video, and price per image × images × takes for images.

Show:

1. A line-by-line table and the total.
2. The same total at each other rate the user gave, marking any option that lacks a model in the plan.
3. A drafting tip when the user has a price for a cheaper draft tier: how much the plan saves if drafts run on that tier and only approved shots run at final quality.

## Example

Plan: 6 shots at 5 seconds each with 2 takes, and 4 keyframes with 3 takes. Illustrative prices: $0.10 per second of video and $0.05 per image.

- Video: 6 × 2 = 12 clips × 5 seconds × $0.10 = $6.00.
- Images: 4 × 3 = 12 images × $0.05 = $0.60.
- Total: $6.60.

Remind the user that promotions, subscriptions and enterprise rates can change the total.
