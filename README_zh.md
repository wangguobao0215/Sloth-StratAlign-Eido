# 同辙 · StratAlign (Sloth-StratAlign-Eido)

[![版本](https://img.shields.io/badge/版本-0.1.0--alpha-blue)](CHANGELOG.md)
[![许可证](https://img.shields.io/badge/许可证-MIT-green)](LICENSE)
[![阶段](https://img.shields.io/badge/阶段-Phase%200%20骨架-orange)]()
[![双语](https://img.shields.io/badge/双语-中文%20%7C%20英文-red)]()

**企业数字化转型战略对齐引擎**

> "同辙"意为"同一轨道"——让数字化举措与企业战略行驶在同一条轨道上。

[English README / 英文说明](README.md)

---

## 什么是同辙 · StratAlign？

同辙 · StratAlign 是一个AI辅助的技能引擎，通过结构化的五模块管线引导企业实现数字化转型投资与企业战略的对齐。它帮助回答一个根本性问题：

> "我们在IT/数字化上的投资，真的对准了战略方向吗？"

引擎引导决策者完成战略分解、瓶颈识别、AI机会分诊、覆盖度分析和投资组合构建，最终产出一份结构化的双语报告。

## 快速开始

1. 将 `phase-0-skeleton` 目录放入您的 QoderWork 技能目录中完成安装。
2. 让您的智能体执行"数字化转型战略对齐评估"来调用本技能。
3. 按照引导对话完成五个模块的分析。
4. 获取结构化的 Markdown 报告。

## 架构概览

引擎遵循严格的五模块顺序管线：

```
M1 战略解码       M2 瓶颈扫描       M3 AI分诊
(Strategic    --> (Bottleneck  -->  (AI
 Decoding)        Scan)             Triage)
                                      |
                                      v
M4 覆盖度分析 <-------------------------
(Coverage Analysis)
        |
        v
M5 投资组合
(Investment Portfolio)
```

### 模块详情

| 模块 | 名称 | 用途 |
|------|------|------|
| M1 | 战略解码 | 基于平衡计分卡四维度分解企业战略目标 |
| M2 | 瓶颈扫描 | 针对每个战略目标识别运营瓶颈 |
| M3 | AI分诊 | 评估每个瓶颈的AI/数字化干预潜力 |
| M4 | 覆盖度分析 | 将现有IT能力映射到战略目标 |
| M5 | 投资组合 | 将举措分配至止血池、换血池和造血池 |

### 三条铁律

所有建议均受三条不可违背的铁律约束：

1. **数据主权第一** — 先完成数据分类，再选型系统
2. **流程先于系统** — 先修复流程问题，再采购技术
3. **渐进演化** — 拒绝大爆炸式转型，必须从快速见效开始

## 文件结构

```
phase-0-skeleton/
  SKILL.md              # 核心技能定义文件（Anthropic格式）
  report-template.md    # 双语报告输出模板
  examples.md           # 制造业企业案例研究
  README.md             # 英文说明
  README_zh.md          # 中文说明（本文件）
  CHANGELOG.md          # 版本变更记录
  LICENSE               # MIT 许可证
```

## 阶段路线图

| 阶段 | 版本 | 状态 | 范围 |
|------|------|------|------|
| **Phase 0** | v0.1.0-alpha | **当前** | 骨架：SKILL.md、报告模板、案例研究 |
| Phase 1 | v0.2.0 | 计划中 | 交互对话优化、多行业模板 |
| Phase 2 | v0.3.0 | 计划中 | 评分模型校准、行业基准数据集成 |
| Phase 3 | v0.4.0 | 计划中 | PDF/PPTX导出、高管摘要生成 |
| Phase 4 | v1.0.0 | 计划中 | 正式生产版本，含API连接器 |

## 参与贡献

本项目处于早期Alpha阶段。欢迎贡献代码、提供反馈和行业案例。请先通过Issue讨论拟议的变更，再提交Pull Request。

## 许可证

本项目采用 MIT 许可证。详见 [LICENSE](LICENSE)。

---

*秉承"树懒"哲学：审慎、周全、战略对齐。*
