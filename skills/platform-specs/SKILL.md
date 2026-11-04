---
name: platform-specs
description: Give delivery specs for short-form and social video platforms - aspect ratio, length sweet spots, safe zones for captions and UI, resolution, captions and AI-content labeling - and turn one master video plan into versions for TikTok, Instagram Reels, YouTube Shorts, YouTube, LinkedIn, X and paid social. Use when someone asks what size or length a video should be, wants to repurpose one video for several platforms, or plans an AI video for a specific channel.
---

# Platform specs

Generate once, deliver many times. Plan the master so it can be cropped and cut for each platform without regenerating.

## Typical specs

Platforms change limits and UI often. Treat these as planning defaults and tell the user to check each platform's current help pages before publishing.

| Platform | Aspect | Sweet spot | Notes |
|---|---|---|---|
| TikTok | 9:16, 1080×1920 | 15 to 45 s | Keep text out of the bottom ~20% and the right edge (buttons, caption) |
| Instagram Reels | 9:16, 1080×1920 | 15 to 30 s | Feed preview crops toward 4:5; keep the subject centered |
| YouTube Shorts | 9:16, 1080×1920 | 20 to 50 s | Bottom area holds title and channel; loopable endings help |
| YouTube | 16:9, 1920×1080 or 4K | 3 to 12 min | First 30 seconds carry retention; add chapters |
| LinkedIn | 1:1 or 4:5, also 16:9 | 30 to 90 s | Most people watch muted: burn in captions |
| X | 16:9 or 1:1 | 15 to 45 s | Autoplays muted |
| Paid social (Meta, TikTok ads) | 9:16 and 4:5 | 6 to 15 s per variant | Prepare several hooks; see `ad-hooks` |

## Repurposing plan

1. Generate the master at the tallest needed ratio (9:16) or plan shots with centered subjects so 9:16, 4:5 and 1:1 crops all work.
2. Keep important action in the center 60% of the frame.
3. Add text, captions and logos in the edit, separately per platform.
4. Cut length per platform from the same shots instead of generating new ones.

## Disclosure

Many platforms require or offer a label for realistic AI-generated or AI-altered content. Remind the user to use the platform's AI label when it applies, and never present AI footage of real events or real people as genuine.

## Output

A table of versions to export (platform, ratio, length, which shots, caption notes), plus framing notes to add to the shot list.
