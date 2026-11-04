---
name: shot-list
description: Turn a video idea, script or product brief into a timed shot list for AI video generation, with clip lengths that fit current model limits, camera and sound notes, and a continuity sheet for recurring characters and props. Use when someone wants to plan, storyboard or break down an AI video, ad, short film, explainer or social clip before generating it.
---

# Shot list for AI video

AI video models generate one clip at a time, usually 4 to 15 seconds, sometimes up to 30. A finished video is a sequence of clips, so the plan has to be cut into shots that each fit one generation. A good shot list saves money: most wasted credits come from vague prompts and shots that are too long or too busy for one clip.

## 1. Pin down the brief

Ask only for what is missing. Use sensible defaults and say what you assumed.

- **Goal and audience**: what the viewer should feel or do at the end.
- **Total length**: default 15 to 30 seconds for social, 45 to 90 seconds for an explainer or short film.
- **Aspect ratio**: 9:16 for TikTok, Reels and Shorts; 16:9 for YouTube and websites; 1:1 or 4:5 for feeds.
- **Style**: live-action photoreal, animation, 3D, anime, stop-motion, documentary and so on.
- **Sound**: native model audio (ambience, effects, short lines of dialogue), a separate voice-over, music only, or silent.
- **Fixed elements**: a real product, a logo, a recurring character, a location.

## 2. Cut it into shots

Rules of thumb:

- One shot is one action, one camera move, one location. If a sentence needs "then", it is probably two shots.
- Keep most shots 4 to 8 seconds. Use 10 to 15 seconds only for slow, simple moments (a reveal, a drift through a landscape). Long, busy shots drift and deform.
- Open with the strongest image. On social, the first 2 seconds decide whether anyone stays.
- Alternate shot sizes (wide, medium, close-up) so cuts feel intentional.
- Put text overlays, logos and exact captions in the edit, not in the generated clip, unless the user specifically wants in-video text.
- Mark which shots should start from a still image (image-to-video). Use a keyframe when the look must be exact: a product, a face that must match across shots, a branded set.

## 3. Output format

Return a table, then a continuity sheet.

| # | Time | Length | Shot size and camera | Action | Sound | Start from |
|---|---|---|---|---|---|---|
| 1 | 0:00 | 5s | Wide, slow push-in | ... | Rain, distant traffic | Text |
| 2 | 0:05 | 4s | Close-up, static | ... | Line: "..." | Keyframe K1 |

**Continuity sheet**: for every recurring character, product and location, write one fixed description that will be pasted word for word into every prompt that uses it, for example: "Mara, a woman in her 30s with a short black bob, round silver glasses and a mustard raincoat". Note props that must stay on the same side (a bag on the left shoulder) and lighting that must stay consistent (golden hour, rain at night).

**Totals**: number of clips, total seconds, number of keyframes. These feed the `generation-budget` skill.

## 4. Hand-offs

- To write the prompts for each shot, use the `video-prompts` skill.
- For shots marked "Keyframe", use the `keyframe-prompts` skill.
- To estimate the cost before generating anything, use the `generation-budget` skill.

## Rights and safety

Plan only with characters, brands and likenesses the user has the right to use. Do not plan videos that imitate a real person without consent, depict minors in unsafe situations or are designed to mislead viewers about real events.
