# Sloth-StratAlign-Eido Knowledge Hub Bridge

> 战略对齐加速器 × 中央知识库集成协议（v1.1.0）
> 仅当 EXTEND.md 中 `knowledge_hub.enabled = true` 时生效。

---

## 知识结晶点（Skill → Hub）

当以下操作完成后，AI **应当**向用户展示预填好的萃取建议卡片，经用户确认后写入中央库。

> v1.0 阶段仅激活 `priority: high` 的结晶点。`medium`/`low` 级别为 opt-in，用户可在 EXTEND.md 中配置。

| 触发条件 | 产出 asset_type | 目标 stage | priority | 萃取要素 |
|---------|----------------|-----------|----------|---------|
| 完成战略诊断报告 | `methodology` | `presales` | **high** | 诊断框架、评估维度、发现问题、建议路径 |
| 完成 AI-Native 评分 | `methodology` | `presales` | medium | 评分体系、维度权重、行业对标、差距分析 |
| 完成数字投资组合建议 | `best_practice` | `presales` | medium | 投资优先级、ROI 估算、实施路线图 |
| 完成行业 Playbook 输出 | `playbook` | `presales` | **high** | 行业特征、典型痛点、推荐方案组合、成功标准 |

### 萃取规则

> 工作流：AI 检测到结晶点 → 预填萃取卡片（含 title/summary/confidence） → 用户确认或微调 → 提交注册。用户可选择「跳过本次」但系统会在下次相同场景再次提示。

1. **战略诊断 → methodology**：
   - `title`："{客户名} 战略诊断方法论 - {行业}"
   - `summary`：诊断核心发现和建议路径
   - `industry`：从客户行业直接提取
   - `confidence`：B（单次诊断）; A（经多客户验证的诊断框架迭代）
   - `content`：诊断背景 → 使用的框架/模型 → 关键发现 → 战略建议 → 框架适用性反思
   - `applicable_skills`：`[Sloth-MfgConsult-Eido, Sloth-PSC-Eido]`

2. **AI-Native 评分 → methodology**（medium）：
   - `title`："{行业} AI-Native 成熟度评估方法论"
   - `summary`：成熟度评分结论和关键差距
   - `tags`：`[ai-native, digital-maturity, assessment]`
   - `applicable_skills`：`[Sloth-MfgConsult-Eido, Sloth-HybridDev-Eido]`

3. **投资组合 → best_practice**（medium）：
   - `title`："{客户名} 数字投资组合最佳实践"
   - `summary`：投资优先级排序和关键 ROI 论据
   - `tags`：`[investment-portfolio, digital-transformation]`

4. **行业 Playbook → playbook**：
   - `title`："{行业} 数字化转型 Playbook"
   - `summary`：行业核心痛点和推荐方案组合
   - `confidence`：B; 经多客户验证后升 A
   - `applicable_skills`：`[Sloth-MfgConsult-Eido, Sloth-DeliveryMatrix-Eido]`

---

## 知识需求点（Hub → Skill）

当用户启动以下操作时，AI **应当**先查询中央库获取相关知识推荐。

| 触发条件 | 查询维度 | 上下文信号 |
|---------|---------|----------|
| 启动战略诊断 | methodology (same industry) + case_study + lesson_learned | 客户行业、客户规模 |
| 启动 AI-Native 评估 | methodology (ai-native) + best_practice (rnd) | 客户技术栈关键词 |
| 启动投资优先级排序 | best_practice (delivery) + risk_pattern + lesson_learned | 客户行业、预算规模 |

### 推荐展示规则

> 有匹配结果时展示推荐卡片（最多 3 条），用户可选择查看详情或直接继续。无匹配则静默跳过。

1. **战略诊断**：优先推荐同行业的历史诊断方法论和交付经验教训，避免重复造轮子。
2. **AI-Native 评估**：推荐已有的评估方法论和研发侧的技术洞察。
3. **投资排序**：推荐交付实施的风险模式和最佳实践，用实施经验校准投资建议。

---

## 反馈通道

当用户在本 Skill 中引用了 Hub 推荐的知识资产后，AI 应当在任务完成时询问："这条知识对你有帮助吗？（有用 / 过时 / 有误）"，并通过 `record_feedback.py` 记录反馈，驱动知识质量自动演化。
