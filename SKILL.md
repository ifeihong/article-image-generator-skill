---
name: article-image-generator
description: AI-powered article illustration generator for Codex, Trae, and Claude Code. Creates illustrations with configurable aspect ratios (16:9, 9:16, 4:3, 3:4, 1:1, 21:9) and quantity (1-9 images). Features dual Character Anchor Modes (Brand Anchor with fixed character reference or Context Anchor with custom per-article character), 10 Visual Styles plus Hybrid Style experiments, multi-language annotation support (auto-detect or manual), Quick/Expert dual workflow modes, session history reuse, series character continuity, and illustration strategy reports. Generates creative, hand-drawn style illustrations for blog posts, reports, and social media content with consistent character branding and visual storytelling.
keywords: AI image generator, article illustration, Codex skill, Trae skill, Claude Code skill, content creation, 16:9 illustration, 9:16 illustration, character consistency, visual style, GPT Image 2, blog illustration generator, WeChat article images, visual storytelling, content branding, aspect ratio configurable, multi-language, quick mode, expert mode, style mixing, series character
---

# Article Image Generator

## Core Positioning

Transform written content into compelling illustrations with configurable aspect ratios and quantity. Convert key judgments, workflows, structures, states, or metaphors from articles into clean, absurd, creative, readable — yet non-instructional — hand-drawn explanatory visuals.

Supports two Character Anchor Modes:
- **Brand Anchor Mode**: Uses a user-provided character reference image. The same figure appears in every illustration, ideal for brand consistency and visual identity
- **Context Anchor Mode**: Generates a bespoke character tailored to each article's theme. **All illustrations within one article use the same character**, maximizing content-native creativity and conceptual depth

Configurable output:
- **Aspect Ratio**: 16:9 (default), 9:16, 4:3, 3:4, 1:1, 21:9
- **Quantity**: 1-9 images per article (smart recommendation based on content length)
- **Language**: Auto-detect from article text, or manually select (Chinese / English / Japanese / Korean)
- **Workflow Mode**: Quick Mode (1-step) or Expert Mode (full 10-step pipeline, Step 0-9)
- **Style**: 10 base styles + Hybrid Style mixing experiments

## Dual Workflow Modes

### Quick Mode
For users who want results fast. One-step invocation:

```
User: "Generate illustrations for this article"
→ Skill auto-detects all parameters
→ Generates images immediately
```

**Quick Mode Auto-Detection**:
- Language: Detect from article text (Chinese characters → zh, English → en, Hiragana/Katakana → ja, Hangul → ko)
- Aspect Ratio: Default 16:9 (or detect from platform keywords like "小红书" → 9:16)
- Quantity: Auto-recommend based on article length
- Style: Base Sketch (default)
- Mode: Context Anchor (default, unless reference image exists)

**Quick Mode Override**: User can still specify any parameter inline:
- "Generate with 9:16, Cyber-Neon style, 4 images" → Quick mode with overrides

### Expert Mode
Full 10-step pipeline (Step 0-9) with granular control. Activated when user says:
- "Expert mode" / "专业模式"
- "I want full control" / "我要完整控制"
- Or when user explicitly selects parameters one by one
- **First-time users**: Automatically enters Guided Expert Mode (see below)

### First-Time User Onboarding
When `output/session-history.json` does NOT exist, the skill automatically enters **Guided Expert Mode** — a step-by-step walkthrough that explains each parameter before proceeding. See `references/onboarding-guide.md` for the complete guided flow.

Skip commands:
- "skip guide" / "跳过引导" → Enter normal Expert Mode
- "don't show this again" / "不再显示" → Create history file, never show guide again
- "quick mode" / "快速模式" → Enter Quick Mode immediately

## Dual Anchor System

### Mode Selection Rules

| Trigger Condition | Mode Used |
|------------------|-----------|
| User explicitly says "use my character" / "brand mode" / "fixed character" | Brand Anchor Mode |
| Character reference image exists in `assets/ip-reference/` | Default to Brand Anchor Mode |
| User says "context mode" / "custom character" / "free form" / "max creativity" | Context Anchor Mode |
| User says "no character" / "pure concept" / "abstract only" / "no IP" / "无角色" / "纯画面" | No-Character Mode |
| No reference image and user unspecified | Context Anchor Mode (default) |
| User says "use my series character [name]" | Series Character Mode (see below) |

### Mode Switching Commands
- "Switch to Brand Anchor mode" → Check `assets/ip-reference/` for reference image; switch if exists, prompt for upload if not
- "Switch to Context Anchor mode" → Switch directly
- "Switch to No-Character mode" / "Use pure concept mode" → Switch directly
- "Use Brand Anchor this time, Context Anchor next time" → Execute as single-task override without changing default
- "Use my [series name] character" → Load series character from `session-history.json`

## Multi-Language Annotation Support

### Auto-Detection (Default)
The skill automatically detects the article's language and generates annotations in the same language:

| Detected Language | Annotation Language | Typography Style |
|-------------------|---------------------|------------------|
| Chinese (中文) | Simplified Chinese | Horizontal, 2-8 characters, handwritten |
| English | English | Horizontal, 1-3 words, handwritten |
| Japanese (日本語) | Japanese (Kanji/Hiragana) | Horizontal or vertical, brief phrases |
| Korean (한국어) | Korean | Horizontal, short phrases |

**Detection Method**: Analyze the article text. If >50% characters are Chinese → zh; >50% Hangul → ko; >50% Hiragana/Katakana → ja; otherwise → en.

### Manual Selection
User can override auto-detection:
- "Generate with English annotations" / "用英文标注"
- "Use Japanese labels" / "日本語のラベル"
- "Labels in Korean" / "한국어 라벨"

### Annotation Guidelines per Language

**Chinese**: Sparse red/orange/blue handwritten annotations. Max 5-8 instances, 2-8 characters each.
**English**: Sparse handwritten labels. Max 5-8 instances, 1-3 words each. Use uppercase for emphasis sparingly.
**Japanese**: 手書き風ラベル。最大5-8個、各2-6文字。漢字とひらがな混在可。
**Korean**: 손글씨 스타일 라벨. 최대 5-8개, 각 2-6자. 받침 있는 글자는 명확하게.

## Reference Documents

Read on-demand based on task requirements; do not load everything at once:

### Universal References (both modes)
- `references/visual-genome/base-genome.md`: Visual DNA, aspect ratio specifications, color discipline, typography, prohibitions
- `references/visual-genome/dialect-atlas.md`: 10 Visual Style definitions and prompt-injection templates
- `references/concept-forge/heterogeneous-synthesis.md`: Cross-domain synthesis matrix for character design
- `references/concept-forge/cognitive-displacement.md`: Four types of deliberate misalignment for creative visuals
- `references/narrative-structures.md`: 8 narrative composition patterns
- `references/generation-protocols.md`: Generation prompt templates for both modes, all styles, and all aspect ratios
- `references/quality-gates.md`: Post-generation quality checklist and iteration methods
- `references/session-history.md`: Session history format, reuse commands, user defaults
- `references/illustration-strategy-report.md`: Strategy report structure and cognitive analysis framework
- `references/series-character-continuity.md`: Series character save/reuse workflow
- `references/onboarding-guide.md`: First-time user guided walkthrough
- `references/error-handling.md`: Error scenarios and recovery strategies
- `references/platform-detection.md`: Platform keyword detection rules for Quick Mode auto-ratio

### Mode-Specific References
- **Brand Anchor Mode**: `references/character-anchors/brand-anchor.md` — Character locking specification, reference image usage rules, character description template
- **Context Anchor Mode**: `references/character-anchors/context-anchor.md` — Character generation rules, type library, design methodologies, mandatory user confirmation workflow
- **No-Character Mode**: `references/character-anchors/no-character.md` — Pure concept generation without any character/IP, three visual directions (abstract metaphor / object narrative / scene atmosphere), concept expression methods

## Workflow

### Step 0: Workflow Mode Selection (Optional)
If user does not specify mode, default to Quick Mode for speed.
If user says "expert mode" / "full control", switch to Expert Mode.

### Step 1: Mode Confirmation
Determine which mode to use:
- Check if image files exist in `assets/ip-reference/`
- Check if user requests a series character (`session-history.json`)
- Check if user requests No-Character mode ("no character" / "pure concept" / "无角色")
- Ask user preference if not explicitly stated
- Read the corresponding mode reference document after confirmation

### Step 2: Language Selection (Expert Mode) / Auto-Detect (Quick Mode)
**Expert Mode**: Present language options:
```
Please select annotation language (or press Enter for auto-detect):
[1] Auto-detect (default) — Detect from article text
[2] Chinese (中文)
[3] English
[4] Japanese (日本語)
[5] Korean (한국어)
```

**Quick Mode**: Auto-detect and proceed silently.

### Step 3: Aspect Ratio Selection
**Before digesting content, the user MUST select an aspect ratio.**

Present the aspect ratio menu with smart recommendation:
```
Please select an aspect ratio (enter number or ratio, press Enter for recommendation):

[Recommended] Based on your content type, suggested: 16:9 horizontal (article illustration)

Available ratios:
[1] 16:9 horizontal — Article body, blog posts, video covers (default)
[2] 9:16 vertical — Xiaohongshu, Douyin, phone wallpapers, short videos
[3] 4:3 horizontal — PPT, course slides, reports, presentations
[4] 3:4 vertical — Xiaohongshu graphics, Instagram, social media
[5] 1:1 square — Avatars, social media, product shots, square posters
[6] 21:9 ultra-wide — Banners, website covers, Bilibili headers, widescreen

Reply with a number (e.g., "2") or ratio (e.g., "9:16"). Press Enter for recommended value.
```

- Confirm user selection
- Lock the aspect ratio for all images in this article (cannot be changed mid-task)
- User says "default" / "standard" / "no preference" → Use [1] 16:9

**Smart Recommendation Logic**:
- Detected WeChat Official Account / blog / report content → Recommend 16:9
- Detected Xiaohongshu / Douyin / short video content → Recommend 9:16 or 3:4
- Detected PPT / courseware / presentation content → Recommend 4:3
- Detected social media / avatar content → Recommend 1:1
- No specific platform detected → Recommend 16:9 (default)

### Step 4: Quantity Confirmation
**Before digesting content, confirm the number of illustrations.**

Present quantity recommendation:
```
Please enter the number of illustrations (1-9, press Enter for recommendation):

[Recommended] Based on article length, suggested: 6 illustrations

Range: 1-9 images
- Short article (<1000 words): 1-3 images
- Medium article (1000-3000 words): 4-6 images
- Long article (>3000 words): 7-9 images

Reply with a number. Press Enter for recommended value.
```

- Confirm user selection
- Default: 4-6 images for medium-length articles
- Short articles: 1-3 images
- Long articles: 7-9 images
- User says "default" / "standard" / "no preference" → Use recommended value

### Step 5: Style Selection
**Before digesting content, the user MUST select a Visual Style.**

Present the style menu:
```
Please select a Visual Style (enter number or style name):

[0] Base Sketch — White canvas, black hand-drawn lines, absurd clarity (default)
[1] Retro-Tech — Yellowed engineering manual, mechanical drafting aesthetic
[2] Organic Warmth — Plant veins, watercolor bleeding, natural growth
[3] Minimal Geometry — Bauhaus grids, precise divisions, restrained color
[4] Mixed Media — Photo base + hand-drawn overlays, real object mashups
[5] Ink-Wash Zen — Eastern ink painting, negative space mastery, brush gradation
[6] Cyber-Neon — Glowing neon lines, dark backgrounds, tech luminescence
[7] Woodcut Print — Bold black-white contrast, knife-cut texture, folk art
[8] Clay Stop-Motion — 3D clay texture, hand-sculpted, rounded and charming
[9] Glitch Art — Digital corruption, stripe displacement, data decay aesthetics

[H] Hybrid Mode — Mix two styles for unique combinations (Expert Mode only)

Reply with a number (e.g., "3") or style name.
```

- Confirm user selection
- Inject corresponding style declaration into all subsequent prompts
- User says "default" / "base" / "no preference" → Use [0] Base Sketch

**Style Preview**: Preview images for each style are available in `assets/style-previews/`. When the user asks "show me the styles" / "看看风格效果", display or describe the preview images to help them choose.

**Hybrid Style Mixing (Optional within Step 5)**
If user selects [H] Hybrid Mode:
```
Hybrid Style Mode — Select two styles to mix:

Primary Style (dominant, 60-70% influence):
[0-9] Select base style

Secondary Style (accent, 30-40% influence):
[0-9] Select accent style

Mix examples:
- Ink-Wash Zen [5] + Cyber-Neon [6] = "Neon ink painting" — traditional brush strokes with glowing neon accents
- Clay Stop-Motion [8] + Glitch Art [9] = "Corrupted clay" — handmade clay forms with digital artifacts
- Retro-Tech [1] + Organic Warmth [2] = "Bio-mechanical vintage" — old machinery with plant overgrowth
```

**Hybrid Style Prompt Injection**:
```text
Style: Hybrid — {Primary Style} dominant + {Secondary Style} accent
{Primary style injection at 60-70% strength}
{Secondary style injection at 30-40% strength, applied selectively}
Fusion principle: {describe how the two styles interact}
```

### Step 6: Content Digestion
Read the user's article text, links, Markdown, Notion, or screenshots. Extract:
- What is the core argument?
- Which paragraphs carry cognitive turning points?
- Which content benefits from visual explanation?
- Which sections are text-only and do not need images?

Do not distribute images evenly. Prioritize "cognitive anchors": core judgments, breakpoints, closed loops, divergences, before/after contrasts, continuation paths, character state changes.

**Illustration Strategy Report (Optional within Step 6)**
If user says "show strategy first" / "先出策略":
- Output strategy report using `references/illustration-strategy-report.md`
- Include: content analysis, visual anchor points, cognitive load map, character strategy, style justification, quantity rationale
- Wait for user approval before proceeding to Visual Script

### Step 7: Visual Script (Shot List)
If the user says "analyze illustration strategy" / "analyze" / "show me the plan", output a Visual Script first. For each image, specify:
- Placement: after which paragraph
- Theme: what the image is about
- Core idea: what concept it communicates
- Narrative structure type
- Character action (Brand Anchor) / Character design direction (Context Anchor)
- Suggested elements
- Suggested annotation keywords (in selected language)

Quantity must match the user-confirmed number from Step 4.

**Context Anchor Mode Additional Step:**
Before outputting the Visual Script, **MUST confirm character design direction with the user**:
1. Based on article theme, provide 2-3 character concepts (each including: character name, visual description, personality traits, thematic connection logic)
2. Explain the generation method for each concept (Direct Translation / Heterogeneous Synthesis / Cognitive Displacement / Random Trigger)
3. Wait for user selection or modification suggestions
4. After user confirmation, output the Visual Script and begin generation

**Prohibited**: Generating characters and images without user confirmation

### Step 8: Single Image Generation
If the user explicitly requests "generate," do not stop for confirmation; generate each image individually.

**Brand Anchor Mode Generation Parameters:**
```
- Prompt: Must include complete character description (from brand-anchor.md)
- Reference image: Pass character image from assets/ip-reference/
- Reference strength: 0.6-0.8 (high consistency, preserving creative space)
- Character must perform the core conceptual action in every image
- Style declaration: Inject user-selected style (see dialect-atlas.md)
- Aspect ratio: Inject user-selected ratio (see base-genome.md)
- Language: Use selected annotation language
```

**Context Anchor Mode Generation Parameters:**
```
- Prompt: Include character description customized for the theme (same character description for all images in one article)
- No reference image: Pure text-driven
- All illustrations in one article MUST use the same character; character appearance must be consistent
- Character actions and poses may vary per image, but core appearance, material, and signature features must remain consistent
- Encourage cross-domain synthesis and cognitive displacement metaphors
- Style declaration: Inject user-selected style (see dialect-atlas.md)
- Aspect ratio: Inject user-selected ratio (see base-genome.md)
- Language: Use selected annotation language
```

Every image prompt must include:
- Aspect ratio declaration (from base-genome.md)
- Style declaration (from dialect-atlas.md, or hybrid declaration)
- Language declaration for annotations
- Black hand-drawn lines (Base Sketch) or corresponding style line definition
- Sparse handwritten annotations in selected language (adjusted per style)
- Generous negative space (adjusted per style and aspect ratio)
- Character as the core action subject
- Prohibition: PPT, commercial illustration, childish/cute, complex architecture, top-left corner type titles

### Step 9: Quality Gates & Save
After generation, check against `references/quality-gates.md`. Common issues:
- Aspect ratio consistency: All images use the same ratio as selected in Step 3
- Character is merely decorative (not performing core action)
- Image too crowded
- Too much like a flowchart/PPT
- Too much text or severe typos (in selected language)
- Top-left corner type title appears
- Style too cute, childish, or rigid
- Background not clean white (for Base Sketch)
- **Brand Anchor Mode extra check**: Does character match reference image? Do signature features appear?
- **Language check**: Are annotations in the correct language? Are they readable?

Save final images to:
```text
output/<article-slug>/
```
Name sequentially:
```text
01-topic-name.png
02-topic-name.png
```

**Auto-Save to History**: After successful generation, append session to `output/session-history.json` with all parameters.

**Series Character Prompt**: If user says "save this character for series" → Save to `session-history.json` → `series_characters` (see `references/series-character-continuity.md`)

## Session History & Reuse Commands

| User Says | Action |
|-----------|--------|
| "Use the same settings as last time" / "和上次一样" | Load last session parameters |
| "Use my default settings" / "用默认设置" | Load `user_defaults` |
| "Save this as my default" / "保存为默认" | Save current params to `user_defaults` |
| "Show my history" / "查看历史" | List last 10 sessions with IDs |
| "Reuse session 3" / "复用第3次" | Load session by index |
| "Save this character for the series" / "保存系列角色" | Save to `series_characters` |
| "Use my [series] character" / "用系列角色" | Load series character |

## Output Style
Before generation: Visual Script should be short and precise.
After generation: Report number of images generated, each image's purpose, save path, aspect ratio used, annotation language, which images are most stable / optional.
Do not write lengthy style theory explanations; let the images speak for themselves.
