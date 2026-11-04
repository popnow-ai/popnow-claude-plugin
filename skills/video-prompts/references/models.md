# Video model reference

Limits as offered by common hosting platforms in late October 2026. Providers change limits often, so check the platform you use before generating. "Audio" means the model can generate synchronized sound with the clip.

| Model | Clip length | Resolutions | Aspect ratios | Audio | Good for |
|---|---|---|---|---|---|
| Seedance 2.5 (ByteDance) | 4 to 30 s | 480p, 720p, 1080p | 21:9, 16:9, 4:3, 1:1, 3:4, 9:16 | Yes | Long takes, strong camera language, multi-shot storytelling, reference-driven consistency |
| Seedance 2.0 | 4 to 15 s | 480p to 4K | 21:9, 16:9, 4:3, 1:1, 3:4, 9:16 | Yes | Cinematic shots, 4K delivery |
| Seedance 2.0 Fast | 4 to 15 s | 480p, 720p | same as 2.0 | Yes | Cheaper finals at 720p, fast iteration |
| Seedance 2.0 Mini | 4 to 15 s | 480p, 720p | same as 2.0 | Yes | Cheapest drafts and previews |
| Kling 3.0 (Kuaishou) | 3 to 15 s | 720p, 1080p, 4K | 16:9, 9:16, 1:1 | Yes | Realistic motion, multi-shot cuts, character animation |
| Kling 4.0 | 3 to 30 s | 720p, 1080p | 16:9, 9:16, 1:1, 21:9 | Check platform | Keyframes, extensions and edits; can queue when busy |
| MiniMax H3 (Hailuo) | 5 to 30 s | 480p, 768p, 2K | 16:9, 9:16, 1:1, 4:3, 3:4, 21:9 | Yes | Expressive characters and faces, fast turnaround, good value at 768p |
| Wan 3.0 (Alibaba) | 2 to 30 s | 480p, 720p, 1080p | 16:9, 9:16, 1:1, 4:3, 3:4 | Yes | Long clips with synced audio |
| Wan 2.6 | 5, 10 or 15 s | 720p, 1080p | 16:9, 9:16, 1:1, 4:3, 3:4 | Yes | Multi-shot sequences |

Most of these also offer image-to-video (start from a still), reference-to-video (keep a character or product consistent from reference images) and extension (continue an existing clip).

## Practical notes

- Video is usually billed per second and per resolution, and audio can add to the price. Draft at low resolution, then render only the approved shots at final quality.
- Typical render times range from under a minute (MiniMax H3) to several minutes (Seedance 2.5 at 1080p). Plan time for retries.
- For a recurring character across many shots, generate one keyframe or reference image first and use image-to-video or reference-to-video for every shot.
