# 质量关卡 (Quality Gates)

## 生成后检查清单

### 通用检查（所有模式）

- [ ] **画幅一致性**：所有图片是否使用相同的画幅比例？
- [ ] **角色核心动作**：角色是否承担核心动作（而非只是装饰）？
- [ ] **画面拥挤度**：主体是否占画面 40%-60%，留白是否充足？
- [ ] **PPT/流程图感**：是否太像 PPT、流程图或课程课件？
- [ ] **文字质量**：标注是否少、短、能读？有无严重错别字？（检查语言是否正确）
- [ ] **标题陷阱**：左上角是否出现"Workflow / 系统架构图 / 常见坑"等类型标题？
- [ ] **风格偏差**：风格是否太可爱、幼稚、死板或过于精致？
- [ ] **背景纯净度**：背景是否为纯白（基础素描）或符合所选风格？
- [ ] **风格统一性**：同一文章的所有图片风格是否一致？
- [ ] **画幅正确性**：图片比例是否与用户选择的一致？

### 品牌锚定模式额外检查

- [ ] **角色一致性**：角色是否与参考图一致？
- [ ] **特征完整性**：标志性特征（颜色、配饰、比例）是否出现？
- [ ] **reference_strength**：是否需要调整（走样时提高到 0.8）？

### 情境锚定模式额外检查

- [ ] **角色统一性**：同一文章的所有图片是否使用同一角色？
- [ ] **概念关联度**：角色是否与文章主题有关联？
- [ ] **记忆点**：角色是否有至少一个让人记住的特征？

---

## 迭代方法

### 问题分类与修复策略

| 问题类型 | 修复方法 |
|---------|---------|
| 角色只是装饰 | 重写提示词，让角色"做"核心动作 |
| 画面太满 | 减少元素数量，增加留白区域 |
| 像 PPT/流程图 | 加入怪诞元素，打破规整感；减少文字 |
| 风格不统一 | 检查是否所有图片都注入了相同的风格声明 |
| 画幅错误 | 重新生成，明确声明正确的 aspect ratio |
| 角色走样（品牌锚定） | 提高 reference_strength 到 0.8，强化关键词 |
| 标注错误（语言/内容） | 减少标注数量，缩短每个标注，检查语言设置 |
| 背景不纯 | 明确声明 "pure white background" |

### 迭代提示词模板

**减少拥挤**：
```text
Regenerate with the same core idea but much simpler. Remove {具体元素}. Increase blank white space to at least 40% of the canvas. Keep only the character and 2-3 key objects.
```

**增强怪诞感**：
```text
Regenerate with the same structure but make it stranger and more unexpected. Add one absurd element that doesn't belong but makes the concept clearer. Keep the hand-drawn sketch feeling.
```

**修正画幅**：
```text
Regenerate with the exact same content but change the aspect ratio to {16:9/9:16/4:3/3:4/1:1/21:9}. Preserve all elements, composition, and style exactly.
```

**统一风格**：
```text
Regenerate to match the style of the previous image exactly. Use the same line weight, color palette, annotation style, and overall aesthetic. The only change should be the content/theme.
```
