# De-AI Checklist — Safety Net

**This is NOT a core step. It's a debug tool.**

If the Craft principles (`craft.md`) are applied properly during drafting, most AI patterns will be eliminated naturally. This checklist exists as a quick scan to catch anything that slipped through.

**When to use:**

- After applying Craft in the Draft step, if the result still feels "off"
- When the Review step scores Human Voice < 6
- As a learning reference to understand common AI writing patterns

**When NOT to use:**

- As a substitute for Craft — fixing AI words without fixing density/rhythm/voice is lipstick on a pig
- As a rigid word-ban list — if a "blacklisted" word serves the craft (rhythm, emphasis, golden line), it stays

The word-level blacklists below are **dated examples**, not eternal rules. AI models evolve. The structural patterns behind these words are what matter long-term.

---

## Quick Scan Passes

If you need to run a de-AI scan, these 5 passes remain useful:

## Pass 1: Person (人称转换)

Replace third-person abstractions with first/second person.

| Before (AI smell) | After (human)             |
| ----------------- | ------------------------- |
| 人们普遍认为      | 我发现 / 你可能也觉得     |
| 研究表明          | 我注意到 / 我看到一个数据 |
| 许多创业者面临    | 我创业第一年              |
| 这一现象值得关注  | 这事儿让我睡不着觉        |

### 🔧 去结构化（新增）

**移除机械结构词**，改为自然过渡：

| Before (AI结构化) | After (人话) |
| ----------------- | ------------ |
| 首先              | 说起来       |
| 其次              | 还有         |
| 最后              | 完了         |
| 综上所述          | 说到底       |
| 总的来说          | 其实吧       |

**规则**：一段话不要超过2个"然后/而且/同时"连着用

## Pass 2: Detail (具体化)

Every abstraction gets one concrete anchor.

| Before           | After                                   |
| ---------------- | --------------------------------------- |
| 很多人有类似经历 | 我问了47个人，38个说了几乎一样的话      |
| 我学到了一个道理 | 那是2021年3月的周二，在星巴克里想明白的 |
| 效果很好         | 转化率从2.1%涨到7.8%，三周内            |
| 成本很高         | 一个月烧了$4,200，比我房租还贵          |

## Pass 3: Emotion (情感注入)

Mark 3 emotional beats in the draft. Rewrite them with raw honesty.

| Before (performed) | After (authentic)                          |
| ------------------ | ------------------------------------------ |
| 这令人深感忧虑     | 看到这数据我真的慌了——说实话，有点生气     |
| 这让人非常激动     | 我当时差点从椅子上跳起来                   |
| 这是一个困难的决定 | 我删了又写，写了又删，最后凌晨三点才定下来 |

## Pass 4: Imperfection (不完美化)

Inject humanity. Add at least 2 of these:

- "我不确定这对每个人都适用，但..."
- "说实话，我可能是错的"
- "（写到这里我犹豫了三分钟要不要发）"
- "这个观点可能会挨骂，但我还是想说"
- "后来证明我当时想多了/想少了"
- 承认运气的作用
- 承认自己不知道的部分

## Pass 5: Read-Aloud (朗读测试)

Read the entire piece out loud. Fix:

- Anything that sounds like a textbook → rewrite conversationally
- Sentences over 40 chars without a breath → split
- Transition words that feel mechanical → remove or replace with natural flow
- Any section where you get bored reading → cut or restructure

### 🔧 重构逻辑（新增）

**故意增加逻辑跳跃和转折**，模拟人类思考过程：

| Before (AI线性逻辑) | After (人话)                        |
| ------------------- | ----------------------------------- |
| 价格合理，性价比高  | 价格还行，但上海打本确实比老家贵... |
| 服务好，体验不错    | 服务挺好的——不过我要说一句...       |
| 效果显著            | 效果还行吧，反正我是踩了坑才搞明白  |

**技巧**：

- 每段加1-2个"不过"、"但是"、"说白了"
- 可以"突然想到"、"扯远了"、"回来继续说"
- 让结论来的意外一点，不是顺理成章

### 🔧 标点故障（新增）

**故意打破完美标点**，增加随意感：

| Before (AI标准)              | After (人话)                                        |
| ---------------------------- | --------------------------------------------------- |
| 店内服务很好，工作人员热情。 | 店内服务很棒~ 工作人员都非常热情！从进门那一刻起... |
| 这是一个很好的选择。         | 这选择...还行吧（。                                 |
| 效果非常好，值得推荐。       | 效果真的很好！值得推荐。。。                        |

**技巧**：

- 适当用"～" "。。。" "！"
- 可以一个句子接一个句子不用任何连接词
- 断句可以很奇怪，比如"那天，我，记得，那是个周三"

## 中文 AI-Smell 词汇参考（snapshot: 2025年，基于 ChatGPT/DeepSeek 时代模型）

数据来源：北京语言大学 ACL 2023 中文AI文本对比研究、多个去AI味实践社区交叉验证（CSDN、53AI、博客园）、AI检测平台实测反馈。

**注意：这是快照，不是永恒规则。** AI模型在进化，这些词的AI信号强度会随时间变化。关注背后的**模式**（机械结构、过度正式、缺乏个性）比记住具体的词更重要。

以下分级基于：(1) 学术论文的词性分布发现（AI文本副词显著偏高），(2) 3个以上独立来源交叉确认，(3) 社区实测的检测器触发率。

### Tier 1: 核弹级（多源确认，检测器高触发）

| AI词/句式                     | 确认来源                               | 人话替换                                                      |
| ----------------------------- | -------------------------------------- | ------------------------------------------------------------- |
| 值得注意的是                  | 3+社区源、检测器高触发                 | 有意思的是 / 说句大实话 / 别忽略                              |
| 综上所述 / 总而言之           | 3+社区源、检测器高触发                 | 说到底 / 反正就是 / 所以                                      |
| 在当今社会 / 在这个时代       | 3+社区源                               | （直接删掉，跟英文 "in today's fast-paced world" 一样是废话） |
| 随着XX的发展/不断进步         | 3+社区源                               | （删掉或具体化："2024年XX用户突破1亿后"）                     |
| 首先...其次...最后            | 3+社区源、ACL论文（AI副词/连接词偏高） | 去掉序号词，用自然过渡或直接开始                              |
| 不仅...而且 / 不仅如此        | 3+社区源                               | 用逗号连接 / "而且" / "还"                                    |
| 具有重要意义 / 发挥着关键作用 | 3+社区源                               | 很重要 / 关键 / 不搞定就完了                                  |
| 与此同时                      | 3+社区源                               | 同时 / 这时候 / 另一边                                        |

### Tier 2: 强信号（2+源确认）

| AI词/句式           | 确认来源 | 人话替换                             |
| ------------------- | -------- | ------------------------------------ |
| 不言而喻 / 毋庸置疑 | 2+社区源 | （删掉。如果真的不言而喻就不需要说） |
| 不容忽视 / 需要注意 | 2+社区源 | 别小看 / 小心                        |
| 此外                | 2+社区源 | 对了 / 还有个坑 / 补一句             |
| 然而 / 因此         | 2+社区源 | 但 / 不过 / 所以 / 说白了            |
| 至关重要            | 2+社区源 | 真的很重要 / 要命                    |
| 显著                | 2+社区源 | 明显 / 肉眼可见                      |
| 深入探讨/深入分析   | 2+社区源 | 聊聊 / 说说 / 拆解一下               |
| 不可否认            | 2+社区源 | 确实 / 没错                          |
| 阐述 / 确保         | sohu源   | 说明 / 保证                          |

### Tier 3: 中文特有的AI模式（学术研究 + 社区共识）

这些不是单个词，而是AI中文写作的**结构性模式**：

**成语/四字词过量**

- AI爱堆成语："无微不至""应有尽有""独树一帜""有条不紊"
- 人类写作中成语密度远低于AI生成的中文
- 规则：一段最多1个成语，且必须用在刀刃上

**排比句泛滥**

- AI爱写："XX是YY，XX是ZZ，XX是WW"的三连排比
- 人类偶尔用排比，但不会每段都用
- 规则：全文最多1组排比句

**语气词缺失**（ACL论文发现：AI文本副词偏高但语气词偏低）

- 人类中文写作自然带语气词：啊、吧、呢、嘛、哎、诶、嗯
- AI几乎不用这些词
- 修复：每500字至少出现2-3个语气词

**数据表述过于精确**

- AI："占比为67.3%"
- 人类："大概三分之二" / "将近七成"
- 修复：非必要不用小数点，用模糊但生动的表述

**被动语态过多**

- AI："该方法被广泛应用于..."
- 人类："大家都在用这个方法"
- 修复：中文天然倾向主动语态，被动句一出现就是AI信号

### 高频强化词去重

AI喜欢重复使用同样的强化词。批量替换：

| 高频词   | 替换池（轮换使用）            |
| -------- | ----------------------------- |
| 非常     | 太 / 超级 / 贼 / 巨 / 特别    |
| 真的     | 讲真 / 说实话 / 其实 / 实话说 |
| 非常感谢 | 谢了 / 感恩 / 多谢            |
| 非常重要 | 要命 / 关键 / 核心 / 命根子   |
| 完美     | 刚好 / 合适 / 还不错          |
| 一定     | 大概率 / 八九不离十           |

**规则**：同一段落同一词不出现2次以上。Ctrl+F 全文搜索高频词。

### 中文AI句式模式

| AI模式     | 例子                                            | 为什么是AI                 |
| ---------- | ----------------------------------------------- | -------------------------- |
| 总分总结构 | "XX很重要。第一...第二...第三...总之XX很重要。" | 教科书模板，人类不这么说话 |
| 万能开头   | "在当今...随着..."                              | 空洞的宏观背景铺垫         |
| 并列控     | 每段都是3个并列短语                             | AI的"平衡感"强迫症         |
| 完美总结   | 结尾必升华、必鼓励                              | 人类结尾可以很突然、很随意 |
| 正反都说   | "一方面...另一方面..." 每个观点都两面看         | 人类会偏向一边，AI怕得罪人 |

## Final Sanity Check

After all 5 passes, verify:

- [ ] No paragraph is longer than 4 sentences
- [ ] At least 1 joke, self-deprecation, or aside per 500 words
- [ ] The opening line has zero AI-smell words
- [ ] There is at least one sentence that only YOU could have written (specific personal detail)
- [ ] Reading it cold, you'd believe a human wrote it

### 🔧 多举自己的例子（增强）

每个观点至少配1个**自己的真实例子**：

| 只有观点       | +自己的例子                            |
| -------------- | -------------------------------------- |
| 做自媒体要坚持 | 我坚持了半年，每天写，现在终于有起色了 |
| AI写作需要调试 | 我那篇爆款改了7遍，第一版简直不能看    |
| 选城市很重要   | 我从北京逃到成都，工资降了但幸福感涨了 |

**技巧**：

- 用"上次"、"去年"、"我有个朋友"
- 越具体越好：日期、地点、人物、对话
- 甚至可以加"具体是谁就不说了"制造神秘感

### 🔧 去专业化：比喻 + 玩梗（新增）

**用通俗比喻解释专业概念**：

| Before (专业) | After (比喻)                 |
| ------------- | ---------------------------- |
| 现金流断裂    | 钱烧没了，发不出工资         |
| 增长黑客      | 疯狂但有效的增长野路子       |
| 认知差        | 你知道但别人不知道的信息优势 |

**技巧**：

- 加1-2个当下热梗/网络用语（但别过度）
- 用生活中熟悉的事物类比
- 自嘲比直接夸更真实

---

## English De-AI Guide

The 5-pass system above works for both languages. Below are English-specific patterns and fixes.

Data sources: Max Planck Institute excess vocabulary study (14M abstracts, arxiv 2406.07016), FSU "Why Does ChatGPT Delve" study (arxiv 2412.11385), GPTZero analysis (3.3M texts), IsGPT.org Top 50 AI phrases.

### English AI-Smell Word Reference (snapshot: 2024-2025, based on GPT-3.5/GPT-4/Claude era)

**Note:** These are dated examples. The FSU study already found "delve" declining since April 2024 as models adjust. Focus on the **patterns** (overuse of fancy synonyms, mechanical connectors, empty intensifiers), not the specific words.

**Tier 1: Nuclear red flags** (data-confirmed, 100x+ overuse vs human writing)

| AI Word/Phrase                  | Overuse Signal                    | Human Alternative                    |
| ------------------------------- | --------------------------------- | ------------------------------------ |
| delve / delves / delving        | +6,697% since ChatGPT (FSU study) | dig into / look at / explore         |
| valuable insights               | 230-902x (IsGPT)                  | what I learned / the takeaway        |
| tapestry / rich tapestry        | 227x (IsGPT)                      | (delete the metaphor entirely)       |
| indelible mark                  | 275-319x (IsGPT)                  | lasting impact / changed everything  |
| plays a crucial role in shaping | 182-250x (GPTZero/IsGPT)          | matters a lot for / shapes           |
| in today's fast-paced world     | 107x (GPTZero)                    | (delete the entire sentence)         |
| unwavering commitment           | 256x (IsGPT)                      | stayed committed / kept going        |
| casting long shadows            | 561x (IsGPT)                      | (delete — pure AI filler)            |
| fostering a sense of            | 138x (IsGPT)                      | building / creating                  |
| adds a layer of complexity      | 194x (IsGPT)                      | makes it harder / complicates things |
| opens new avenues               | 206x (IsGPT)                      | creates opportunities / leads to     |

**Tier 2: Strong signals** (10-100x overuse, or 500%+ frequency increase)

| AI Word/Phrase           | Overuse Signal                     | Human Alternative                     |
| ------------------------ | ---------------------------------- | ------------------------------------- |
| showcasing               | +1,396%, 20x (FSU/GPTZero)         | showing / proving                     |
| underscores              | +904%, r=13.8 (FSU/MPI)            | highlights / shows                    |
| intricate / intricacies  | +611%, 165x in phrases (FSU/IsGPT) | complex / tricky / messy              |
| realm                    | in focal words list (FSU)          | space / world / area                  |
| surpassing               | +667%, 12x (FSU/GPTZero)           | beating / passing                     |
| groundbreaking           | in focal words (FSU)               | new / first-of-its-kind               |
| pivotal                  | 131x in phrases (IsGPT)            | key / turning point                   |
| crucial                  | frequency gap 0.026 (MPI)          | really important / critical           |
| aligns                   | 16x (GPTZero)                      | matches / fits                        |
| comprehensive            | in common excess words (MPI)       | full / complete / thorough            |
| notably                  | in common excess words (MPI)       | especially / worth mentioning:        |
| embark on                | community consensus + lists        | start / begin / kick off              |
| remarked                 | 18x (GPTZero)                      | said / told me                        |
| landscape (metaphorical) | community consensus + lists        | scene / space / world                 |
| navigate (metaphorical)  | community consensus + lists        | deal with / figure out / work through |

**Tier 3: Moderate signals** (common in AI but also used by humans — flag only when clustered)

| AI Word/Phrase               | Note                                              | Human Alternative           |
| ---------------------------- | ------------------------------------------------- | --------------------------- |
| Furthermore / Moreover       | AI connector habit, but humans use too            | And / Plus / Also           |
| However                      | Only a signal when every paragraph starts with it | But / Thing is —            |
| In conclusion / To summarize | AI wrap-up habit                                  | So — / Bottom line —        |
| It's important to note       | AI hedging pattern                                | Look — / Here's the thing — |
| Significant                  | Only when used as empty intensifier               | Big / Real / Actual         |
| Additionally                 | In common excess words (MPI)                      | And / Oh, and —             |
| Enhance / Enhancing          | In common excess words (MPI)                      | Improve / Make better       |

**Removed from previous version** (no quantitative AI-specific signal):

- ~~Leverage~~ — traditional writing advice, not AI-specific
- ~~Utilize~~ — traditional writing advice (but still bad writing)
- ~~Facilitate~~ — no data
- ~~Beacon of~~ — no quantitative data

### English AI-Smell Phrase Patterns

Beyond individual words, these structural patterns are strong AI signals (from Plus AI / community analysis):

| Pattern                        | Example                                              | Why It's AI                                                                |
| ------------------------------ | ---------------------------------------------------- | -------------------------------------------------------------------------- |
| "It's not X, it's Y" structure | "It's not about the money. It's about freedom."      | AI loves contrasting pairs. Humans do too — but AI does it in EVERY piece. |
| Dramatic flattery opener       | "Great question!" / "What a fascinating topic!"      | Humans don't narrate their reactions to prompts.                           |
| Excessive signposting          | "Here's the key takeaway" / "Let me break this down" | 1-2 is fine. AI does it every other paragraph.                             |
| Perfect parallel lists         | Every bullet same length, same structure             | Break the pattern. Make the last item different.                           |
| "And honestly? That's rare."   | Standalone dramatic sentence after a claim           | AI-generated pseudo-authenticity.                                          |

### English Sentence Pattern Fixes

| AI Pattern                               | Human Pattern                       |
| ---------------------------------------- | ----------------------------------- |
| Long compound sentence with semicolons   | Split into 2-3 short sentences      |
| "This is not just X; it's Y"             | "Forget X. It's Y."                 |
| "While X, it's important to Y"           | "X. But here's what matters: Y."    |
| "One might argue that..."                | "You could say..." / "Sure, maybe." |
| Perfect parallel structure in every list | Break the pattern on the last item  |
| "The reality is that..."                 | "Truth is," / "Real talk:"          |

### English Imperfection Techniques

- Start a sentence with "And" or "But" — frequently
- Use dashes — like this — instead of parenthetical clauses
- One-word paragraphs. Seriously.
- Fragment sentences for emphasis. Not always complete thoughts.
- Use contractions (don't, can't, won't) — AI often avoids them
- End with a preposition if it sounds natural ("the thing I'm most excited about")
- Rhetorical questions that you actually don't answer
- "I think" / "I'm not sure" / "honestly" — sprinkle real uncertainty

### English Rhythm

AI tends to write every sentence at the same medium length. Human writing has rhythm:

```
Short punch. Short punch.
Then a longer, more reflective sentence that gives the reader room to breathe and process what you just said.
One word.
And then back to medium pace with a casual aside (like this one).
```

Rule of thumb: after every 2 medium sentences, insert either a short punch (< 8 words) or a long breath (> 25 words). Never three medium sentences in a row.
