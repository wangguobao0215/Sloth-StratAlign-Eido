# Changelog

All notable changes to the Sloth-StratAlign-Eido project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.0-alpha] - 2026-04-17

### Added

- **Core skill definition** (`SKILL.md`) with Anthropic-standard metadata block, five-module pipeline specification, three iron rules, dialogue flow, and output format.
- **Five-module pipeline architecture**:
  - M1 Strategic Decoding (战略解码) -- BSC four-perspective decomposition
  - M2 Bottleneck Scan (瓶颈扫描) -- Severity-rated operational blocker identification
  - M3 AI Triage (AI分诊) -- Feasibility/Impact/Readiness scoring framework
  - M4 Coverage Analysis (覆盖度分析) -- IT capability vs. strategic objective mapping
  - M5 Investment Portfolio (投资组合) -- Three-pool allocation (止血池/换血池/造血池)
- **Bilingual report template** (`report-template.md`) with placeholder-driven sections for all five modules, iron rules compliance check, and next steps.
- **Manufacturing case study** (`examples.md`) -- Complete worked example for a fictional mid-size precision manufacturing company (华锐精密制造), demonstrating all five modules with realistic data.
- **Project documentation**:
  - `README.md` -- English GitHub-standard README with architecture overview and phase roadmap
  - `README_zh.md` -- Chinese README with equivalent content
  - `CHANGELOG.md` -- This file
  - `LICENSE` -- MIT License

- Note: This is the initial skeleton release (Phase 0). The skill structure is complete but no automated scoring, data connectors, or export capabilities are included.
- All content is bilingual (Chinese primary, English secondary).
- Scoring in M3 is qualitative and user-assisted; model-driven scoring is planned for Phase 2.
