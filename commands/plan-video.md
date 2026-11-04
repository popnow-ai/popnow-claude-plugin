---
description: Plan an AI video from an idea or script - shot list, prompts, keyframes and a cost estimate
argument-hint: "[idea, script or brief]"
---

Plan an AI video for this brief: $ARGUMENTS

Work through these steps in order, using the plugin's skills:

1. Use the `shot-list` skill to confirm the brief (ask only for what is missing) and produce the timed shot list and continuity sheet.
2. Use the `keyframe-prompts` skill for every shot that should start from an image.
3. Use the `video-prompts` skill to write one prompt per shot, with the recommended model and settings.
4. Use the `generation-budget` skill to estimate the total cost with retries, and show the cheaper drafting option.

Finish with a short summary: number of shots, total length, recommended models and the estimated budget range. Do not generate any media; this plan is text only.
