# 📚 Literature Review Skill for Claude

> **让 Claude 像学术导师一样，陪你从零构建一篇发表级文献综述。**
>
> **Turn Claude into your academic mentor — guiding you step-by-step to craft a publication-ready literature review from scratch.**

A seven-phase, problem-driven Claude Custom Skill that transforms literature review writing from "summarizing what scholars said" into "constructing a scholarly argument."

一个七阶段、问题驱动的 Claude 自定义技能，将文献综述从「文献搬运」升级为「学术论证」。

---

## ✨ Core Philosophy | 核心理念

> A literature review is NOT a summary of what scholars have said. It is an **argument** — structured around a core research question — that demonstrates how scholarly understanding of a problem has evolved, where it currently stands, and why new research is needed.
>
> 文献综述不是学者们说了什么的摘要，而是围绕核心研究问题构建的**论证**——它展示了学术界对一个问题的理解如何演变、目前处于什么状态、以及为什么需要新的研究。

**The Golden Rule | 黄金法则：**

Problem-driven, not literature-driven. The reader should finish the review understanding the intellectual landscape of a question, not a catalogue of publications.

问题驱动，而非文献驱动。读者读完你的综述，应该理解一个学术问题的智识版图，而不是看到一份出版物清单。

---

## 🎯 Why You Need This Skill | 为什么需要这个 Skill

Without this Skill, asking AI to "write a literature review" typically produces:

直接让 AI "帮我写一篇文献综述"，你大概率会得到：

- ❌ "Scholar X argued that..." style summaries — 一堆文献搬运式描述
- ❌ Chronological or thematic lists with no argumentative thread — 按时间/主题罗列，没有论证主线
- ❌ No distinction between journal quality — 不区分期刊质量，MDPI 和顶刊混为一谈
- ❌ "Nobody has studied X" as a research gap — 以"没人研究过 X"草率收尾
- ❌ One-shot output with zero user involvement — 一次性输出，没有任何用户参与

**With this Skill, you get | 使用本 Skill 后：**

- ✅ Argument-driven review structured around a core research question — 围绕核心问题构建的论证式综述
- ✅ Strict "understand first, search later" workflow — 先理解研究、再搜索文献的严格流程
- ✅ Three-tier journal quality filtering — 三级期刊质量过滤体系
- ✅ Exemplar analysis before writing — 拆解顶刊范文后再动笔
- ✅ Phase-by-phase confirmation, section-by-section review — 逐阶段确认、逐节审阅的协作模式

---

## 🔄 Seven-Phase Workflow | 七阶段工作流程

```
Phase 1: Research Understanding         研究理解 — 苏格拉底式对话
    ↓ user confirms | 用户确认
Phase 2: Literature Discovery           文献发现 — 种子 → 滚雪球 → 筛选
    ↓ user confirms corpus | 用户确认语料库
Phase 3: Full-text Acquisition          全文获取 — 自动获取 + 缺失清单
    ↓ user provides missing papers | 用户补充缺失文献
Phase 4: Exemplar Analysis              范例分析 — 拆解 2-3 篇顶刊综述
    ↓
Phase 5: Architecture Design            架构设计 — 论证结构提交审批
    ↓ user approves | 用户审批
Phase 6: Section-by-Section Draft       逐节撰写 — 写一节、审一节
    ↓ user approves all sections | 用户逐节审批
Phase 7: Integration & Polish           整合润色 — 合并、校验、交付
```

Every phase has a **Hard Gate** — Claude will never proceed without your explicit confirmation.

每个阶段都设有**硬性关卡**——未经你明确确认，Claude 绝不会擅自推进。

---

## 📖 Phase Details | 各阶段详解

### Phase 1: Research Understanding | 研究理解

Socratic questioning (one question at a time) to collect:

通过苏格拉底式提问（每次只问一个问题）收集：

| Item | 信息项 | Description | 说明 |
|------|--------|-------------|------|
| Research topic & object | 研究主题与对象 | What exactly are you studying? | 你具体在研究什么？ |
| Core research question | 核心研究问题 | What question does your research answer? | 你的研究回答什么问题？ |
| Disciplinary positioning | 学科定位 | Which academic field(s) and conversations? | 属于哪个学术领域和对话？ |
| Theoretical orientation | 理论取向 | What theoretical lens or framework? | 使用什么理论框架？ |
| Hypothesized contribution | 预期贡献 | What does your research add? | 你的研究增加了什么？ |
| Literature scope | 综述范围 | Language, time span, key journals | 语言、时间跨度、核心期刊 |
| Output requirements | 输出要求 | Word count, language, format | 目标字数、语言、格式 |

After collecting all information, Claude generates a structured summary for your confirmation — **only then does literature searching begin.**

全部收集后，Claude 生成结构化摘要请你确认——**确认后才开始搜文献。**

### Phase 2: Literature Discovery | 文献发现

- **Seed papers | 种子文献**: 5-8 highly cited, high-impact core papers | 高被引核心论文
- **Snowball expansion | 滚雪球扩展**: Forward/backward citation tracking | 正向/反向引文追踪
- **Curate to 30-50 papers | 筛选至 30-50 篇**: Filtered by journal tier, temporal balance, and perspective diversity | 按期刊层级、时间平衡、观点多样性筛选

### Phase 3: Full-text Acquisition | 全文获取

- Auto-attempts OA channels (OpenAlex, Semantic Scholar, institutional repos) | 自动尝试 OA 渠道
- Generates a clear **missing papers list** with DOIs for papers behind paywalls | 无法获取的生成含 DOI 的缺失清单
- **Never silently skips any paper | 绝不会静默跳过任何文献**

### Phase 4: Exemplar Analysis | 范例分析

Before writing, dissect 2-3 top-journal literature reviews:

在动笔前，拆解 2-3 篇顶刊文献综述：

- Section architecture & logical flow | 章节架构与逻辑流
- Argumentative strategy (theoretical debate? empirical contradiction? conceptual genealogy?) | 论证策略
- Citation technique (clustered vs. individual) | 引用技巧（聚类 vs 逐篇）
- Transition logic & opening strategy | 转场逻辑与开篇策略

### Phase 5: Architecture Design | 架构设计

Design principles | 设计原则：

1. **One core question runs through the entire review | 一个核心问题贯穿全文**
2. **Sections represent shifts in the answer, not shifts in chronology | 章节代表「答案的转变」而非「时间的推移」**
3. **The research gap emerges from the logic of the argument | 研究缺口从论证逻辑中浮现**
4. **The opening creates cognitive tension | 开篇制造认知张力** — an anomaly, contradiction, or puzzle | 异常、矛盾或谜题

### Phase 6: Drafting | 逐节撰写

Writing rules | 写作规范：

```
❌ BAD:  "Hsing (2010) argued that local governments compete for land rents."
         Scholar X argued... 式文献搬运

✅ GOOD: "Local governments compete fiercely to capture land rents, using
         construction projects to consolidate territorial authority (Hsing, 2010)."
         观点先行，引用为证
```

- Claim first, citation as evidence (parenthetical) | 观点先行，括号引用为证
- Cluster citations for shared claims | 多来源支持同一论点时聚类引用
- Every paragraph must serve the argument | 每段必须服务于论证
- Transitions are arguments, not connectors | 转场即论证，不写"接下来讨论..."

### Phase 7: Integration & Polish | 整合润色

- Merge all approved sections | 合并全部已审批章节
- Cross-check citation consistency (text ↔ reference list) | 交叉校验引用一致性
- Verify journal names, years, volume/issue numbers | 核实期刊名、年份、卷期号
- Final read for argumentative coherence | 通读论证连贯性
- Deliver final version | 交付最终版本

---

## 📊 Journal Tier System | 期刊质量分层体系

Built-in three-tier filtering (example for Urban Studies / China Studies — customizable for your field):

内置三级期刊过滤（以城市研究/中国研究为例，可按你的领域自定义）：

| Tier | 层级 | Role | 定位 | Examples | 示例 |
|------|------|------|------|----------|------|
| **Tier 1** | 第一梯队 | Must-use if relevant | 必须使用 | *Urban Studies*, *IJURR*, *Environment and Planning A/B/C/D*, *The China Quarterly*, *World Development* |
| **Tier 2** | 第二梯队 | Strong sources | 优质来源 | *Cities*, *Habitat International*, *Regional Studies*, *China Economic Review*, *Geoforum* |
| **Tier 3** | 第三梯队 | Search clues only | 仅作搜索线索 | MDPI series (*Land*, *Sustainability*), SCIRP, conference proceedings, working papers |

> Books from major university presses (Oxford, Cambridge, Chicago, etc.) are equivalent to Tier 1.
>
> 主要大学出版社的学术专著等同于 Tier 1。

---

## 🚫 Seven Anti-Patterns | 七大反模式

| # | Anti-pattern | 反模式 | Correct approach | 正确做法 |
|---|-------------|--------|-----------------|----------|
| 1 | Searching before understanding the research | 没理解研究就搜文献 | Phase 1 must complete first | Phase 1 完成前禁止搜索 |
| 2 | Organizing by chronology | 按时间顺序组织 | Organize by argumentative logic | 按论证逻辑组织 |
| 3 | Treating all papers equally | 所有文献平均用力 | Allocate space by argumentative importance | 按论证重要性分配篇幅 |
| 4 | Claiming "nobody has studied X" | 声称"没人研究过 X" | Acknowledge adjacent work, specify what's unintegrated | 承认相邻研究，指出未整合之处 |
| 5 | Using low-tier journals as primary evidence | 引用低质量期刊作为主要证据 | Three-tier filtering; Tier 3 as clues only | Tier 3 仅作线索 |
| 6 | Writing before studying exemplars | 不看范文就动笔 | Phase 4 mandates exemplar analysis | Phase 4 强制拆解范例 |
| 7 | Delivering a complete draft at once | 一次性交付完整初稿 | Section-by-section drafting & review | 逐节撰写、逐节审阅 |

---

## 🚀 Quick Start | 快速开始

### Option A: Project Skill (Recommended) For ClaudeCode | 方式一：对于Claudecode使用者

1. Clone this repo into your project's .claude/skills/ directory| 将该仓库克隆到项目的 .claude/skills/ 目录中
2. Start a conversation: **"帮我写一篇文献综述"** or **"Help me write a literature review"**

### Option B: In-conversation Upload For Claude.ai | 方式二：对于Claude.ai使用者

1. Sign in to claude.ai Create a new Project Click 'Add Content' → Upload `SKILL.md`｜ 登录claude.ai创建项目然后上传`SKILL.md`
2. Start chatting: **"请按照这个 Skill 帮我写文献综述"** or **"Follow this Skill to help me write a literature review"**

### How to Verify | 验证是否生效

If Claude starts asking questions one by one (rather than immediately searching or generating an outline), the Skill is loaded correctly.

如果 Claude 开始逐个提问（而不是直接搜索文献或生成大纲），说明 Skill 已正确加载。

---

## 🛠️ Tool Ecosystem | 工具生态

建议安装web-access skill：https://github.com/eze-is/web-access，提升claudecode联网查询的能力，便于进行文献搜索。

---

## 💡 Tips for Best Results | 使用建议

**Invest time in Phase 1 | 在 Phase 1 投入充足时间**

The Socratic dialogue is the foundation. The clearer your research question, the exponentially better every subsequent phase will be. If you haven't figured out your contribution yet, let Claude help you think it through.

苏格拉底式对话是整个流程的基石。研究问题越清晰，后续每一步质量都会指数级提升。

**Prepare to manually fetch some papers | 准备手动获取部分文献**

Paywalls mean some papers always need institutional access. The Skill gives you a clear missing list with DOIs — just download and upload.

付费墙意味着总有部分文献需要机构订阅下载。Skill 会给你含 DOI 的清晰清单。

**Take section reviews seriously | 认真对待逐节审阅**

Academic writing is deeply personal. Actively provide revision feedback — don't just say "looks good."

学术写作高度个人化。积极提出修改意见，不要只说"可以"。

**Customize journal tiers for your field | 自定义你的期刊层级**

The built-in list targets Urban Studies / China Studies. Tell Claude your field's key journals during Phase 1.

内置列表以城市研究/中国研究为基准。在 Phase 1 中告知 Claude 你的核心期刊列表。

---

## 📄 License

MIT

---

## 🤝 Contributing

Issues and PRs are welcome | 欢迎提交 Issue 和 PR：

- Add journal tier lists for other disciplines | 为其他学科补充期刊层级列表
- Improve writing rules or add new anti-patterns | 改进写作规范或新增反模式
- Integrate more literature discovery MCP tools | 集成更多文献检索 MCP 工具
- Share usage experiences and improvement suggestions | 分享使用体验和改进建议

---

<p align="center">
  <strong>Problem-driven, not literature-driven.</strong><br>
  <strong>问题驱动，而非文献驱动。</strong><br><br>
  Built as a Claude Custom Skill | 为 Claude 打造的自定义技能
</p>
