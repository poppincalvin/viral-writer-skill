---
name: viral-writer
description: >
  Write viral, human-sounding long-form content for social platforms (X long posts/threads, 公众号, LinkedIn, 小红书, 抖音文案, newsletters).
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

## Entry Modes

This skill has two entry modes. Detect automatically from user input.

### Mode A: 生成模式（Topic → Article）

User provides a topic or asks to write about something. Run the full pipeline.

```
DISCOVER → BRIEF → FRAMEWORK → HOOK → DRAFT(+Craft) → FORMAT → REVIEW ⇄ DELIVER → POST-DELIVERY
```

### Mode B: 润色模式（Raw Material → Polished Article）

User provides raw text (unstructured notes, messy draft, stream-of-consciousness). Polish it into publishable content.

```
EXTRACT → BRIEF → FRAMEWORK → HOOK → REWRITE(+Craft) → FORMAT → REVIEW ⇄ DELIVER → POST-DELIVERY
```

**How to detect Mode B:** User pastes a block of text, says "帮我润色/整理/改一下", or provides notes/draft material.

**Core principle: 保留原作者的观点、事实、个人经历。只重组结构和打磨表达。**

#### Step 0B: EXTRACT（提炼）

Read the raw material and extract:

1. **核心观点**: What is the author actually trying to say? (often buried in the middle or end)
2. **关键论据**: Facts, data, personal stories, examples — preserve ALL of these
3. **情感基调**: Is the author angry? reflective? excited? — match and amplify, don't flatten
4. **素材评估**:
   - 有什么：列出可用的好素材（个人经历、数据、金句种子）
   - 缺什么：哪些论点缺支撑？哪里需要补充案例或数据？
   - 多什么：哪些内容重复或离题？建议删除

**Output to user for confirmation:**

```
EXTRACT | 素材分析
─────────────────────
核心观点: {一句话概括}
情感基调: {基调}

可用素材:
- {素材1}: {为什么好}
- {素材2}: {为什么好}
...

建议补充:
- {缺口1}: {为什么需要}
...

建议删除:
- {冗余1}: {为什么多余}
...

结构建议: {推荐框架} + {理由}
内容线: {自动判断属于哪条线}

确认后进入 BRIEF →
```

**User confirms or adjusts** → proceed to BRIEF (extract from material, not Q&A).

In Mode B, BRIEF is inferred from the material:

- **Topic**: Extracted from core message
- **Platform**: Ask if not obvious
- **Audience**: Infer from content, confirm with user
- **Voice**: Preserve author's natural voice from the raw material, enhance it
- **Goal**: Ask if not obvious

Then continue through FRAMEWORK → HOOK → REWRITE → FORMAT → REVIEW → DELIVER as normal.

#### REWRITE vs DRAFT

In Mode B, Step 4 is REWRITE, not DRAFT. The difference:

|         | DRAFT (Mode A)                  | REWRITE (Mode B)                                                      |
| ------- | ------------------------------- | --------------------------------------------------------------------- |
| Source  | Framework template + topic      | User's raw material                                                   |
| Freedom | Full creative freedom           | Bound to author's facts and opinions                                  |
| Voice   | From Voice Profile              | Extracted from raw material + enhanced                                |
| Craft   | Apply 6 principles from scratch | Apply 6 principles to restructure existing content                    |
| Can add | Anything that fits              | Only add what's missing (per EXTRACT assessment)                      |
| Cannot  | —                               | Invent facts, change opinions, add experiences the author didn't have |

**REWRITE 的 Craft 应用顺序:**

1. **认知落差**: 从 raw 素材中找到最强的认知转变，把它放大
2. **具体→普遍跳跃**: 作者的个人细节已经有了（raw素材的优势），补上"起飞"部分
3. **广度**: 确保开头能让圈外人进入
4. **密度**: 大刀砍冗余——raw素材通常最大的问题就是不够压缩
5. **节奏**: 重组句子长短，制造呼吸感
6. **金句**: 从作者的原话中提炼，或基于作者的洞察锻造

## Core Workflow

> Below are the shared steps. Mode A starts at Step 0 (Discover). Mode B starts at Step 0B (Extract, defined above) then joins at Step 1 (Brief).

### Step 0: Discover (Mode A only)

Find the right topic before you write. See `references/discovery.md` for the full methodology.

**Two sub-modes:**

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
- **Content Line**: Which content line does this belong to? See `references/voice.md` → Content Line Presets.
  - `ai-vertical` — AI + 垂直领域分享（专业可读、案例驱动）
  - `silver` — 银发经济/中老年（简洁温暖、实用为主）
  - `ai-frontier` — 前沿 AI 洞悉（快速、深度、高信息密度）
  - `custom` — 不属于以上三条线，使用通用 Voice Profile
  - **判断方式**（按优先级）:
    1. 用户显式指定（"写一篇银发线的..."）→ 直接采用
    2. Mode B 从 raw 素材自动判断 → 在 EXTRACT 输出中标注，用户确认
    3. 不确定时 → 询问用户
- **Platform (主平台)**: X 长文 / X Thread / 公众号 / LinkedIn / Newsletter / 小红书 / 抖音文案?
- **Platform (副平台, 可选)**: 同一内容需要适配的其他平台（可多选）。副平台版本在主平台完成后生成。
- **Audience**: Who reads this? (demographics, pain points)
- **Voice**: 根据 Content Line 自动加载对应 Preset（见 `references/voice.md` → Content Line Presets）。如果该线的 Preset 尚未填充，退回到 Quick Start 3 问建立临时 Voice Profile。`custom` 线始终走 Quick Start 或用户已有 Profile。
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

### Step 4: Draft / Rewrite — The Core Step

This is where the real work happens. Everything before this is preparation. Everything after is polish.

- **Mode A (生成)**: Write the full draft using the selected framework template from `references/frameworks.md`.
- **Mode B (润色)**: Restructure the user's raw material into the selected framework. See "REWRITE vs DRAFT" table above for boundaries.

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

- **X 长文**: 1000-3000 字, 富文本排版, Hook 标题 + 封面图, 深度内容首选
- **X Thread**: 5-10 条 ≤280 字符, 清单/tips/快速观点场景
- **公众号**: ~2000 chars, scene-setting opener, quotable golden lines, emoji headers
- **LinkedIn**: Professional tone, paragraph breaks, 1-3 hashtags at end
- **Discord/WhatsApp**: No markdown tables, use bullet lists, wrap links in `<>`
- **小红书**: Visual-first, emoji-heavy, shorter paragraphs, relatable tone
- **抖音文案**: 口语化短句, 3秒 Hook, 节奏标记 `[停顿]` `[画面切换]`, 60-90秒时长

**多平台分发流程（如果 BRIEF 中有副平台）:**

1. **先完成主平台版本** — 走完 FORMAT → REVIEW → DELIVER 全流程
2. **再生成副平台适配版本** — 基于主平台终稿，按目标平台规范调整：
   - 长度裁剪/扩展（公众号→X 需大幅压缩，X→公众号需扩展深度）
   - 语气微调（参考 `references/voice.md` → Adapting Voice Across Platforms 矩阵）
   - 格式转换（标题、排版、CTA 按平台惯例调整）
   - 内容线的 Voice Preset 不变，只调平台语气强度
3. **副平台版本不需要完整 REVIEW** — 做快速 Platform Fit 检查（≥7/10 即可）
4. **所有版本一起 DELIVER** — 主平台标注 `[主]`，副平台标注 `[副:平台名]`

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
- 内容线: {ai-vertical / silver / ai-frontier / custom}
- 主平台: {platform}
- 副平台: {platform list, if any}
- 选题来源: {how the topic was found}
- 使用框架: {which framework}
- Review 分数: {final score}/80

## Hook 选择记录
- 候选 Hook (5个):
  1. {hook text} — 公式: {formula} — 内部评分: {N}/10
  2. {hook text} — 公式: {formula} — 内部评分: {N}/10
  3. {hook text} — 公式: {formula} — 内部评分: {N}/10
  4. {hook text} — 公式: {formula} — 内部评分: {N}/10
  5. {hook text} — 公式: {formula} — 内部评分: {N}/10
- 最终选择: #{N} — 选择理由: {why this one}

## 写作决策记录
- 认知落差设计: {from what → to what}
- 金句: "{the golden line that made it to final}"
- 关键取舍: {what was cut, what was kept, and why}
- Craft 维度 Review 得分:
  - Hook: {N}/10 | Gap: {N}/10 | Density: {N}/10 | Craft: {N}/10
  - Breadth: {N}/10 | Voice: {N}/10 | Share: {N}/10 | Platform: {N}/10

## 数据表现 (发布后更新)

### {主平台}
- 阅读/曝光:
- 点赞:
- 评论:
- 转发/分享:

### {副平台1} (if applicable)
- 阅读/曝光:
- 点赞:
- 评论:
- 转发/分享:

## 复盘 (有数据后更新)
- 表现 vs 预期:
- 什么 worked:
- 什么 didn't:
- Hook 回溯: 选的 Hook 表现如何？评分最高的那个是否真的更好？
- 下次可复用的 pattern:
```

**2. Feed back to knowledge base**

If the content performs well (or fails notably), update:

- `素材库/案例库.md` — add any new real cases used
- `素材库/金句库.md` — add golden lines that resonated
- `方法论/标题方法论.md` — add title performance data to the validation table
- `方法论/开头方法论.md` — add opening hook performance data
- `方法论/选题方法论.md` — add topic evaluation + actual performance

**3. Every-5 Retrospective (数据驱动复盘)**

When `已发布/` accumulates每 5 篇新增（5, 10, 15...），触发一次完整复盘：

#### 3a. 分线 ROI 对比

按内容线分组统计：

```
{内容线} | 篇数 | 平均阅读 | 平均互动率 | 最佳表现 | 最差表现
---------|------|----------|-----------|---------|--------
ai-vertical | ... | ... | ... | ... | ...
silver      | ... | ... | ... | ... | ...
ai-frontier | ... | ... | ... | ... | ...
```

输出建议：哪条线继续加码 / 需要调整方向 / 可以暂停。如果用户记录了写作时间，计算时间投入 vs 产出比。

#### 3b. Hook A/B 回溯

从所有存档中提取 Hook 选择记录：

- 统计：选了内部评分最高 Hook 的文章 vs 选了非最高分 Hook 的文章，实际表现对比
- 按 Hook 公式分类统计：哪种公式在哪条内容线效果最好？
- 输出：Hook 评分系统是否准确？哪些公式值得优先使用？

#### 3c. Craft 原则关联分析

从所有存档中提取 Review 8 维度得分 vs 实际数据表现：

- 计算每个维度得分与实际阅读/互动的相关性
- 找出：哪个维度的高分最能预测实际表现？
- 如果发现某维度得分与实际表现不相关（如 Shareability 高分但转发量低），建议调整 Review 评分权重

#### 3d. 方法论自动更新建议

复盘发现的规律 → 建议更新到对应方法论文件：

| 发现类型           | 目标文件               | 更新内容                     |
| ------------------ | ---------------------- | ---------------------------- |
| 高表现标题的公式   | `方法论/标题方法论.md` | 追加验证数据、调整公式排序   |
| 高表现 Hook 的类型 | `方法论/开头方法论.md` | 追加成功案例、标注最佳内容线 |
| 高表现选题的特征   | `方法论/选题方法论.md` | 更新选题评估权重             |
| Voice Preset 迭代  | `references/voice.md`  | 根据数据微调各线 Preset      |

**执行方式**: 列出具体更新建议 → 用户确认 → 执行写入。不自动更新方法论文件。

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
