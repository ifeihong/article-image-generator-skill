# 固定IP模式 — 角色锁定规范

## 概述
固定IP模式使用用户提供的角色三视图/参考图，确保每张配图中的角色形象高度一致。适合需要品牌统一性、系列感的内容生产。

## 参考图存放位置
```
assets/ip-reference/
├── ip.png                 ← 主参考图（三视图或完整形象）
├── character-front.png    ← 正面（可选，辅助）
├── character-side.png     ← 侧面（可选，辅助）
└── character-back.png     ← 背面（可选，辅助）
```

**替换规则**：用户只需覆盖 `ip.png` 文件，即可替换角色形象。支持 PNG/JPG/WebP 格式。

## 参考图使用规范

### 生图时必传参数
```
reference_image: assets/ip-reference/ip.png
reference_strength: 0.7
```

- **reference_strength 0.6-0.8**：推荐值 0.7
  - 0.6：角色特征较松，创作空间大
  - 0.7：平衡一致性与创作空间（推荐）
  - 0.8：高度一致，几乎完全复刻参考图

**Note**: The current Codex/Trae GenerateImage tool does not support a `reference_image` parameter. When the underlying tool supports it, use `reference_image` + `reference_strength`. Until then, achieve consistency through enhanced text descriptions + session context (see SKILL.md Technical Notes).

### 提示词中的角色描述块
即使传入参考图，提示词中仍需包含完整的角色文字描述，作为**双重保险**：

```text
Recurring IP character required:
[角色名称], [来自参考图的完整描述]
- 外形：[颜色、形状、比例]
- 头部：[面部特征、发型、五官]
- 身体：[服装、配饰、标志性元素]
- 四肢：[手脚特征、比例]
- 表情风格：[空/呆/热血/冷峻等]
- 动态特征：[常见动作姿态]

[角色名称] must perform the core conceptual action, not decorate the scene.
Make [角色名称] serious, deadpan, and slightly bizarre, not cute.
```

## 角色描述提取模板

当用户上传三视图后，按以下维度提取并固化描述：

```markdown
## [角色名称]

### 基础信息
- 名称：
- 物种/类型：
- 主色调：
- 身高比例：

### 头部特征
- 脸型：
- 眼睛：
- 嘴巴：
- 特殊装饰：

### 身体特征
- 体型：
- 服装：
- 标志性配饰（必须出现）：
- 标志性图案/纹理：

### 四肢特征
- 手臂：
- 腿部：
- 手脚：

### 表情库
- 默认表情：
- 认真时：
- 困惑时：
- 兴奋时：

### 动作特征
- 走路姿态：
- 常用手势：
- 标志性姿势：

### 绝对不变项
生成时必须检查，以下元素不能改变或省略：
- [ ] 特征A
- [ ] 特征B
- [ ] 特征C
```

## 一致性保障机制

### 生成前检查
- [ ] 参考图文件是否存在？
- [ ] reference_image 参数是否传入？
- [ ] 提示词中是否包含角色描述块？

### 生成后检查
- [ ] 角色颜色是否与参考图一致？
- [ ] 标志性特征是否出现？
- [ ] 比例是否符合三视图？
- [ ] 角色是否承担核心动作（而非只是站着）？

### 走样处理
如果生成的角色与参考图不一致：
1. 提高 reference_strength 到 0.8
2. 在提示词中强化角色描述的关键词
3. 如仍不一致，用局部重绘修正角色部分

## 使用示例

用户上传了一只蓝色机械猫的三视图：

```text
参考图路径：assets/ip-reference/ip.png
reference_strength: 0.7

角色描述：
蓝仔，一只蓝白相间的机械猫，约2.5头身。
头部圆形，有一只发光的右眼（机械义眼），左耳缺一角。
身体穿银色工装背心，背心上有一个齿轮标志（必须出现）。
四肢是机械关节，爪子有三根金属指。
表情空、呆、认真，不卖萌。
尾巴是数据线形状，末端有USB接口。

蓝仔 must perform the core conceptual action, not decorate the scene.
```

## 注意事项
- 参考图质量直接影响生成一致性，建议提供清晰、完整、白底的角色图
- 过于复杂的角色（多配件、多颜色）一致性难度更高
- 角色在每张图中的姿态可以不同，但核心特征必须保持一致
