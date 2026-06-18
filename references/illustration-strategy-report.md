# Illustration Strategy Report (配图策略报告)

## Overview

Before generating images, the skill can optionally output an **Illustration Strategy Report** that explains the visual thinking behind the proposed images. This serves as both a planning document and an educational tool for content creators.

## Report Structure

### 1. Content Analysis Summary

```markdown
## Content Analysis

**Article Type**: [深度分析 / 教程 / 观点 / 故事]
**Core Argument**: [一句话总结文章核心论点]
**Target Audience**: [技术从业者 / 普通读者 / 决策者]
**Cognitive Complexity**: [高 / 中 / 低] — How abstract is the content?
```

### 2. Visual Anchor Points (视觉锚点分析)

Identify which sections benefit most from visual support:

```markdown
## Visual Anchor Points

| Section | Why Visual? | Suggested Structure | Cognitive Role |
|---------|-------------|---------------------|----------------|
| 引言：行业现状 | 建立场景感 | 概念隐喻 | **降低进入门槛** — 让读者快速进入情境 |
| 核心痛点分析 | 强化冲突感 | 前后对比 | **制造认知张力** — 问题越痛，解决方案越有价值 |
| 技术原理 | 降低理解成本 | 系统局部 | **分解复杂度** — 把抽象流程变成可触摸的物件 |
| 案例展示 | 提供可信度 | 角色状态 | **情感共鸣** — 让读者看到"像自己"的角色 |
| 结论与展望 | 留下记忆点 | 地图路线 | **强化行动意愿** — 给读者一条清晰的前进路径 |
```

### 3. Cognitive Load Distribution (认知负荷分配)

```markdown
## Cognitive Load Map

Text-Only Sections: [段落1, 段落3, 段落5] — 信息密度低，文字足够
Visual-Supported Sections: [段落2, 段落4, 段落6] — 需要图像降低认知负荷

**Principle**: Images are not decorations. They are cognitive compression — 
converting 500 words of explanation into one glanceable visual.
```

### 4. Character Strategy (角色策略)

```markdown
## Character Strategy

**Mode**: [Brand Anchor / Context Anchor]
**Character Role**: [旁观者 / 参与者 / 化身 / 隐喻]
**Character-Audience Relationship**: 
- 品牌锚定：读者认出角色 → 产生熟悉感和信任
- 情境锚定：角色即概念 → 读者通过角色理解抽象思想

**Why This Character Works**:
1. [与主题的关联逻辑]
2. [记忆点设计]
3. [情感投射点]
```

### 5. Style Justification (风格选择理由)

```markdown
## Style Selection Rationale

**Selected Style**: [风格名]
**Why This Style**:
- 与内容情绪的匹配：[理由]
- 与目标平台的匹配：[理由]
- 与品牌调性的匹配：[理由]

**Alternative Considered**: [其他风格] — 未选原因
```

### 6. Quantity & Placement Rationale (数量与位置理由)

```markdown
## Quantity & Placement

**Total Images**: [N]
**Placement Logic**:
- 平均每 [X] 字一张图 — 避免视觉疲劳
- 关键转折点必配图 — 强化认知锚点
- 开头和结尾各一张 — 建立场景 + 强化记忆
```

## Output Format

The report is output as Markdown before image generation. User can:
- Review and approve
- Request modifications
- Skip directly to generation

## User Commands

| User Says | Action |
|-----------|--------|
| "Show me the strategy first" / "先出策略" | Output strategy report before generation |
| "Why this image here?" / "为什么这里配图？" | Explain the cognitive role of a specific image |
| "Can we reduce images?" / "能减少配图吗？" | Re-analyze and propose fewer anchor points |
| "Add more visuals" / "增加配图" | Identify additional cognitive load points |
