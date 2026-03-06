# Viral Writer — OpenClaw Skill

Write viral, human-sounding long-form content for social platforms.

**Platforms supported:** X/Twitter threads, 公众号, LinkedIn, 小红书, Discord, Newsletter

**Languages:** Chinese & English

## What It Does

This is an [OpenClaw](https://github.com/openclaw/openclaw) skill that transforms any topic into high-engagement social content through a craft-driven pipeline:

```
DISCOVER → BRIEF → FRAMEWORK → HOOK → DRAFT(+Craft) → FORMAT → REVIEW ⇄ DELIVER
```

The critical differentiator: **Craft is the engine, not de-AI.** Good writing doesn't need an "AI removal" pass — it's naturally human because every sentence is an intentional choice driven by 6 craft principles: density, specific→universal jump, cognitive gap, rhythm, golden line engineering, and breadth.

## Key Features

- **Smart Discovery** — Multi-source hot topic scanning, trend staging, angle gap analysis, fit scoring
- **Voice System** — 5-dimension persona profiling for consistent, recognizable writing
- **6 Craft Principles** — The core engine: Density, Jump, Cognitive Gap, Rhythm, Golden Line, Breadth
- **5 Proven Frameworks** — Narrative, Contrast, Listicle, Counter-Intuitive, Personal Journey
- **Hook A/B Testing** — Generate 5 candidates, score on 4 dimensions, ship the best
- **Depth Lenses** — Philosophy, psychology, sociology, communication, viral science, and more
- **Scored Review Loop** — 8-dimension quality scoring (80-point scale) with auto-iteration
- **Platform Formatting** — Specific rules for X, 公众号, LinkedIn, 小红书, Discord, and newsletters
- **De-AI Safety Net** — Dated pattern reference for edge case cleanup (not a core step)

## Installation

### For OpenClaw users

Copy the skill into your OpenClaw skills directory:

```bash
git clone https://github.com/xiaofangkuai666-cyber/viral-writer-skill.git
cp -r viral-writer-skill ~/.openclaw/skills/viral-writer
```

### For everyone else

The reference files in `references/` are standalone and useful even without OpenClaw:

- [`references/craft.md`](references/craft.md) — **The 6 principles of great writing** (start here)
- [`references/discovery.md`](references/discovery.md) — Hot topic discovery methodology
- [`references/voice.md`](references/voice.md) — Voice & persona system
- [`references/frameworks.md`](references/frameworks.md) — 5 content frameworks with templates
- [`references/hooks.md`](references/hooks.md) — Hook formulas, A/B testing, and quality tests
- [`references/depth-lenses.md`](references/depth-lenses.md) — Add intellectual depth
- [`references/platforms.md`](references/platforms.md) — Platform-specific formatting rules
- [`references/de-ai-checklist.md`](references/de-ai-checklist.md) — Safety net: dated AI pattern reference

## File Structure

```
viral-writer/
├── SKILL.md                  # Main skill definition (OpenClaw entry point)
├── README.md                 # This file
└── references/
    ├── craft.md              # The 6 principles of great writing (core)
    ├── discovery.md          # Hot topic discovery methodology
    ├── voice.md              # Voice & persona system
    ├── frameworks.md         # 5 writing frameworks
    ├── hooks.md              # Hook design formulas + A/B testing
    ├── depth-lenses.md       # Intellectual depth lenses
    ├── platforms.md          # Platform formatting guide
    └── de-ai-checklist.md    # Safety net: AI pattern reference (dated)
```

## Craft: The Real Engine

Most AI writing tools focus on "removing AI smell." We focus on **writing well.** If your writing has genuine craft, it's naturally human.

The 6 principles:

1. **Density > Length** — Every sentence earns its place. If you can delete it without loss, delete it.
2. **Specific → Universal** — One foot in the mud, one foot in the clouds. Personal detail → universal truth.
3. **Cognitive Gap** — The reader sees the world differently after reading.
4. **Rhythm** — Writing is music. Short punches + long breaths, alternating.
5. **Golden Line** — One sentence that outlives the article. 5 structural patterns to engineer them.
6. **Breadth** — Outsiders can enter. A finance piece your artist friend would share.

These principles are timeless — they work for Lu Xun, Paul Graham, Naval, and your next tweet.

## License

MIT

## Credits

Built by [AH Company](https://github.com/xiaofangkuai666-cyber) for [OpenClaw](https://github.com/openclaw/openclaw).
