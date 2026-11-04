---
name: prompt-doctor
description: Diagnose why an AI image or video generation came out wrong - warped hands and faces, identity drift between shots, flicker, garbled text, ignored camera moves, wrong aspect, too much or too little motion - and rewrite the prompt and settings to fix it. Use when someone says a generation looks bad, the model ignored the prompt, characters do not match, or they want to stop wasting retries.
---

# Prompt doctor

Every retry costs money. Before regenerating, find the cause and change one thing at a time.

## Ask for

The prompt, the model and settings (length, resolution, aspect, audio, image-to-video or text-to-video), and a description of what went wrong. You cannot see the output unless the user shares an image, so ask them to describe it precisely.

## Common problems and fixes

| Symptom | Likely cause | Fix |
|---|---|---|
| Warped hands, melting objects | Too much action or a long clip | Simplify to one action, shorten to 4 to 6 s, slow the camera |
| Face or outfit changes between shots | Different wording per shot | Paste one fixed character description word for word; start from the same keyframe or reference images |
| Subject drifts or morphs late in the clip | Clip too long for the motion | Split into two shots or use extension from the last good frame |
| Camera move ignored | Move buried late or conflicting | Put shot and camera first; use one move; remove contradicting words like "static" |
| Garbled on-screen text | Video models handle text poorly | Remove text from the prompt and add it in the edit; for stills use a text-strong image model |
| Flicker or jitter | Busy textures, fast motion, low resolution | Calmer motion, simpler background, higher resolution for the final |
| Too little motion in image-to-video | Prompt re-describes the image | Describe only motion and camera; add a clear action verb |
| Ignored style | Style words at the end, mixed styles | One style, stated early, consistent suffix (see `style-bible`) |
| Wrong framing or crop | Aspect ratio not set | Set the ratio in settings, not only in the prompt |
| Unwanted logos or text | Model filled empty signage | Add "plain, unbranded" to props and surfaces |

## Output

1. The most likely cause, in one or two sentences.
2. A rewritten prompt.
3. Settings to change (model, length, resolution, mode).
4. What to try next if it still fails, and whether a cheaper draft tier can be used to test the fix first.
