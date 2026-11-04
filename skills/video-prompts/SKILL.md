---
name: video-prompts
description: Write production-ready prompts for AI video models such as Seedance, Kling, MiniMax Hailuo and Wan, one prompt per shot, with the right length, aspect ratio, resolution and audio settings for each model. Use when someone needs text-to-video or image-to-video prompts, wants to rewrite a weak prompt, or has a shot list to turn into prompts.
---

# Video prompts

Write one prompt per shot. The goal is a clip that is usable on the first or second try, because every attempt is paid.

## Choose the model and settings first

Read `references/models.md` for each model's clip lengths, resolutions, aspect ratios and audio support. Pick the cheapest model and the lowest resolution that fit the shot, and say why:

- Drafts and iteration: a fast or mini tier at 480p or 720p.
- Final shots: the full model at 720p or 1080p. Use 4K or 2K only when the delivery really needs it.
- Long single takes (over 15 seconds): only models that support them, and only for slow, simple action.
- Shots with spoken lines or synced sound effects: a model with native audio, with audio turned on.

If the user has not chosen a model, recommend one per shot and offer a cheaper alternative.

## Prompt structure

Write in plain, concrete sentences, in this order:

1. **Shot and camera**: shot size, lens feel and movement. "Medium close-up, 50mm, slow dolly in."
2. **Subject**: paste the fixed description from the continuity sheet word for word.
3. **Action**: one main action with a clear start and end. "She lifts the cup, pauses, and smiles at the camera."
4. **Setting and light**: place, time of day, weather, light quality and direction.
5. **Style**: "photoreal, shot on 35mm film, soft grain" or "3D animated, soft clay look".
6. **Sound** (models with audio): ambience, effects, and any dialogue in quotes with who says it. Keep spoken lines short, about 2 to 3 seconds of speech per 5 seconds of video.

Keep it to roughly 40 to 120 words. More words rarely help; contradictory words always hurt.

## Image-to-video

When the shot starts from a keyframe, the image already fixes the look. Describe only motion, camera and sound. Do not re-describe the subject's appearance, which can fight the image.

## Multi-shot prompts

Some models can cut between shots inside one clip. Use it only when the shots share a location and characters, and label them: "Shot 1 (0-3s): ... Shot 2 (3-6s): ...". Otherwise generate shots separately and cut them in the edit.

## Avoid

- Several actions in one shot ("she runs, jumps, turns and waves").
- Exact on-screen text, logos and long captions. Add them in the edit.
- Named real people, celebrities and copyrighted characters.
- Vague quality words on their own ("amazing, 8k, masterpiece"). Describe what you want to see.

## Output format

For each shot:

```
Shot 3 · 5s · 9:16 · 720p · audio on
Model: <recommended model> (cheaper option: <model>)
Mode: text-to-video | image-to-video from K2
Prompt: <the prompt>
Negative / avoid (only if the model supports it): <short list>
```

End with the total number of clips and seconds per model so the `generation-budget` skill can price the plan.
