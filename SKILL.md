---
name: sloth-stratalign-eido
version: 0.1.0-alpha
description: >
  Sloth-StratAlign-Eido ("同辙 · StratAlign") is an enterprise digital transformation
  strategic alignment engine. It guides users through a structured five-module pipeline
  to decode corporate strategy, identify operational bottlenecks, triage AI opportunities,
  analyze coverage gaps, and compose a balanced investment portfolio spanning quick wins,
  core IT modernization, and AI innovation bets.
---

# Sloth-StratAlign-Eido / 同辙 · StratAlign

## Overview / 概述

This skill implements an enterprise digital transformation strategic alignment engine.
It walks the user through five sequential analysis modules, enforces three iron rules,
and produces a structured bilingual Markdown report.

The name "同辙" (tong zhe) means "same track" -- aligning digital initiatives with
corporate strategy so they travel the same path toward shared objectives.

## Five-Module Pipeline / 五模块管线

The engine proceeds through five modules in strict order:

```
M1 Strategic Decoding    M2 Bottleneck Scan    M3 AI Triage
   战略解码          -->      瓶颈扫描      -->    AI分诊
        |                                           |
        v                                           v
M4 Coverage Analysis  <-------------------------  M3 output
   覆盖度分析
        |
        v
M5 Investment Portfolio
   投资组合
```

### M1: Strategic Decoding / 战略解码

Decompose the corporate strategy into measurable objectives using the Balanced Scorecard
(BSC) four perspectives:

1. **Financial / 财务**: Revenue, margin, cost targets
2. **Customer / 客户**: Satisfaction, retention, market share
3. **Internal Process / 内部流程**: Efficiency, quality, cycle time
4. **Learning & Growth / 学习与成长**: Talent, culture, technology capability

Ask the user to provide or confirm 2-4 strategic objectives per perspective.

### M2: Bottleneck Scan / 瓶颈扫描

For each strategic objective from M1, identify the top operational bottlenecks by asking:

- What prevents achieving this objective today?
- Where does the process break down?
- What are the data gaps or manual workarounds?

Rate each bottleneck on a 1-5 severity scale (5 = critical blocker).

### M3: AI Triage / AI分诊

For each bottleneck rated >= 3, evaluate AI/digital intervention potential:

- **Feasibility / 可行性** (1-5): Is the data available? Is the technology mature?
- **Impact / 影响力** (1-5): How much would solving this move the strategic needle?
- **Readiness / 就绪度** (1-5): Does the organization have the capability to adopt?

Compute a composite score: `AI_Score = (Feasibility + Impact + Readiness) / 3`

### M4: Coverage Analysis / 覆盖度分析

Map the current IT/digital landscape against the strategic objectives:

- Which objectives already have adequate digital support?
- Where are the critical gaps?
- Are there redundant or overlapping systems?

Produce a coverage matrix: Objectives (rows) vs. Existing Systems (columns).

### M5: Investment Portfolio / 投资组合

Allocate recommended initiatives into three investment pools:

| Pool | Chinese | Horizon | Description |
|------|---------|---------|-------------|
| Quick Wins | 止血池 | 0-6 months | Low-cost fixes that stop the bleeding |
| Core IT | 换血池 | 6-18 months | Platform modernization and integration |
| AI Bets | 造血池 | 12-36 months | Transformative AI/data-driven initiatives |

Each initiative should reference back to the bottleneck and strategic objective it addresses.

## Three Iron Rules / 三条铁律

These rules are non-negotiable guardrails applied throughout the entire pipeline:

### Iron Rule 1: Data Sovereignty First / 数据主权第一

- All data classification and ownership must be established before any system recommendation.
- No external SaaS recommendation without explicit data residency analysis.
- User must confirm data sensitivity classification for each domain.

### Iron Rule 2: Process Before Systems / 流程先于系统

- Never recommend a system to fix a broken process.
- Bottleneck analysis (M2) must identify process issues before technology triage (M3).
- If the root cause is process, prescribe process redesign first.

### Iron Rule 3: Gradual Evolution / 渐进演化

- No big-bang transformation recommendations.
- Every initiative must have an incremental rollout plan.
- Quick Wins pool must be non-empty -- always start with achievable victories.

## Dialogue Flow / 对话流程

When invoked, follow this interaction sequence:

1. **Greeting & Context Gathering**
   - Introduce the skill and its purpose.
   - Ask: "Please describe your company's industry, size, and current strategic priorities."
   - Ask: "What prompted this digital transformation assessment?"

2. **M1: Strategic Decoding**
   - Guide the user to articulate 2-4 objectives per BSC perspective.
   - Confirm the objective list before proceeding.

3. **M2: Bottleneck Scan**
   - For each objective, ask about blockers and pain points.
   - Assign severity ratings collaboratively with the user.

4. **M3: AI Triage**
   - Score each significant bottleneck on Feasibility, Impact, Readiness.
   - Present the ranked list for user validation.

5. **M4: Coverage Analysis**
   - Ask about existing IT systems and digital tools.
   - Build the coverage matrix together.

6. **M5: Investment Portfolio**
   - Propose initiative allocation across the three pools.
   - Discuss trade-offs and adjust based on user feedback.

7. **Report Generation**
   - Compile all findings into the report template.
   - Present the final report for review.

## Output Format / 输出格式

The final deliverable is a structured Markdown report following the template defined in
`report-template.md`. The report is bilingual (Chinese primary, English secondary) and
includes:

- One-line diagnosis summary
- Strategic decoding results by BSC perspective
- Bottleneck severity heatmap
- AI triage scoring table
- Coverage gap matrix
- Investment portfolio with three pools
- Recommended next steps with timeline

## Reference Files / 参考文件

- `report-template.md` -- Report output template with section structure and placeholders
- `examples.md` -- Manufacturing company case study demonstrating full pipeline execution

## Limitations / 局限性 (v0.1.0-alpha)

- This alpha version provides the structural skeleton only.
- No automated data connectors or API integrations.
- Scoring is qualitative and user-assisted, not model-driven.
- Single report format (Markdown); PDF/PPTX export planned for future phases.
- No persistent state between sessions.
