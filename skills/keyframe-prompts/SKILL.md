---
name: keyframe-prompts
description: Write prompts for the still images that start or anchor AI video shots (keyframes, character sheets, product hero frames), choosing between Nano Banana, GPT Image, Seedream and FLUX for each frame. Use when a shot list marks shots that start from an image, when a character or product must look the same across shots, or when someone wants image prompts for a storyboard.
---

# Keyframe prompts

A keyframe is the still image a video shot starts from. It is the cheapest way to lock a look: an image costs a few cents, a video clip costs much more, so iterate on the still until it is right, then animate it.

## When to make keyframes

- A recurring character: make one character sheet first (front, three-quarter, profile on a plain background), then one keyframe per shot.
- A real product: start from a photo of the real product and edit it into the scene (image-to-image), rather than asking a model to invent the product.
- A specific composition: a poster-like opening frame, a final logo shot, a branded set.

## Pick the model per frame

See `references/models.md`. In short:

- Exact text inside the image (signs, packaging, posters, non-English text): GPT Image first, then Seedream.
- Photoreal people and products: Nano Banana or FLUX.
- Consistency from several reference images: Seedream (up to ten references) or Nano Banana edits.
- Layout-heavy frames (diagrams, infographics, title cards): Nano Banana Pro.

## Prompt structure

1. **Framing**: shot size and angle, matching the video shot. "Low-angle medium shot."
2. **Subject**: the continuity description, word for word.
3. **Pose and expression**: frozen at the first moment of the shot's action.
4. **Setting and light**.
5. **Style and medium**.
6. **Aspect ratio and resolution**: the same aspect ratio as the video. 1K or 2K is enough for a video start frame.

Leave room for motion: if the character will walk to the right, frame them with space on the right.

## Output format

```
K2 · for shot 3 · 9:16 · 2K
Model: <model> (alternative: <model>)
Mode: text-to-image | edit from <reference>
Prompt: <the prompt>
```

## Rights

Only use photos the user owns or has permission to use, especially photos of people. Do not create images of real public figures or recognizable private people without consent.
