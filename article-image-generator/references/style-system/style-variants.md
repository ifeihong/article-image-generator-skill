# 风格变体系统

## 概述
在基础 DNA 不变的前提下，提供 **10 种可选风格变体**，适配不同内容情绪。生成前必须提示用户选择，默认使用基础风格。

---

## 用户选择流程

### 步骤1：展示风格菜单
向用户展示 10 种风格的名称、关键词和适用场景（见下表）。

### 步骤2：用户选择
- 用户说数字（如"选3"）或风格名（如"水墨意境"）
- 或用户说"默认""基础""不选" → 使用基础风格

### 步骤3：确认并生成
- 确认用户选择
- 在提示词中注入对应风格声明
- 开始生成

---

## 10 种风格一览

| 编号 | 风格名称 | 一句话描述 | 线条特征 | 色彩特点 | 适用场景 |
|------|---------|-----------|---------|---------|---------|
| 0 | **基础手绘**（默认） | 纯白背景、黑色手绘线稿、怪诞清爽 | 细线、轻微抖动 | 黑+红橙蓝批注 | 通用、科技、商业 |
| 1 | **复古科技** | 旧工程手册、泛黄纸纹、机械制图感 | 稍粗、精确感 | 暗褐、铜绿、低饱和 | 历史、工业、怀旧 |
| 2 | **有机温暖** | 植物脉络、水彩晕染、自然生长感 | 柔软、流动性 | 植物绿、土壤棕、天空蓝 | 环保、健康、生活方式 |
| 3 | **极简几何** | 包豪斯、蒙德里安、精确网格分割 | 极细、几何感强 | 严格2-3色、大面积色块 | 数据、设计、高端理性 |
| 4 | **混合媒介** | 照片底图+手绘叠加、真实物体混搭 | 手绘线条+真实质感 | 丰富材质对比 | 教程、DIY、创意过程 |
| 5 | **水墨意境** | 东方水墨、留白意境、笔触浓淡 | 毛笔笔触、飞白、浓淡变化 | 黑灰水墨+单点朱红 | 文化、哲学、东方主题 |
| 6 | **赛博霓虹** | 霓虹光效、暗色背景、科技感线条 | 发光线条、像素感 | 荧光粉、电光蓝、霓虹紫 | 未来科技、AI、元宇宙 |
| 7 | **木刻版画** | 强烈黑白对比、刀刻纹理、民间艺术 | 粗黑线条、刀刻棱角 | 黑白为主+单色套印 | 社会议题、人文、复古宣传 |
| 8 | **黏土定格** | 3D黏土质感、手工捏制、圆润可爱 | 无线条、体积感、圆润边缘 | 柔和粉彩、哑光质感 | 教育、儿童、轻松科普 |
| 9 | **故障艺术** | 数字故障、条纹错位、数据损坏感 | 断裂线条、条纹干扰、像素错位 | 高饱和冲突色、RGB分离 | 数字批判、黑客、实验艺术 |

---

## 风格详细定义

### 0. 基础手绘（Base Hand-Drawn）— 默认
来自 `style-dna.md`：纯白背景、黑色手绘线稿、少量红橙蓝批注、大量留白、怪诞清爽。

---

### 1. 复古科技（Retro-Tech）

**视觉关键词**：旧报纸、机械制图、泛黄但不脏、打字机字体、齿轮与蒸汽

**与基础 DNA 的差异**：
- 背景：极浅的米白（#FAF8F5），允许细微纸纹
- 线条：稍粗，有机械制图的精确感，但仍保留手绘抖动
- 色彩：增加暗褐色、铜绿色，红橙蓝饱和度降低
- 质感：像从旧工程手册上撕下来的草图

**适用场景**：历史回顾、产业变迁、机械工程、怀旧感内容

**禁忌**：不要真做旧（污渍、破损、烧边）；不要复古到难以阅读

**提示词注入**：
```text
Style variant: Retro-Tech
Slightly off-white background with subtle paper texture. Lines are slightly thicker, resembling old engineering blueprints. Colors include dark brown and copper green alongside the standard red/orange/blue.
```

---

### 2. 有机温暖（Organic-Warm）

**视觉关键词**：植物脉络、水流痕迹、手绘水彩、自然生长、柔软边界

**与基础 DNA 的差异**：
- 线条：更柔软、有流动性，像藤蔓或水流
- 色彩：增加植物绿、土壤棕、天空蓝，色彩过渡更自然
- 留白：留白区域可以有极淡的有机纹理（如叶脉、水波）
- 角色：角色可以由自然元素构成

**适用场景**：自然、环保、生态、健康疗愈、生活方式、女性向

**禁忌**：不要变成儿童绘本；不要过度装饰

**提示词注入**：
```text
Style variant: Organic-Warm
Soft flowing lines like vines or water currents. Colors include plant green, soil brown, and sky blue with natural transitions. Subtle organic textures in blank areas.
```

---

### 3. 极简几何（Minimal-Geometry）

**视觉关键词**：包豪斯、蒙德里安、精确网格、几何分割、克制色彩

**与基础 DNA 的差异**：
- 线条：极细、极精确，几何感强
- 形状：圆形、方形、三角形的组合与分割
- 色彩：严格限制为 2-3 种，大面积色块
- 留白：更多，可能达到 60%-70%

**适用场景**：数据可视化、抽象概念、设计建筑、高端冷静理性内容

**禁忌**：不要变成 PPT 图表；不要过度分割导致信息碎片化

**提示词注入**：
```text
Style variant: Minimal-Geometry
Ultra-thin precise lines with strong geometric feel. Shapes are combinations of circles, squares, and triangles. Strictly limited to 2-3 colors with large color blocks. 60-70% white space.
```

---

### 4. 混合媒介（Mixed-Media）

**视觉关键词**：照片+手绘叠加、真实物体+涂鸦、拼贴感、层次丰富

**与基础 DNA 的差异**：
- 底图：可以是真实照片（如桌面、纸张、布料）
- 手绘：在照片上用线条勾画、标注、涂鸦
- 元素：真实物体（如剪刀、胶带、回形针）与手绘元素混搭
- 质感：更丰富的材质对比

**适用场景**：创意过程、设计思路、教程、DIY、手工主题

**禁忌**：不要变成杂乱拼贴；真实元素与手绘元素要有逻辑关联

**提示词注入**：
```text
Style variant: Mixed-Media
Real photograph as background (desk, paper, fabric texture). Hand-drawn lines and doodles overlaid on photo. Real objects (scissors, tape, paper clips) mixed with drawn elements.
```

---

### 5. 水墨意境（Ink-Wash Zen）

**视觉关键词**：东方水墨、留白意境、笔触浓淡、山水气韵、禅意

**与基础 DNA 的差异**：
- 背景：宣纸质感，米白色，允许水墨晕染
- 线条：毛笔笔触，有飞白、浓淡干湿变化，粗细不一
- 色彩：以黑灰水墨为主，仅保留一处朱红或赭石作为点睛
- 质感：水墨在纸上晕染的自然效果，边缘模糊
- 留白：更多留白，讲究"计白当黑"的意境

**适用场景**：中国文化、哲学思辨、东方美学、历史人文、茶道禅意

**禁忌**：不要变成日式浮世绘；不要过度渲染失去简洁；不要用西方透视

**提示词注入**：
```text
Style variant: Ink-Wash Zen
Rice paper texture background with ink wash bleeding effects. Brush strokes with dry brush texture and ink gradation. Primarily black and gray ink with a single touch of vermillion. Emphasize negative space and Zen atmosphere.
```

---

### 6. 赛博霓虹（Cyber-Neon）

**视觉关键词**：霓虹光效、暗色背景、科技感线条、像素、全息

**与基础 DNA 的差异**：
- 背景：深色（深灰或近黑），而非纯白
- 线条：发光线条，有霓虹灯管效果，可能带像素感
- 色彩：荧光粉、电光蓝、霓虹紫、激光绿，高饱和
- 质感：光晕、扫描线、数字网格、全息投影感
- 留白：深色背景上的"暗留白"，而非白底

**适用场景**：未来科技、AI、元宇宙、虚拟现实、数字文化、游戏

**禁忌**：不要变成夜店风；不要过度炫光导致信息淹没；不要丢失手绘感

**提示词注入**：
```text
Style variant: Cyber-Neon
Dark gray or near-black background. Glowing neon lines with light bloom effects. Colors are fluorescent pink, electric blue, neon purple, laser green. Include subtle scan lines and digital grid. Hand-drawn feel with tech aesthetic.
```

---

### 7. 木刻版画（Woodcut Print）

**视觉关键词**：强烈黑白对比、刀刻纹理、民间艺术、宣传画、粗犷有力

**与基础 DNA 的差异**：
- 背景：纯白或单色底
- 线条：粗黑线条，有刀刻的棱角和力度，无渐变
- 色彩：黑白为主，最多加一种套印色（如大红、土黄）
- 质感：木刻刀痕纹理，黑白交界锐利
- 形状：概括性强，不追求细节，追求力量感

**适用场景**：社会议题、人文关怀、复古宣传、乡土文化、力量感表达

**禁忌**：不要变成漫画；不要过度细腻；不要多色混杂

**提示词注入**：
```text
Style variant: Woodcut Print
Bold black lines with knife-cut texture and sharp edges. High contrast black and white with at most one additional block-print color. Wood grain texture visible. Strong graphic summary style, not detailed.
```

---

### 8. 黏土定格（Clay Stop-Motion）

**视觉关键词**：3D黏土质感、手工捏制、圆润可爱、哑光、指纹痕迹

**与基础 DNA 的差异**：
- 无线条：不用线条勾勒，用体积和光影表现
- 形状：圆润、饱满、有机形态，有手工捏制的不规则感
- 色彩：柔和粉彩、马卡龙色系、哑光质感
- 质感：黏土表面纹理，可能有细微指纹痕迹
- 光影：柔和漫射光，小范围投影

**适用场景**：教育、儿童内容、轻松科普、治愈系、手工主题

**禁忌**：不要变成光滑3D渲染；不要过度写实；保持手工感

**提示词注入**：
```text
Style variant: Clay Stop-Motion
No outline lines. Forms are rounded, volumetric, hand-sculpted clay with subtle fingerprint textures. Soft pastel colors with matte finish. Gentle diffused lighting with soft shadows. Handmade irregular charm.
```

---

### 9. 故障艺术（Glitch Art）

**视觉关键词**：数字故障、条纹错位、数据损坏、RGB分离、扫描干扰

**与基础 DNA 的差异**：
- 线条：断裂、错位、重复的线条，有数字损坏感
- 色彩：RGB通道分离、色彩条纹、高饱和冲突色
- 质感：扫描线、像素块、数据压缩 artifacts
- 构图：元素可能重复、错位、撕裂，但核心信息可读
- 整体：像一张被数字损坏后又修复的图片

**适用场景**：数字批判、黑客文化、实验艺术、后互联网、数据隐私

**禁忌**：不要变成无法阅读的乱码；故障要可控、有美感；不要过度干扰核心信息

**提示词注入**：
```text
Style variant: Glitch Art
Lines are broken, duplicated, and offset with digital corruption feel. RGB channel separation and color stripe artifacts. Subtle scan lines and pixel blocks. Core image remains readable despite controlled glitches.
```

---

## 风格选择速查表

| 用户说 | 对应风格 |
|--------|---------|
| "默认""基础""不选""手绘" | 0. 基础手绘 |
| "复古""旧时光""工业""怀旧" | 1. 复古科技 |
| "自然""温暖""柔和""有机""水彩" | 2. 有机温暖 |
| "极简""几何""冷静""理性""包豪斯" | 3. 极简几何 |
| "真实""照片""拼贴""混搭""手工" | 4. 混合媒介 |
| "水墨""东方""禅意""中国风""意境" | 5. 水墨意境 |
| "赛博""霓虹""科技""未来""AI感" | 6. 赛博霓虹 |
| "木刻""版画""黑白""粗犷""力量" | 7. 木刻版画 |
| "黏土""3D""可爱""教育""儿童" | 8. 黏土定格 |
| "故障"" glitch""实验""数字""黑客" | 9. 故障艺术 |

---

## 风格选择界面模板

向用户展示时使用：

```
请选择配图风格（输入数字或风格名）：

【0】基础手绘 — 纯白背景，黑色手绘线稿，怪诞清爽（默认）
【1】复古科技 — 泛黄工程手册，机械制图感
【2】有机温暖 — 植物脉络，水彩晕染，自然生长
【3】极简几何 — 包豪斯网格，精确分割，克制色彩
【4】混合媒介 — 照片+手绘，真实物体混搭
【5】水墨意境 — 东方水墨，留白意境，笔触浓淡
【6】赛博霓虹 — 霓虹光效，暗色背景，科技感
【7】木刻版画 — 强烈黑白，刀刻纹理，民间艺术
【8】黏土定格 — 3D黏土，手工捏制，圆润可爱
【9】故障艺术 — 数字故障，条纹错位，数据损坏感

直接回复数字（如"3"）或风格名即可。
```
