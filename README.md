# Sloth-StratAlign-Eido

[![Version](https://img.shields.io/badge/version-0.1.0--alpha-blue)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Phase](https://img.shields.io/badge/phase-0--skeleton-orange)]()
[![Language](https://img.shields.io/badge/bilingual-ZH%20%7C%20EN-red)]()

**Enterprise Digital Transformation Strategic Alignment Engine**

> Chinese name: **同辙 · StratAlign** -- "Same Track", aligning digital initiatives with corporate strategy.

[Chinese README / 中文说明](README_zh.md)

---

## What is Sloth-StratAlign-Eido?

Sloth-StratAlign-Eido is an AI-assisted skill that guides enterprises through a structured five-module pipeline to align digital transformation investments with corporate strategy. It helps answer the fundamental question:

> "Are our IT/digital investments actually aligned with our strategic direction?"

The engine walks decision-makers through strategic decomposition, bottleneck identification, AI opportunity triage, coverage gap analysis, and investment portfolio construction -- producing a comprehensive bilingual report.

## Quick Start

1. Install as a skill in your QoderWork environment by placing the `phase-0-skeleton` directory in your skills folder.
2. Invoke the skill by asking your agent to run a digital transformation strategic alignment assessment.
3. Follow the guided dialogue through the five modules.
4. Receive your structured Markdown report.

## Architecture Overview

The engine follows a strict five-module sequential pipeline:

```
M1 Strategic Decoding    M2 Bottleneck Scan    M3 AI Triage
   (战略解码)        -->    (瓶颈扫描)      -->   (AI分诊)
                                                     |
                                                     v
M4 Coverage Analysis  <----------------------------  |
   (覆盖度分析)
        |
        v
M5 Investment Portfolio
   (投资组合)
```

### Module Details

| Module | Name | Purpose |
|--------|------|---------|
| M1 | Strategic Decoding / 战略解码 | Decompose strategy into BSC four-perspective objectives |
| M2 | Bottleneck Scan / 瓶颈扫描 | Identify operational blockers per strategic objective |
| M3 | AI Triage / AI分诊 | Score AI/digital intervention potential per bottleneck |
| M4 | Coverage Analysis / 覆盖度分析 | Map existing IT capabilities against strategic objectives |
| M5 | Investment Portfolio / 投资组合 | Allocate initiatives into Quick Wins, Core IT, and AI Bets |

### Three Iron Rules

Every recommendation is governed by three non-negotiable guardrails:

1. **Data Sovereignty First** (数据主权第一) -- Data classification before system selection
2. **Process Before Systems** (流程先于系统) -- Fix processes before buying technology
3. **Gradual Evolution** (渐进演化) -- No big-bang; always start with quick wins

## File Structure

```
phase-0-skeleton/
  SKILL.md              # Core skill definition (Anthropic format)
  report-template.md    # Bilingual report output template
  examples.md           # Manufacturing company case study
  README.md             # This file (English)
  README_zh.md          # Chinese README
  CHANGELOG.md          # Version history
  LICENSE               # MIT License
```

## Phase Roadmap

| Phase | Version | Status | Scope |
|-------|---------|--------|-------|
| **Phase 0** | v0.1.0-alpha | **Current** | Skeleton: SKILL.md, report template, case study |
| Phase 1 | v0.2.0 | Planned | Interactive dialogue refinement, multi-industry templates |
| Phase 2 | v0.3.0 | Planned | Scoring model calibration, benchmark data integration |
| Phase 3 | v0.4.0 | Planned | PDF/PPTX export, executive summary generation |
| Phase 4 | v1.0.0 | Planned | Full production release with API connectors |

## Contributing

This project is in early alpha. Contributions, feedback, and industry case studies are welcome. Please open an issue to discuss proposed changes before submitting a pull request.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

*Built with the Sloth philosophy: deliberate, thorough, strategically aligned.*
