# 生成协议 (Generation Protocols)

## 通用基础（所有模式共用）

```text
Generate one standalone {aspect_ratio} article illustration.

Visual Genome:
Pure white background. Minimalist black hand-drawn line art. Slightly wobbly pen lines. Lots of empty white space. Sparse red/orange/blue handwritten Chinese annotations. Clean absurd product-sketch feeling. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Theme:
{正文配图主题}

Structure type:
{结构类型：Workflow / 系统局部 / 前后对比 / 角色状态 / 概念隐喻 / 方法分层 / 地图路线 / 小漫画分镜}

Core idea:
{这张图要表达的核心意思}

Composition:
{具体画面：角色在哪里、正在做什么、主要物件是什么、信息如何流动}

Suggested elements:
{元素1} / {元素2} / {元素3} / {元素4}

Handwritten labels (in selected language):
{标注词1} / {标注词2} / {标注词3} / {标注词4} / {可选标注词5}
Language: {zh/en/ja/ko} — All labels must be in this language

Color use (Base Sketch default):
Black for main line art and character. Orange for main flow/path/arrows. Red only for key warnings/problems/results. Blue only for secondary notes or feedback/system state.

Note: For non-Base-Sketch styles, follow the color discipline defined in the selected style (see dialect-atlas.md).

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten labels in the selected language. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. It should be clear but not instructional, interesting but not childish, strange but clean.
```

---

## 品牌锚定模式专用模板

在通用基础前增加：

```text
Recurring IP character required:
{角色名称}, {来自 brand-anchor.md 的完整角色描述}
- 外形：{颜色、形状、比例}
- 头部：{面部特征、发型、五官}
- 身体：{服装、配饰、标志性元素}
- 四肢：{手脚特征、比例}
- 表情风格：{空/呆/热血/冷峻等}
- 动态特征：{常见动作姿态}

{角色名称} must perform the core conceptual action, not decorate the scene.
Make {角色名称} serious, deadpan, and slightly bizarre, not cute.

Reference image: assets/ip-reference/ip.png
Reference strength: 0.7
```

---

## 情境锚定模式专用模板

在通用基础前增加：

```text
Character design for this illustration:
{角色名称}, {为该主题定制的角色描述}

角色生成方法：{直译法 / 异质合成法 / 认知错位法 / 随机触发法}
- 如用异质合成法：结构来源={}，质感来源={}，动作来源={}
- 如用认知错位法：错位类型={尺度/功能/时空/情感}，具体错位={}

{角色名称} must perform the core conceptual action, not decorate the scene.
Make {角色名称} strange but clean, interesting but not childish.
```

---

## 无角色模式专用模板

在通用基础前增加：

```text
No character in this illustration. The image conveys the concept purely through abstract elements, object relationships, or scene atmosphere.

Visual direction: {纯概念隐喻 / 物体叙事 / 场景氛围}
Concept expression method: {概念拆解法 / 视觉对比法 / 空间隐喻法}

Core visual metaphor:
{用 2-3 句话描述画面的核心视觉隐喻：什么元素代表什么概念，它们之间的关系是什么}

Visual focus:
{画面的视觉焦点是什么：一个形状、一个对比、一个空间关系、一个光影效果}

Atmosphere:
{画面氛围：冷峻/温暖/紧张/希望/神秘/秩序/混乱}

No human-like figures. No faces. No anthropomorphized objects with expressions or poses.
The concept must be readable from the image alone, without relying on text or character action.
```

---

## 风格变体声明（可选）

在通用基础中插入：

```text
Style variant: {变体名称}
{该变体与基础 DNA 的差异描述，1-2句话}
```

---

## 画幅比例声明

根据用户选择的画幅，在提示词中明确声明：

```text
Aspect ratio: {16:9 / 9:16 / 4:3 / 3:4 / 1:1 / 21:9}
Image size: {对应推荐尺寸}
```

---

## 图像编辑提示

### 去掉左上角标题
```text
Edit the provided image. Remove only the handwritten title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

### 增强角色核心动作
```text
Regenerate this illustration with the same core meaning and simple layout, but make the character more central to the conceptual action. The character should be doing the strange work that explains the idea, not standing beside the diagram. Keep it clean, sparse, hand-drawn, and not cute.
```

### 品牌锚定模式角色修正
```text
Regenerate this illustration with the same composition and meaning, but ensure the character matches the reference image exactly. Key features to preserve: {列出3-5个关键特征}. The character must perform the core action while maintaining these features.
```
