# PopNow for Claude

AI video pre-production and PopNow API integration, as one Claude plugin.

Built by PopNow AI ([popnow.ai](https://popnow.ai)), the world's first AI studio with automatic price protection.

- **Creators and marketers** plan videos before spending credits: shot lists, model-specific prompts, keyframes, ad hooks, UGC scripts, explainers, style bibles, platform versions, voice-over briefs, prompt fixes and cost estimates.
- **Developers** add image, video and audio generation to their own apps with the PopNow SDKs, with keys kept on the server, idempotent retries and webhooks.

The planning skills are text only: they make no network requests, need no API key and never run a paid generation. Use the plans with whichever tools you prefer.

## Commands

| Command | What you get |
|---|---|
| `/plan-video` | Full plan from one brief: shot list, keyframes, prompts, budget and a review pass |
| `/ad-hooks` | 6 to 8 opening hooks and angles to A/B test, with shot prompts |
| `/ugc-script` | A creator-style product video script with shot list, alt hooks and caption |
| `/explainer` | A narrated or faceless explainer: timed script, scene table, style note |
| `/remix-reference` | A reference video's structure broken down and rebuilt as original work |
| `/style-bible` | A visual style guide with hex palette and a reusable prompt suffix |
| `/fix-prompt` | Why a generation went wrong, and a rewritten prompt and settings |
| `/video-budget` | Cost with retries across PopNow, Higgsfield, Runway and fal |
| `/repurpose` | One master plan turned into TikTok, Reels, Shorts, YouTube, LinkedIn and X versions |
| `/integrate-popnow` | PopNow generation added to your codebase with the official SDK |

## Skills

| Skill | Use it for |
|---|---|
| `shot-list` | Breaking an idea or script into shots that fit model clip limits, with a continuity sheet |
| `video-prompts` | Prompts for Seedance 2.5 and 2.0, Kling 3.0 and 4.0, MiniMax Hailuo H3 and Wan, with length, resolution, ratio and audio |
| `keyframe-prompts` | Still frames with Nano Banana, GPT Image, Seedream and FLUX to lock a look before animating |
| `generation-budget` | Pricing a plan from public list prices, with a cheaper drafting path |
| `ad-hooks` | Hook variants and ad angles for paid social |
| `ugc-ad-script` | UGC and product review scripts |
| `reference-remix` | Learning from a format without copying it |
| `explainer-script` | Explainers and faceless videos in six visual styles |
| `style-bible` | Consistent looks across many generations |
| `platform-specs` | Ratios, lengths, safe zones and AI-content labels per platform |
| `voiceover-music-brief` | Timed narration, music and sound-effect briefs |
| `prompt-doctor` | Fixing warped hands, identity drift, flicker, garbled text and ignored camera moves |
| `popnow-api` | Integrating the PopNow API: models, quotes, tasks, waiting, downloads, errors |
| `popnow-webhooks` | Verifying and handling PopNow task callbacks |

The `storyboard-reviewer` agent checks a plan for model limits, continuity, rights and wasted spend before you generate.

## Install

In Claude Code:

```
/plugin marketplace add popnow-ai/popnow-claude-plugin
/plugin install popnow@popnow
```

## Examples

```
/plan-video 20-second vertical ad for a handmade ceramic mug brand: morning light, steam, a hand reaching for the mug, ends on the logo
/ad-hooks a $29 posture corrector for remote workers, proof: 4.6-star average from 2,000 reviews
/explainer why the sky is blue, 60 seconds, stickman style
/fix-prompt Kling 3.0, 10 s, 1080p: "a woman dances, spins, jumps and waves in a busy market" - her hands warp after 5 seconds
/integrate-popnow let users turn an uploaded product photo into a 5-second 9:16 video in our Next.js app
```

## Price data

`skills/generation-budget/references/prices.csv` lists public prices for the same models and settings on four platforms, with the date they were checked. Prices change often; confirm on each platform before buying. Live table with sources: [popnow.ai/compare](https://popnow.ai/compare).

## About

Made by [PopNow](https://popnow.ai), an AI image, video and audio platform with one API for many models. PopNow is one of the platforms in the price table; the planning skills compare platforms neutrally. Model names belong to their respective owners.

- API docs: https://popnow.ai/docs
- Support: support@popnow.ai

## License

MIT
