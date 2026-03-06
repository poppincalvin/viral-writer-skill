---
name: viral-writer
description: >
  Write viral, human-sounding long-form content for social platforms (X/Twitter threads, 公众号, LinkedIn, newsletters).
  Use when asked to: write a thread, draft a post, create content for social media, write with "human voice",
  去AI味写作, 写推文/长文/帖子, build personal brand content, or any content creation task targeting engagement and virality.
  Supports Chinese and English. Includes craft-driven writing, hook design, framework selection, and platform formatting.
---

# Viral Writer

Production-grade writing skill for high-engagement social content.

## Design Philosophy

**Craft is the engine. Everything else is support.**

Good writing doesn't need a "de-AI" pass — it's naturally human because every sentence is an intentional choice, not a probabilistic default. The craft principles (density, jump, cognitive gap, rhythm, golden line, breadth) are the primary quality system. De-AI patterns exist only as a safety net for edge cases.

## Local Knowledge Base

This skill is integrated with a personal writing system at `~/Documents/write-infinite/`:

```
~/Documents/write-infinite/
├── 素材库/
│   ├── 案例库.md    # Real cases by domain — inject into drafts for credibility
│   ├── 金句库.md    # Collected golden lines — reference during golden line engineering
│   ├── 热梗库.md    # Trending slang with expiry dates — check before using any slang
│   └── 结构库.md    # Proven structures with success cases — supplement frameworks.md
├── 方法论/
│   ├── 标题方法论.md  # Title formulas with validation data
│   ├── 开头方法论.md  # Opening hook types with performance data
│   └── 选题方法论.md  # Topic selection framework with historical records
├── 对标研究/          # Competitive account analyses (per account)
└── 已发布/            # Published content with performance data and retrospectives
```

**Usage rules:**

- **During DISCOVER**: Read `选题方法论.md` for historical topic performance data
- **During HOOK**: Read `标题方法论.md` + `开头方法论.md` for validated formulas
- **During DRAFT**: Read `案例库.md` for relevant cases, `金句库.md` for inspiration, `结构库.md` for proven structures
- **During DRAFT**: Check `热梗库.md` — only use slang marked as current, never use items in the expired section
- **Before writing about a niche**: Check `对标研究/` for any existing competitive analyses
- **After DELIVER**: Save to `已发布/` and update methodology files (see Post-Delivery below)

## Core Workflow

```
0. DISCOVER → 1. BRIEF → 2. FRAMEWORK → 3. HOOK → 4. DRAFT(+Craft) → 5. FORMAT → 6. REVIEW ⇄ 7. DELIVER → POST-DELIVERY
                                                        ↑                          ↓
                                                    (core step)          (loop back if score < 64)
```

### Step 0: Discover

Find the right topic before you write. See `references/discovery.md` for the full methodology.

**Two entry modes:**

- **No topic yet** → Run the full discovery pipeline: multi-source scan → trend staging → angle gap analysis → fit scoring → Top 3 recommendations
- **User has a topic** → Skip scanning, run trend check + angle gap + fit assessment only, then move to Brief

**Quick discovery pipeline:**

1. **Multi-source scan**: Search 3+ platforms based on target language (see `references/discovery.md` for source matrix)
2. **Trend staging**: Tag each topic as Rising / Peak / Declining — prioritize Rising
3. **Angle gap**: Search existing coverage, categorize angles taken, identify what's missing
4. **Fit scoring**: Rate topic on expertise, audience overlap, persona fit, uniqueness (each 1-3, need >= 8 total)
5. **Recommend**: Present Top 3 with composite scores and suggested angles

**Key principle:** Not every hot topic is worth chasing. Only chase topics where you have a genuine edge.

**Local knowledge:** Read `~/Documents/write-infinite/方法论/选题方法论.md` for the topic evaluation framework and historical performance data. Check `~/Documents/write-infinite/对标研究/` for any existing competitive analyses relevant to the topic.

After user picks a topic (or confirms their own), proceed to Brief.

### Step 1: Brief

Clarify before writing. Extract or ask:

- **Topic**: What's the core message?
- **Platform**: X thread / 公众号 / LinkedIn / Newsletter / 小红书?
- **Audience**: Who reads this? (demographics, pain points)
- **Voice**: Author's voice profile — see `references/voice.md`. If no profile exists, ask the 3 Quick Start questions to build one.
- **Goal**: Engagement? Authority? Conversion? Community?
- **Language**: 中文 / English / bilingual

### Step 2: Framework Selection

Choose the best framework based on the content type. See `references/frameworks.md` for full templates.

| Content Type          | Framework             | When to Use                       |
| --------------------- | --------------------- | --------------------------------- |
| Personal story        | **Narrative**         | Have a unique experience to share |
| Challenge consensus   | **Contrast**          | Old thinking vs new thinking      |
| Research/tips summary | **Listicle**          | Compiled knowledge or resources   |
| Shock & rebuild       | **Counter-Intuitive** | Provocative claim + evidence      |
| Transformation arc    | **Personal Journey**  | From bad → trigger → good         |

### Step 3: Hook Design

The hook determines 80% of performance. See `references/hooks.md` for formulas, A/B testing process, and examples.

Also read the local methodology files for validated formulas with performance data:

- `~/Documents/write-infinite/方法论/标题方法论.md` — title formulas with historical performance
- `~/Documents/write-infinite/方法论/开头方法论.md` — opening hook types with conversion data

**Quick formulas:**

- `[Identity] + [Secret]` → "I spent 10 years as X. Here's what nobody tells you."
- `[Number] + [Contrast]` → "From $200K debt to millionaire in 4 years (no crypto)"
- `[Time] + [Discovery]` → "I spent 500 hours studying X. These 6 things changed everything."
- `[Anti-consensus] + [Stance]` → "The most overrated career advice is actually wrong."
- `[Specific group] + [Direct]` → "If you're a 20-something founder, read this:"

**Hook test:** Read it aloud. Would you stop scrolling? Would a friend want to hear more?

### Step 4: Draft — The Core Step

This is where the real work happens. Everything before this is preparation. Everything after is polish.

Write the full draft using the selected framework template from `references/frameworks.md`.

**The 6 Craft Principles are non-negotiable. See `references/craft.md` for full methodology.**

| #   | Principle                | One-line                                | Check                                                                   |
| --- | ------------------------ | --------------------------------------- | ----------------------------------------------------------------------- |
| 1   | **Density > Length**     | Every sentence earns its place          | Can you delete any sentence without making the piece worse?             |
| 2   | **Specific → Universal** | One foot in mud, one foot in clouds     | Is there a moment where a personal detail jumps to a universal truth?   |
| 3   | **Cognitive Gap**        | Reader sees the world differently after | Does the reader's understanding shift between first and last paragraph? |
| 4   | **Rhythm**               | Writing is music                        | Are there short punches and long breaths alternating?                   |
| 5   | **Golden Line**          | One sentence that outlives the article  | Is there a line someone would screenshot or quote?                      |
| 6   | **Breadth**              | Outsiders can enter                     | Can someone outside the niche enjoy the first 3 paragraphs?             |

**Drafting order:**

1. Design the cognitive gap first (what should the reader think differently?)
2. Build the specific→universal jump (what concrete detail leaps to that truth?)
3. Check breadth (can an outsider get in?)
4. Compress for density (does every sentence earn its place?)
5. Shape rhythm (read aloud — does it have music?)
6. Forge golden lines (at least 3 candidates → best 1-2 survive)

**Pull from local knowledge base during drafting:**

- Read `~/Documents/write-infinite/素材库/案例库.md` — find relevant cases for the topic
- Read `~/Documents/write-infinite/素材库/金句库.md` — look for reusable golden lines or inspiration
- Read `~/Documents/write-infinite/素材库/结构库.md` — check if a proven structure fits better than frameworks.md templates
- Check `~/Documents/write-infinite/素材库/热梗库.md` — only use slang in the "当前流行" section

**Additional drafting rules:**

- Write in first person
- Include at least 1 specific personal detail per section
- Use concrete numbers over vague claims
- End each section with a reason to keep reading

**Safety net scan (after drafting, before formatting):**

If the draft still has obvious AI patterns after applying Craft, do a quick scan using `references/de-ai-checklist.md`. This is a debug tool, not a core step. Focus on:

- Structural patterns (总分总, 排比控, 首先其次最后) — these are timeless signals
- Voice consistency check — does it match the voice profile from Step 1?
- Read-aloud test — if it sounds like an essay, Craft wasn't applied hard enough

The word-level blacklists in de-ai-checklist.md are **dated examples** (labeled with source and year), not eternal rules. AI models evolve, words rotate. The patterns behind them are what matter.

### Step 5: Platform Formatting

Apply platform-specific rules. See `references/platforms.md`.

**Quick reference:**

- **X Thread**: ≤280 chars/tweet, 8-12 tweets optimal, number them (1/10), no markdown tables
- **公众号**: ~2000 chars, scene-setting opener, quotable golden lines, emoji headers
- **LinkedIn**: Professional tone, paragraph breaks, 1-3 hashtags at end
- **Discord/WhatsApp**: No markdown tables, use bullet lists, wrap links in `<>`
- **小红书**: Visual-first, emoji-heavy, shorter paragraphs, relatable tone

### Step 6: Review

**Role**: You are now a ruthless senior editor with 20 years of experience. You've seen thousands of viral hits and failures. Be harsh, be specific.

**Score the draft on 8 dimensions (each 1-10, total 80):**

| Dimension                           | What to evaluate                                                                                                  | Reference             |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------------------- | --------------------- |
| Hook Power                          | Would you stop scrolling? Is the promise clear?                                                                   | `hooks.md`            |
| Cognitive Gap                       | Does the reader's worldview shift after reading?                                                                  | `craft.md` P3         |
| Density                             | Does every sentence earn its place? Can you delete any paragraph without loss?                                    | `craft.md` P1         |
| Craft (Jump + Rhythm + Golden Line) | Is there a specific→universal jump? Does it have rhythm? Is there a quotable line?                                | `craft.md` P2, P4, P5 |
| Breadth                             | Can someone outside the niche enjoy the first 3 paragraphs?                                                       | `craft.md` P6         |
| Human Voice                         | Does it sound like a real person with a consistent persona? Not "is it de-AI'd" but "does it have genuine voice?" | `voice.md`            |
| Shareability                        | Would a reader screenshot this or send it to a friend?                                                            | `craft.md` P5         |
| Platform Fit                        | Does the format match the target platform's rules?                                                                | `platforms.md`        |

**Score thresholds:**

- **64+/80**: Ship it → proceed to Deliver
- **48-63**: Needs a targeted fix → identify the weakest dimension, loop back to the corresponding step
- **<48**: Major rewrite needed → loop back to Draft

**Loop-back routing** — based on the weakest dimension:

| Weakest Dimension | Route Back To  | Why                                                             |
| ----------------- | -------------- | --------------------------------------------------------------- |
| Hook Power        | Step 3: Hook   | Rewrite the hook with a different formula                       |
| Cognitive Gap     | Step 4: Draft  | Redesign the knowledge gap                                      |
| Density           | Step 4: Draft  | Compression pass — delete weak sentences, merge weak paragraphs |
| Craft             | Step 4: Draft  | Add jumps, vary rhythm, forge golden lines                      |
| Breadth           | Step 4: Draft  | Simplify entry point, add cross-domain analogies                |
| Human Voice       | Step 4: Draft  | Revisit voice profile, rewrite with persona consistency         |
| Shareability      | Step 4: Draft  | Add golden lines, stronger emotion beats                        |
| Platform Fit      | Step 5: Format | Re-apply platform rules                                         |

**Review output format:**

```
REVIEW | Score: {total}/80
─────────────────────────────
Hook:      {N}/10  {one-line verdict}
Gap:       {N}/10  {one-line verdict}
Density:   {N}/10  {one-line verdict}
Craft:     {N}/10  {one-line verdict}
Breadth:   {N}/10  {one-line verdict}
Voice:     {N}/10  {one-line verdict}
Share:     {N}/10  {one-line verdict}
Platform:  {N}/10  {one-line verdict}
─────────────────────────────

Best line:  "{the strongest sentence in the draft}"
Weakest:    "{the sentence that should be killed or rewritten first}"

Issues (line-level):
1. "{exact quote}" → {problem} → Fix: {suggestion}
2. "{exact quote}" → {problem} → Fix: {suggestion}
...

Verdict: [SHIP] / [FIX {dimension} → back to Step {N}] / [REWRITE → back to Step 4]
```

**Iteration rules:**

- Auto-iterate up to 2 rounds before presenting to user
- If still < 64 after 2 rounds, present the best version + remaining issues, let user decide
- Never iterate silently more than 2 rounds — the user should see what's happening

### Step 7: Deliver

- Present the final content in the appropriate format
- Show the final Review score so user knows quality level
- If sending to a channel, use proper message formatting
- For long content (>2000 chars on Discord), split intelligently at section breaks
- Offer variations: "要调整哪个部分？Hook可以更尖锐 / 结尾可以更有力 / 换个框架试试"
- If user requests changes → route back to the appropriate step (not always Step 4)

### Post-Delivery: Record & Learn

After content is delivered, close the loop by saving to the local knowledge base.

**1. Save to 已发布/**

Create file at `~/Documents/write-infinite/已发布/{YYYY-MM-DD}-{标题简称}.md`:

```
# {完整标题}

## 元数据
- 发布日期: {date}
- 发布平台: {platform}
- 选题来源: {how the topic was found}
- 使用框架: {which framework}
- Review 分数: {final score}/80

## 写作决策记录
- Hook 选择: {which formula, why}
- 认知落差设计: {from what → to what}
- 金句: "{the golden line that made it to final}"
- 关键取舍: {what was cut, what was kept, and why}

## 数据表现 (发布后更新)
- 阅读/曝光:
- 点赞:
- 评论:
- 转发/分享:

## 复盘 (有数据后更新)
- 表现 vs 预期:
- 什么 worked:
- 什么 didn't:
- 下次可复用的 pattern:
```

**2. Feed back to knowledge base**

If the content performs well (or fails notably), update:

- `素材库/案例库.md` — add any new real cases used
- `素材库/金句库.md` — add golden lines that resonated
- `方法论/标题方法论.md` — add title performance data to the validation table
- `方法论/开头方法论.md` — add opening hook performance data
- `方法论/选题方法论.md` — add topic evaluation + actual performance

**3. Trigger methodology review**

When `已发布/` accumulates 5+ entries, suggest running a retrospective:

- Compare scores vs actual performance — is the Review scoring calibrated?
- Find patterns in top performers — what craft principles correlated with success?
- Update methodology files with new validated rules

### Competitive Analysis (On-Demand)

Not part of the per-session writing pipeline, but available when researching a niche.

**Trigger:** User says "对标 @{账号}" or "研究一下这个账号" or provides an account to analyze.

**Process:**

1. WebSearch the account's recent high-performing content
2. Analyze top 5 posts: hook type, structure, golden lines, engagement triggers
3. Extract patterns: title formulas, recurring themes, posting rhythm
4. Separate learnable techniques from non-learnable advantages (requires specific resources/persona)
5. Save to `~/Documents/write-infinite/对标研究/{平台}-{账号名}.md`

**Output feeds into writing:** Patterns from competitive analysis inform DISCOVER (what angles work), HOOK (what formulas resonate), and DRAFT (what structures succeed in the niche).

## Multi-Dimensional Depth

When content needs intellectual depth, layer 1-2 of these perspectives. See `references/depth-lenses.md`.

- **Philosophy**: Stoicism, existentialism, Eastern philosophy (Dao, Yin-Yang)
- **Sociology**: Class/cultural capital, group behavior, generational analysis
- **Psychology**: Loss aversion, identity, cognitive load, emotional triggers, curiosity gap
- **Communication**: Clarity hierarchy, story > argument, conversation not lecture
- **Viral Science**: Social currency, practical value, triggers & top-of-mind
- **Data**: First-hand (n=1 stories) + second-hand (reports, studies)
- **Analogy**: Map unfamiliar concepts to familiar domains

**Layered writing principle:**

- Surface: Story + examples (everyone)
- Middle: Methods + actionable advice (doers)
- Deep: Theory + first principles (thinkers)

## Quality Standards

The Review step (Step 6) uses a quantitative scoring system. See `references/craft.md` for the underlying principles.

### Scoring Rubric

Each dimension is scored 1-10:

**Hook Power**

- 1-3: Generic, could be anyone's, no reason to click
- 4-6: Has a hook but weak specificity or emotion
- 7-8: Strong hook, would stop most scrollers
- 9-10: Elite hook, readers screenshot the first line alone

**Cognitive Gap**

- 1-3: Reader thinks the same before and after — no new perspective
- 4-6: Provides new information but no framework shift
- 7-8: Reader's understanding of the topic genuinely changes
- 9-10: Reframes how the reader sees the world — "I can't unsee this now"

**Density**

- 1-3: Bloated — can delete 50%+ of sentences without loss
- 4-6: Some filler, some weak sentences, but core is solid
- 7-8: Tight — every paragraph earns its place
- 9-10: Compressed like poetry — every sentence carries weight, nothing to cut

**Craft (Jump + Rhythm + Golden Line)**

- 1-3: No specific→universal jump, monotonous rhythm, no memorable line
- 4-6: Has one of the three but not all
- 7-8: Has a clear jump, varied rhythm, and at least 1 golden line
- 9-10: The jump gives you chills, the rhythm makes you read aloud, the golden line gets tattooed

**Breadth**

- 1-3: Only insiders can understand — full of jargon, no bridges
- 4-6: Somewhat accessible but non-experts lose interest quickly
- 7-8: Clear entry point for outsiders, professional concepts well-bridged
- 9-10: Anyone can enjoy it — a finance piece your artist friend would share, a tech piece your mom would read

**Human Voice**

- 1-3: Generic, could be anyone or anything — no personality, no persona
- 4-6: Has some personality but inconsistent or occasionally slips into default AI patterns
- 7-8: Consistent voice throughout, sounds like a specific real person
- 9-10: Unmistakably one person — you'd recognize this voice in a blind test

**Shareability**

- 1-3: No reason to share, no golden lines, no practical value
- 4-6: Interesting but not screenshot-worthy
- 7-8: Has 1-2 golden lines or highly actionable takeaways
- 9-10: Multiple "I need to send this to someone" moments

**Platform Fit**

- 1-3: Wrong format, wrong length, wrong tone for the platform
- 4-6: Correct format but not optimized (e.g., thread too long)
- 7-8: Well-formatted, follows platform conventions
- 9-10: Exploits platform-specific features for maximum reach

### Thresholds

| Score | Verdict       | Action                       |
| ----- | ------------- | ---------------------------- |
| 72-80 | Exceptional   | Ship immediately             |
| 64-71 | Ready to ship | Ship with confidence         |
| 56-63 | Almost there  | Fix the weakest 1 dimension  |
| 48-55 | Needs work    | Fix the weakest 2 dimensions |
| < 48  | Major issues  | Rewrite from Draft step      |
