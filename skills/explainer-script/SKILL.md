---
name: explainer-script
description: Write a narrated explainer or faceless video, from topic to timed voice-over script and a scene-by-scene visual plan in a chosen style (editorial mixed media, stickman cartoon, kinetic typography, whiteboard, 3D product, documentary B-roll). Use when someone wants an explainer, a faceless YouTube or TikTok video, a product walkthrough, a history or science short, or a video essay.
---

# Explainer script

A good explainer answers one question clearly. The voice-over carries the information; the visuals make it easy to follow and remember.

## Inputs

- The one question the video answers, and who is watching (beginner or expert).
- Length (default 60 seconds for Shorts/TikTok, 3 to 6 minutes for YouTube).
- Visual style (see below) and aspect ratio.
- Facts, sources or product details the user wants included.

## Script rules

- Structure: hook question (first 5 seconds), why it matters, 3 to 5 steps or ideas, a recap, a call to action.
- Timing: about 150 spoken words per minute in English (2.5 per second). Show the word count and estimated duration per section.
- Use concrete examples and numbers. If a fact needs a source, mark it "[source]" and ask the user to confirm; do not invent statistics or quotes.
- Write for the ear: short sentences, no parentheses, spell out symbols.

## Visual styles

| Style | Looks like | Works for |
|---|---|---|
| Editorial mixed media | Paper cut-outs, archival photos, bold type, collage | History, news, culture |
| Stickman cartoon | Simple line characters on plain backgrounds | Concepts, processes, humor |
| Kinetic typography | Animated words synced to the voice | Quotes, lists, punchy facts |
| Whiteboard | Hand-drawn diagrams appearing step by step | Teaching, how it works |
| 3D product | Clean renders, rotating objects, exploded views | Product features, tech |
| Documentary B-roll | Realistic establishing shots and details | Travel, nature, lifestyle |

Pick one and keep it for the whole video. Some styles, such as kinetic typography and whiteboard, are often easier in a motion-graphics or HTML-to-video tool than with an AI video model; say so when it applies.

## Output

1. The script in sections with word counts and timings.
2. A scene table: time | voice-over line | visual | on-screen text | asset type (AI video, AI image with motion, motion graphic, stock, screen recording).
3. A style note to paste into every visual prompt (or use `style-bible`).
4. Hand-offs: `video-prompts` and `keyframe-prompts` for the AI shots, `voiceover-music-brief` for the narration and music, `generation-budget` for the cost.
