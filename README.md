<h1 align="center">Article Image Generator</h1>

<p align="center">
  <strong>AI-Powered Visual Storytelling for Written Content — Turn Articles into Compelling Illustrations with Configurable Aspect Ratios & Quantity</strong>
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#installation">Installation</a> •
  <a href="#quickstart">Quick Start</a> •
  <a href="#workflow">Workflow</a> •
  <a href="#visual-styles">Visual Styles</a> •
  <a href="#concepts">Concepts</a>
</p>

<p align="center">
  <a href="README.zh.md">中文</a> •
  <a href="README.ja.md">日本語</a> •
  <a href="README.ko.md">한국어</a>
</p>

---

## Overview

**Article Image Generator** is an AI skill designed for Codex, Trae, and Claude Code that transforms written content into visually striking illustrations. Unlike generic AI art tools or stock photo searches, it understands the narrative structure of your articles and generates images that serve as genuine visual extensions of your ideas — not mere decorations.

Built around two distinct **Character Anchor Modes**, ten **Visual Styles**, and configurable **Aspect Ratios** (16:9, 9:16, 4:3, 3:4, 1:1, 21:9) and **Quantity** (1-9 images), this skill adapts its creative output to match your content's platform, tone, subject matter, and audience expectations.

> "An illustration should not illustrate — it should extend."

---

## Features

### Triple Anchor Modes

Choose the right visual approach for your content:

| Aspect | Brand Anchor Mode | Context Anchor Mode | No-Character Mode |
|--------|------------------|---------------------|-------------------|
| **Core Logic** | Upload a character reference; all illustrations use the same figure | Generate a unique character tailored to each article's theme | No character at all — pure concept through abstract elements, objects, or scenes |
| **Best For** | Brand content, series articles, personal IPs, corporate blogs | Deep-dive articles, creative experiments, trending topics | Data analysis, methodology, concept explanation, atmosphere pieces |
| **Character Consistency** | Maximum (same figure across all content) | High (same figure within one article) | N/A (no character) |
| **Brand Recognition** | Strong (visual signature) | Subtle (content-first approach) | None (pure concept) |
| **Creative Freedom** | Constrained by existing character | Unbounded, maximizes creative potential | Maximum (no character constraints) |
| **User Action** | Upload reference image → auto-reuse | Confirm character concept → proceed | Select visual direction → proceed |

**Brand Anchor Mode** is ideal for content creators building a visual identity. Upload a character turnaround sheet once, and every article features your recognizable figure.

**Context Anchor Mode** is for when the content itself demands a bespoke visual voice. The character exists only for this article, making it inseparable from the content.

**No-Character Mode** is for when you want the concept itself to be the visual. No faces, no figures, no IP — just pure visual metaphors, object relationships, or atmospheric scenes that speak directly to the idea. All images in the article still share the **same locked visual style** (chosen in Step 5), ensuring the set feels cohesive even without a recurring character.

---

### Configurable Aspect Ratios & Quantity

Before generating, the skill guides you through two quick configuration steps:

**Aspect Ratio Selection** — Choose the canvas shape that matches your target platform:

| Ratio | Orientation | Best For |
|:---:|:---:|:---|
| **16:9** | Horizontal | Blog posts, YouTube thumbnails, LinkedIn articles, Medium (default) |
| **9:16** | Vertical | TikTok, Instagram Reels, YouTube Shorts, Pinterest, phone wallpapers |
| **4:3** | Horizontal | PowerPoint, Keynote, course slides, reports, presentations |
| **3:4** | Vertical | Instagram carousel, Facebook posts, Pinterest pins, Substack |
| **1:1** | Square | Instagram feed, Twitter/X, avatars, product shots, square ads |
| **21:9** | Ultra-wide | Website banners, Twitter/X headers, Twitch, ultrawide displays |

The skill provides smart recommendations based on your content type, but you can override with any ratio.

**Quantity Selection** — Choose how many illustrations to generate (1-9):

| Article Length | Recommended Quantity |
|:---|:---:|
| Short (< 1000 words) | 1-3 images |
| Medium (1000-3000 words) | 4-6 images |
| Long (> 3000 words) | 7-9 images |

---

### Ten Visual Styles

Before generating, the skill prompts you to select a visual style — a complete aesthetic system that transforms the base visual DNA:

| ID | Style | Visual Signature | Best For |
|:---:|:---|:---|:---|
| 0 | **Base Sketch** | White canvas, black hand-drawn lines, absurd clarity | Default — tech, business, general |
| 1 | **Retro-Tech** | Yellowed engineering manual, mechanical drafting aesthetic | History, industry, nostalgia |
| 2 | **Organic Warmth** | Plant veins, watercolor bleeding, natural growth | Environment, wellness, lifestyle |
| 3 | **Minimal Geometry** | Bauhaus grids, precise divisions, restrained color | Data visualization, design, high-end rationality |
| 4 | **Mixed Media** | Photo base + hand-drawn overlays, real object mashups | Tutorials, DIY, creative processes |
| 5 | **Ink-Wash Zen** | Eastern ink painting, negative space mastery, brush gradation | Culture, philosophy, Eastern aesthetics |
| 6 | **Cyber-Neon** | Glowing neon lines, dark backgrounds, tech luminescence | Future tech, AI, metaverse, digital culture |
| 7 | **Woodcut Print** | Bold black-white contrast, knife-cut texture, folk art | Social issues, humanities, powerful expression |
| 8 | **Clay Stop-Motion** | 3D clay texture, hand-sculpted, rounded and charming | Education, children, light science, healing |
| 9 | **Glitch Art** | Digital corruption, stripe displacement, data decay aesthetics | Digital critique, hacker culture, experimental art |

Each dialect includes a complete prompt-injection template that automatically appends to generation instructions, ensuring visual coherence across all illustrations in an article.

**Style Previews** — Same character, same scene, 10 different styles:

| Base Sketch | Retro-Tech | Organic Warmth | Minimal Geometry | Mixed Media |
|:---:|:---:|:---:|:---:|:---:|
| ![Base Sketch](assets/style-previews/00-base-sketch.jpg) | ![Retro-Tech](assets/style-previews/01-retro-tech.jpg) | ![Organic Warmth](assets/style-previews/02-organic-warmth.jpg) | ![Minimal Geometry](assets/style-previews/03-minimal-geometry.jpg) | ![Mixed Media](assets/style-previews/04-mixed-media.jpg) |

| Ink-Wash Zen | Cyber-Neon | Woodcut Print | Clay Stop-Motion | Glitch Art |
|:---:|:---:|:---:|:---:|:---:|
| ![Ink-Wash Zen](assets/style-previews/05-ink-wash-zen.jpg) | ![Cyber-Neon](assets/style-previews/06-cyber-neon.jpg) | ![Woodcut Print](assets/style-previews/07-woodcut-print.jpg) | ![Clay Stop-Motion](assets/style-previews/08-clay-stop-motion.jpg) | ![Glitch Art](assets/style-previews/09-glitch-art.jpg) |

---

### Concept Forge: Four Creative Methodologies

Context Anchor Mode includes four distinct character-design methodologies, ensuring your visual protagonist is never a random creation but a deliberate conceptual extension:

**1. Direct Translation**
Translate the article's core concept directly into visual form:
- "Light chip bottleneck" → A light-woven figure being squeezed between two walls
- "Data flood" → A fish made of streaming binary code

**2. Heterogeneous Synthesis**
Force-combine three unrelated domains into a coherent visual:
- Structure (kitchen/post office/factory/forest) × Texture (circuit board/paper/glass/plant) × Action (climbing/cooking/detecting/sailing)
- Example: Post office structure + paper texture + cooking action = A kitchen made of envelopes and stamps, where the character "cooks" information

**3. Cognitive Displacement**
Four types of deliberate misalignment that create memorable visuals:
- **Scale Displacement**: A microchip expanded to city size, or an ocean shrunk to a teacup
- **Function Displacement**: Using an umbrella as a funnel, or making an elephant thread a needle
- **Temporal Displacement**: An abacus processing AI data, or a laser pen writing calligraphy
- **Emotional Displacement**: An anxious microchip sweating, or a lazy fiber optic cable refusing to transmit

**4. Random Trigger**
When direction is unclear, combine from pools:
- Material (metal/glass/paper/wood/light) + Entity (cat/bird/tree/gear/cloud) + Profession (messenger/guard/chef/detective) + Emotion (anxious/calm/excited/confused)

---

### User Confirmation Flow (Context Anchor Mode)

The skill never generates characters without your approval:

1. **Present Options**: 2-3 character concepts based on article theme, each with name, visual description, personality traits, and thematic connection logic
2. **Await Selection**: You choose, modify, or provide your own concept
3. **Freeze Description**: The approved character description is locked and reused for all illustrations in the article
4. **Unified Execution**: Every image in the article uses the same character, ensuring visual consistency

---

### Multi-Language Annotation Support

The skill auto-detects your article's language and generates annotations in the same language — or you can manually select:

| Detected Language | Annotation Style | Example |
|:---|:---|:---|
| **Chinese** | Horizontal, 2-8 characters, handwritten | 光芯片 / 数据流 / 瓶颈 |
| **English** | Horizontal, 1-3 words, handwritten | Light Chip / Data Flow / Bottleneck |
| **Japanese** | Horizontal or vertical, brief phrases | 光チップ / データ流 / ボトルネック |
| **Korean** | Horizontal, short phrases | 광칩 / 데이터 흐름 / 병목 |

**Auto-detection**: Analyzes article text (>50% character type). **Manual override**: "Generate with English annotations."

---

### Quick Mode vs Expert Mode

Choose your workflow based on time and control needs:

| Aspect | Quick Mode | Expert Mode |
|--------|-----------|-------------|
| **Steps** | 1-step auto-detect | Full 10-step pipeline (Step 0-9) |
| **Best For** | Fast results, familiar users | First-time users, precise control |
| **Parameters** | All auto-detected | User selects each parameter |
| **Override** | Inline overrides supported | Full granular control |
| **Strategy Report** | Skipped | Optional pre-generation |

**Quick Mode Example**: "Generate illustrations for this article" → Auto-detects language, 16:9, 6 images, Base Sketch.

**Expert Mode Example**: "Expert mode" → Step-by-step: mode → language → aspect ratio → quantity → style → (optional strategy report) → content digestion → generation.

---

### Hybrid Style Mixing (Expert Mode)

Combine two styles for unique visual effects:

| Primary (60-70%) | Secondary (30-40%) | Result |
|:---|:---|:---|
| Ink-Wash Zen | Cyber-Neon | "Neon ink painting" — traditional brush with glowing accents |
| Clay Stop-Motion | Glitch Art | "Corrupted clay" — handmade forms with digital artifacts |
| Retro-Tech | Organic Warmth | "Bio-mechanical vintage" — old machinery with plant overgrowth |

Activate by selecting **[H] Hybrid Mode** during style selection.

---

### Session History & Reuse

The skill automatically saves your generation parameters after each session. Reuse with simple commands:

| Command | Action |
|:---|:---|
| "Use the same settings as last time" | Load last session |
| "Use my default settings" | Load saved defaults |
| "Save this as my default" | Save current params |
| "Show my history" | List last 10 sessions |
| "Reuse session 3" | Load specific session |

History is stored locally in `output/session-history.json` — no data leaves your machine.

---

### Series Character Continuity

Writing a series? Save your Context Anchor character for reuse across multiple articles:

1. **Save**: "Save this character for my AI Weekly series" → Stored in session history
2. **Reuse**: "Use my AI Weekly character" → Skips confirmation, uses saved character
3. **Manage**: List, update, retire, or clone series characters

| Feature | Brand Anchor | Series Character | Context Anchor |
|--------|-------------|------------------|----------------|
| Scope | All content | One series | One article |
| Persistence | Permanent | Semi-permanent | Temporary |
| Best For | Personal IP | Column series, newsletters | One-off articles |

---

### Illustration Strategy Report (Expert Mode)

Before generating, request a strategy report to understand the visual thinking:

```
"Show me the strategy first"
```

The report includes:
- **Content Analysis**: Article type, core argument, target audience
- **Visual Anchor Points**: Which sections need images and why
- **Cognitive Load Map**: Text-only vs visual-supported sections
- **Character Strategy**: Why this character fits the content
- **Style Justification**: Why this style matches the tone
- **Quantity & Placement**: How many images and where

This turns image generation into a teachable content design process.

---

### First-Time User Onboarding

New users are automatically guided through a **step-by-step walkthrough** on first use:

1. **Welcome**: Friendly introduction with option to skip
2. **Mode Explanation**: Visual comparison of Brand Anchor vs Context Anchor vs No-Character with use cases
3. **Language Selection**: Clear explanation of each language option
4. **Aspect Ratio Guide**: Visual shape previews with platform recommendations
5. **Quantity Guide**: Word count → image count mapping with cognitive purpose
6. **Style Gallery**: Each style with emoji icon, description, and best-for guidance
7. **Content Input**: Clear instructions on supported formats
8. **Strategy Report Offer**: Optional pre-generation analysis
9. **Character Selection**: Guided character concept comparison
10. **Completion**: Summary with tips for next time

Skip commands: "skip guide" / "don't show this again" / "quick mode"

---

### Error Handling

The skill provides clear guidance for common issues:

| Scenario | Recovery |
|----------|----------|
| Reference image not found | Prompt upload or switch to Context Anchor |
| Reference image too small/blurry | Explain requirements, offer alternatives |
| Reference image has multiple characters | Ask which to use, offer crop |
| Article too short (<500 words) | Suggest 1 hero image or provide more content |
| Article too long (>5000 words) | Recommend section-based generation |
| Character inconsistency | Strengthen keywords, simplify design |
| Wrong annotation language | Re-generate with explicit declaration |
| Style not applied correctly | Re-generate with stronger injection |
| Generation failed (rate limit) | Wait 30s and retry, reduce count |

All errors include: explanation of what went wrong, why, and 2-3 actionable options.

---

### Style Preview Gallery

Preview images for all 10 styles are available in `assets/style-previews/`. Say "show me the styles" to browse before choosing.

---

### Professional Workflow: 10-Step Pipeline (Step 0-9)

```
Step 0: Workflow Mode Selection → Step 1: Mode Confirmation → Step 2: Language Selection
    → Step 3: Aspect Ratio Selection → Step 4: Quantity Confirmation → Step 5: Style Selection
    → Step 6: Content Digestion → Step 7: Visual Script (Shot List)
    → Step 8: Single Image Generation → Step 9: Quality Gates & Save
```

| Step | Name | Description |
|:---:|:---|:---|
| 0 | Workflow Mode Selection | Choose Quick Mode (1-step auto) or Expert Mode (full control) |
| 1 | Mode Confirmation | Check `assets/ip-reference/` for reference image; ask user preference |
| 2 | Language Selection | Auto-detect or manually select annotation language (zh/en/ja/ko) |
| 3 | Aspect Ratio Selection | Choose canvas shape: 16:9, 9:16, 4:3, 3:4, 1:1, or 21:9 |
| 4 | Quantity Confirmation | Confirm number of illustrations (1-9, smart recommendation) |
| 5 | Style Selection | Select from 10 Visual Styles; optional Hybrid Mode mixing |
| 6 | Content Digestion | Analyze article structure, cognitive anchors, visual opportunities |
| 7 | Visual Script (Shot List) | Plan each image: placement, theme, composition, annotations |
| 8 | Single Image Generation | Generate images sequentially with style/character/ratio injection |
| 9 | Quality Gates & Save | Check quality, iterate if needed, save to `output/<article-slug>/` |

---

## Installation

### Prerequisites

- **Codex**, **Trae**, or **Claude Code** (any AI assistant supporting the Skill system)
- Image generation capability enabled (GPT Image 2 / ChatGPT Images 2.0)
- Git (for cloning)

### Method 1: Git Clone (Recommended)

```bash
git clone https://github.com/ifeihong/article-image-generator-skill.git
cd article-image-generator-skill
```

Copy the repository contents to your AI assistant's Skills directory:

| AI Assistant | Skills Directory |
|-------------|------------------|
| **Codex** | `~/.codex/skills/` or `.codex/skills/` in project root |
| **Trae** | `~/.trae/skills/` or `.trae/skills/` in project root |
| **Claude Code** | `~/.claude/skills/` or `.claude/skills/` in project root |

Expected directory structure:
```
skills/
└── article-image-generator/
    ├── SKILL.md
    ├── README.md
    ├── README.zh.md
    ├── README.ja.md
    ├── README.ko.md
    ├── output/                       ← Generated illustrations (auto-created)
    ├── assets/
    │   ├── style-previews/           ← 10 style preview images (bundled)
    │   └── ip-reference/             ← Brand Anchor reference (user-provided)
    │       └── ip.png
    └── references/
        ├── visual-genome/
        ├── character-anchors/
        ├── concept-forge/
        ├── narrative-structures.md
        ├── generation-protocols.md
        └── quality-gates.md
```

### Method 2: Direct Install (Trae/Codex Native)

Some AI assistants support direct installation from GitHub URL:

```
Install Skill: https://github.com/ifeihong/article-image-generator-skill
```

### Method 3: Manual Download

1. Download from [GitHub Releases](https://github.com/ifeihong/article-image-generator-skill/releases)
2. Extract to your Skills directory
3. For Brand Anchor mode, place your character turnaround in `assets/ip-reference/ip.png`

---

## Quick Start

### Basic Invocation

```
Use Article Image Generator to create illustrations for this article.
```

Or with article text:

```
Generate illustrations for the following content:
[paste article text]
```

### Specify Mode

```
Use Brand Anchor mode for this article.    ← Uses assets/ip-reference/ reference image
Use Context Anchor mode for this article.  ← Generates a custom character
```

### Specify Aspect Ratio & Quantity

```
Use 9:16 aspect ratio, 6 images.           ← Direct ratio + quantity
Use Article Image Generator with 4:3, 3 images.  ← Ratio + quantity
```

### Specify Style

```
Use Cyber-Neon style for this article.     ← Direct style selection
Use Article Image Generator with Ink-Wash Zen style.  ← By style name
```

### Specify Language

```
Generate with English annotations.   ← Manual language selection
Use Japanese labels.                 ← Japanese annotations
```

### Quick Mode vs Expert Mode

```
Generate illustrations for this article.     ← Quick Mode (auto-detect all)
Use expert mode.                             ← Full 10-step pipeline (Step 0-9)
Same as last time.                           ← Reuse last session
Show me the strategy first.                  ← Expert Mode + Strategy Report
```

### Series Character

```
Save this character for my AI Weekly series.  ← Save series character
Use my AI Weekly character.                   ← Reuse series character
```

### Complete Example

```
Use Article Image Generator, Context Anchor mode, 9:16 aspect ratio, 6 images, Cyber-Neon style,
to generate illustrations for:

[article text...]
```

---

## Visual Genome

The foundational DNA shared across all styles:

- **Configurable aspect ratio** — 16:9 (default), 9:16, 4:3, 3:4, 1:1, or 21:9
- **Pure white canvas**: No beige, warm gray, paper texture, gradients, or shadows
- **Black hand-drawn lines**: Fine, slightly wobbly, non-mechanical, non-vector
- **Generous negative space**: Subject occupies 40-60% of canvas; at least 35% blank
- **Sparse Chinese handwritten annotations**: Maximum 5-8 instances, 2-8 characters each
- **One image, one core idea**: A single action, structure, state, or metaphor per image

### Color Discipline

| Color | Purpose |
|-------|---------|
| Black | Main line art, character, frames, primary text |
| Red | Critical annotations, problems, emotional points, key reminders, results |
| Orange | Main flow, paths, arrows, movement from A to B |
| Blue | Supplementary notes, system states, secondary explanations, AI/automation hints |

Blue is optional per image. Color usage should be restrained — less is more.

### What to Avoid

- Commercial illustrations, PPT infographics, formal flowcharts
- Course slides, cute cartoon posters, children's illustrations
- Complex architecture diagrams, polished flat illustrations, tech UI aesthetics
- Real app screenshots, complex backgrounds, gradients, shadows
- Over-explaining every node
- Top-left corner titles like "Workflow / System Architecture / Common Pitfalls"

---

## Technical Notes

### Reference Image Upload (Brand Anchor Mode)

The current Codex/Trae `GenerateImage` tool does not support a `reference_image` parameter. Brand Anchor mode achieves consistency through:

1. **Enhanced text descriptions**: Comprehensive character appearance embedded in every prompt
2. **GPT Image 2 session context**: Multi-turn generation within the same session references historical outputs
3. **Frozen character descriptions**: A standardized description format reused across all images

**Future enhancement**: When the underlying tool supports reference image parameters, `character-anchors/brand-anchor.md` will be updated to use `reference_image` and `reference_strength` for true image-level character locking.

### GPT Image 2 Multi-Image Consistency

GPT Image 2 (ChatGPT Images 2.0) supports:
- Single-prompt generation of 8 images with consistent character and style
- Multi-turn conversational editing: reference historical outputs within a session
- 4K resolution and precise text rendering

This skill leverages session context mechanisms, combined with frozen character descriptions, to maximize consistency probability in Context Anchor mode.

---

## File Structure

| File/Directory | Purpose |
|----------------|---------|
| `SKILL.md` | Skill entry point — complete workflow and invocation rules |
| `README.md` | Project documentation (this file) |
| `README.zh.md` | Chinese documentation |
| `README.ja.md` | Japanese documentation |
| `README.ko.md` | Korean documentation |
| `output/` | Generated illustrations and session history (user output) |
| `references/visual-genome/` | Base visual DNA and 10 dialect definitions |
| `references/character-anchors/` | Brand Anchor and Context Anchor mode specifications |
| `references/concept-forge/` | Heterogeneous Synthesis matrix and Cognitive Displacement methods |
| `references/narrative-structures.md` | 8 narrative composition patterns |
| `references/generation-protocols.md` | Generation prompt templates for both modes and all styles |
| `references/quality-gates.md` | Post-generation quality checklist and iteration methods |
| `references/session-history.md` | Session history format and reuse commands |
| `references/illustration-strategy-report.md` | Strategy report structure and cognitive analysis framework |
| `references/series-character-continuity.md` | Series character save/reuse workflow |
| `references/onboarding-guide.md` | First-time user guided walkthrough |
| `references/error-handling.md` | Error scenarios and recovery strategies |
| `references/platform-detection.md` | Platform keyword detection rules for Quick Mode auto-ratio |
| `assets/style-previews/` | 10 Visual Style preview images (bundled) |
| `assets/ip-reference/` | Brand Anchor mode reference image (user-provided, not in repo) |

---

## FAQ

**Q: The character in Brand Anchor mode doesn't match my reference image.**

A: Current environment limitations. Improve by: (1) strengthening character keywords in prompts, (2) ensuring a clear, complete, white-background reference, (3) simplifying character design. True reference-image support is planned for future updates.

**Q: Can I save a Context Anchor character for future use?**

A: Yes. Save the character description as an image and place it in `assets/ip-reference/ip.png` to convert it to Brand Anchor mode.

**Q: Are generated images commercially usable?**

A: Depends on your underlying image generation model's terms. GPT Image 2 outputs are generally commercially usable; verify OpenAI's current usage policy.

**Q: Does it support English articles?**

A: Currently optimized for Chinese content (annotation conventions, layout habits). English articles work but annotations may feel less natural.

**Q: How long does one image take?**

A: GPT Image 2 typically 5-15 seconds per image; 4K resolution may take 20-30 seconds.

---

## Contributing

Issues and Pull Requests welcome!

- Bugs or questions: [Open an Issue](https://github.com/ifeihong/article-image-generator-skill/issues)
- New dialects or features: [Submit a PR](https://github.com/ifeihong/article-image-generator-skill/pulls)
- Showcase your creations: Tag your Issue with `showcase`

---

<p align="center">
  If this project helps you, please give it a ⭐ Star!
</p>

<p align="center">
  <a href="https://github.com/ifeihong/article-image-generator-skill">GitHub Repository</a> •
  <a href="https://github.com/ifeihong/article-image-generator-skill/issues">Issue Tracker</a>
</p>
