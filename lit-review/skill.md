---
name: lit-review
description:
  Use this skill whenever the user asks to write, draft, or help with a literature review for academic research.
  Triggers include any mention of 'literature review', 'lit review', 'research gap', 'review the literature',
  'survey of existing research', 'scholarly review', or requests to find and synthesize academic papers on a topic.
  This skill orchestrates a multi-phase process from understanding the research to producing a publication-ready
  literature review. It MUST be invoked before any literature searching or review writing begins.
---

# Literature Review Skill

## Core Philosophy

A literature review is NOT a summary of what scholars have said. It is an **argument** — structured around a core research question — that demonstrates how scholarly understanding of a problem has evolved, where it currently stands, and why new research is needed. Every citation is **evidence** supporting a claim, not a description of a study.

**The golden rule: problem-driven, not literature-driven.** The reader should finish the review understanding the intellectual landscape of a question, not a catalogue of publications.

## Hard Gate

**DO NOT search for literature, outline, or begin writing until Phase 1 (Research Understanding) is fully completed and confirmed by the user.** The quality of a literature review depends entirely on the clarity of the research question it serves. Rushing to search before understanding the research guarantees a mediocre product.

## Process Overview

```
Phase 1: Research Understanding (Socratic dialogue with user)
    ↓ user confirms
Phase 2: Literature Discovery (seed → snowball → curate)
    ↓ user confirms corpus
Phase 3: Full-text Acquisition (self-attempt → user assistance)
    ↓ user provides missing papers
Phase 4: Exemplar Analysis (dissect 2-3 top-journal lit reviews)
    ↓
Phase 5: Architecture Design (propose structure for user approval)
    ↓ user approves
Phase 6: Drafting (write section by section, user reviews each)
    ↓ user approves all sections
Phase 7: Integration & Polish (combine, check citations, finalize)
```

---

## Phase 1: Research Understanding

### Goal
Achieve crystal-clear understanding of the user's research before touching any literature. Use Socratic questioning — one question at a time, building on each answer.

### Required Information (must collect ALL before proceeding)

1. **Research topic & object**: What exactly are you studying? What is the empirical case or phenomenon?
2. **Core research question**: What question does your research answer? (If the user can't articulate this clearly, help them formulate it through dialogue.)
3. **Disciplinary positioning**: Which academic field(s) does this sit in? Which scholarly conversations does it join?
4. **Theoretical orientation**: What theoretical lens or framework are you using or building on?
5. **Hypothesized contribution**: What do you think your research adds to existing knowledge? What makes your case or argument distinctive?
6. **Literature review scope**: What language (English, Chinese, both)? What time span? What journals matter most in your field?
7. **Output requirements**: Target word count? Part of a larger paper or standalone? Language of output?

### Questioning Strategy

- Ask ONE question per message. Do not overwhelm.
- Prefer multiple-choice when possible to help users clarify their thinking.
- When the user's answer is vague, probe deeper: "You mentioned X — can you be more specific about what makes this different from Y?"
- If the user struggles to articulate their contribution, offer candidate framings: "Based on what you've described, your contribution might be framed as A, B, or C — which resonates most?"
- Summarize your understanding after collecting all information and ask the user to confirm before proceeding.

### Confirmation Gate

Before moving to Phase 2, present a structured summary:

> **Research Summary for Confirmation:**
> - Topic: [...]
> - Research question: [...]
> - Field: [...]
> - Theoretical lens: [...]
> - Hypothesized contribution: [...]
> - Literature scope: [language, time span, key journals]
> - Output spec: [word count, language, format]
>
> Is this accurate? Any corrections before I begin searching for literature?

**Only proceed after explicit user confirmation.**

---

## Phase 2: Literature Discovery

### Step 2.1: Seed Literature

Identify 5-8 seed papers through:
- User-provided references (always ask: "Do you already have key papers in mind?")
- WebSearch for the most-cited papers on the core topic
- lit-review-mcp tools (resolve_papers, snowball_expand) if available

**Seed selection criteria:**
- Published in high-impact journals (see Journal Tier List below)
- Highly cited in the field
- Directly relevant to the core research question

### Step 2.2: Snowball Expansion

From seeds, expand outward:
- Use citation networks (who cites these papers? who do they cite?)
- Use lit-review-mcp snowball_expand if available
- Search for recent papers (last 3-5 years) that cite the classic seeds
- Search for papers that challenge or complicate the seeds

### Step 2.3: Curation

Target: **30-50 papers** in the final corpus.

**Curation rules:**
1. **Journal quality filter**: Strongly prefer Tier 1 and Tier 2 journals (see list below). Tier 3 papers may be used as search clues but should NOT appear in the final review unless they make a unique, irreplaceable contribution.
2. **Temporal balance**: Include both foundational/classic works AND recent publications (last 5 years). A review with no papers after 2020 looks outdated; a review with no papers before 2010 looks rootless.
3. **Perspective balance**: Include papers that support, complicate, and challenge the user's framing. A review that only cites sympathetic literature is unconvincing.
4. **Relevance triage**: Every paper must serve a specific argumentative function in the review. If you can't articulate why a paper is included, cut it.

### Journal Tier List (customize per field — below is for Urban Studies / China Studies)

**Tier 1 — Must-use if relevant:**
Urban Studies, International Journal of Urban and Regional Research (IJURR), Environment and Planning A/B/C/D, Progress in Human Geography, Antipode, Annals of the Association of American Geographers, The China Quarterly, Journal of Peasant Studies, World Development

**Tier 2 — Strong sources:**
Cities, Habitat International, Urban Geography, Regional Studies, China Economic Review, Journal of Contemporary China, Development and Change, Geoforum, Political Geography, Journal of Rural Studies, Land Use Policy

**Tier 3 — Use as search clues only:**
MDPI journals (Land, Sustainability, etc.), SCIRP journals, conference proceedings, working papers, book reviews

**Books from major university presses** (Oxford, Cambridge, Chicago, Minnesota, etc.) are equivalent to Tier 1 journal articles.

### Deliverable

Present the curated corpus to the user as a structured list:

| # | Author(s) | Year | Title | Journal/Publisher | Role in review |
|---|-----------|------|-------|-------------------|----------------|

Ask the user to review, suggest additions, or flag removals before proceeding.

---

## Phase 3: Full-text Acquisition

### Step 3.1: Self-attempt

For each paper in the corpus, attempt to obtain full text through:
1. Open access URLs (check OpenAlex, Semantic Scholar)
2. Author institutional repositories
3. WebFetch / Jina on known open-access versions
4. web-access skill CDP browser mode for publisher sites (if user's browser has institutional access)

### Step 3.2: Gap Report

For papers whose full text cannot be obtained, compile a clear list for the user:

> **Papers I could not access — please help me obtain these:**
>
> 1. Wu (2018) "Planning centrality, market instruments" — Urban Studies 55(7): 1383-1399
>    DOI: 10.1177/0042098017721828
> 2. [...]
>
> Please download these PDFs and save them to [working directory]. Once available, tell me and I'll read them.

### Step 3.3: Reading & Analysis

For each acquired paper, extract:
- Section structure and headings
- Core argument (in 2-3 sentences)
- How the literature review section is organized (if present)
- Key concepts or frameworks introduced
- Empirical evidence or cases used
- How it relates to the user's research question

**Store notes** in a working file for reference during drafting.

---

## Phase 4: Exemplar Analysis

### Goal
Before writing, study how excellent literature reviews in the user's field are actually constructed.

### Process

1. Select 2-3 papers from the corpus that are published in Tier 1 journals AND contain substantial literature review sections (or are themselves review articles).
2. For each, analyze and extract:
   - **Section architecture**: How many sections? What are the headings? What's the logical flow?
   - **Argumentative strategy**: How does the author establish the research gap? Through theoretical debate? Empirical contradiction? Conceptual genealogy?
   - **Citation technique**: How are citations used — as clustered evidence for claims (parenthetical) or as descriptions of individual studies ("Scholar X argued that...")?
   - **Transition logic**: How does the author move from one section to the next? What connects them?
   - **Opening strategy**: How does the paper begin — with a puzzle? A contradiction? A bold claim?

3. Present findings to user:

> **Exemplar Analysis: What top papers in your field do**
>
> Paper A uses [strategy]...
> Paper B uses [strategy]...
>
> For your review, I recommend combining [elements] because [reasoning].

---

## Phase 5: Architecture Design

### Design Principles (derived from experience)

1. **One core question runs through the entire review.** Every section answers or advances this question.
2. **Sections represent shifts in the answer**, not shifts in chronology. Time may be a dimension, but the organizing principle is how the scholarly answer to the question has changed.
3. **The research gap emerges from the logic of the argument**, not from a claim that "nobody has studied X." A credible gap is one that the reader can see is logically necessary given the preceding analysis.
4. **The opening creates cognitive tension** — present an anomaly, a contradiction, or a puzzle that the existing literature cannot resolve. This hooks the reader and justifies the review's existence.

### Structure Template (adapt to specific case)

```
1. Opening (~10% of word count)
   - Anomaly or puzzle that motivates the review
   - Core question stated explicitly
   - Roadmap of the argument

2-N. Body sections (~70% of word count)
   - Each section: one phase/dimension of how the question has been answered
   - Within each section: thesis statement → evidence (citations as proof) → limitation/transition
   - Transitions between sections: "This framework was powerful, but it carried an implicit assumption that..."

N+1. Gap & Contribution (~20% of word count)
   - What the preceding analysis reveals is missing
   - Why this gap matters (derived from the logic, not asserted)
   - How the present study addresses it
   - Honest engagement with adjacent work that partially overlaps
```

Present the proposed architecture to the user for approval before drafting.

---

## Phase 6: Drafting

### Writing Rules

1. **No "Scholar X argued/found/demonstrated" constructions.** Instead: state a claim, then cite evidence parenthetically.
   - BAD: "Hsing (2010) argued that local governments compete for land rents."
   - GOOD: "Local governments compete fiercely to capture land rents, using construction projects to consolidate territorial authority (Hsing, 2010)."

2. **Cluster citations** when multiple sources support the same point: "(Wang et al., 2009; Liu et al., 2010; Hao et al., 2011)". Name individual scholars in the text ONLY when they introduced a distinctive concept that cannot be attributed generically.

3. **Every paragraph has a job.** It either advances the argument, provides evidence, or transitions to the next point. Paragraphs that merely describe a study without connecting it to the argument should be cut.

4. **Transitions are arguments, not connectors.** Don't write "Moving on to the next topic..." Write "This framework was powerful, but it carried an implicit assumption: that high-quality urbanization requires state direction. This assumption was thrown into relief by..."

5. **The gap section must be honest.** Acknowledge adjacent work (Hou, Smith, Chung & Unger, etc.) that partially addresses the space you're claiming. Explain precisely what remains unintegrated, not that nobody has ever looked at this.

### Process

- Write one section at a time.
- After each section, present to user for review.
- Incorporate feedback before proceeding to the next section.
- Track word count to stay within target.

---

## Phase 7: Integration & Polish

1. Combine all approved sections into a single document.
2. Check citation consistency — every parenthetical citation must appear in references; every reference must be cited in text.
3. Verify journal names, years, and volume/issue numbers against known data.
4. Compile the full reference list in the required citation style.
5. Read the complete review once more for argumentative coherence — does each section flow logically into the next?
6. Present the final integrated version to the user.

---

## Tool Usage

### Literature Search
- **WebSearch**: For discovering papers, checking journal impact, finding open-access versions
- **lit-review-mcp tools** (if available): resolve_papers, snowball_expand, run_snowball_pipeline, filter_by_topic, rank_by_importance
- **web-access skill CDP mode**: For accessing papers through the user's browser (institutional subscriptions)

### Full-text Reading
- **Read tool**: For PDFs downloaded to local workspace
- **WebFetch / Jina**: For open-access HTML versions
- **web-access skill CDP mode**: For reading papers through the user's authenticated browser sessions

### When Access Fails
**NEVER silently skip a paper you can't access.** Always report to the user:
- Which papers you could not access
- Why (paywall, 403, institutional login required)
- What the user should do (download PDF, log into university library, etc.)
- Where to save the files so you can read them

---

## Anti-patterns to Avoid

1. **Starting to search before understanding the research.** This produces a generic, unfocused literature dump.
2. **Organizing by chronology instead of argument.** Time can be a dimension within an argument, but "First scholars said X, then scholars said Y" is not an argument.
3. **Treating all papers equally.** Some papers deserve a sentence; some deserve a paragraph. Allocate space by argumentative importance, not by recency or citation count.
4. **Claiming "nobody has studied X."** Almost certainly someone has studied something adjacent. The honest move is to show what they studied, what they missed, and why the gap matters.
5. **Using small-journal papers as primary evidence.** These can help you find relevant work, but the review itself should be built on high-quality sources.
6. **Writing the review before reading exemplars.** You cannot produce publication-quality writing without first studying what publication-quality writing looks like in the specific field.
7. **Presenting a complete draft without iterative user review.** Academic writing is deeply personal — the user must shape it section by section.
