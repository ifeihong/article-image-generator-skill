<h1 align="center">Article Image Generator</h1>

<p align="center">
  <strong>AI-Powered Visual Storytelling for Written Content — Turn Articles into Compelling 16:9 Illustrations</strong>
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#installation">Installation</a> •
  <a href="#quickstart">Quick Start</a> •
  <a href="#workflow">Workflow</a> •
  <a href="#visual-dialects">Visual Dialects</a> •
  <a href="#concepts">Concepts</a>
</p>

<p align="center">
  <a href="README.zh.md">中文</a> •
  <a href="README.ja.md">日本語</a> •
  <a href="README.ko.md">한국어</a>
</p>

---

## Overview

**Article Image Generator** is an AI skill designed for Codex, Trae, and Claude Code that transforms written content into visually striking 16:9 horizontal illustrations. Unlike generic AI art tools or stock photo searches, it understands the narrative structure of your articles and generates images that serve as genuine visual extensions of your ideas — not mere decorations.

Built around two distinct **Character Anchor Modes** and ten **Visual Dialects**, this skill adapts its creative output to match your content's tone, subject matter, and audience expectations.

> "An illustration should not illustrate — it should extend."

---

## Features

### Dual Character Anchor Modes

Choose between brand consistency and content-native creativity:

| Aspect | Brand Anchor Mode | Context Anchor Mode |
|--------|------------------|---------------------|
| **Core Logic** | Upload a character reference; all illustrations use the same figure | Generate a unique character tailored to each article's theme |
| **Best For** | Brand content, series articles, personal IPs, corporate blogs | Deep-dive articles, creative experiments, trending topics |
| **Character Consistency** | Maximum (same figure across all content) | High (same figure within one article) |
| **Brand Recognition** | Strong (visual signature) | Subtle (content-first approach) |
| **Creative Freedom** | Constrained by existing character | Unbounded, maximizes creative potential |
| **User Action** | Upload reference image → auto-reuse | Confirm character concept → proceed |

**Brand Anchor Mode** is ideal for content creators building a visual identity. Upload a character turnaround sheet once, and every article features your recognizable figure — readers see your character and know it's your content.

**Context Anchor Mode** is for when the content itself demands a bespoke visual voice. Writing about quantum computing? Your character might be a "Probability Ghost" — a translucent figure made of floating equations. The character exists only for this article, making it inseparable from the content.

---

### Ten Visual Dialects

Before generating, the skill prompts you to select a visual dialect — a complete aesthetic system that transforms the base visual DNA:

| ID | Dialect | Visual Signature | Best For |
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

### Professional Workflow: 8-Step Standardized Pipeline

```
Mode Confirmation → Dialect Selection → Content Digestion → Visual Script (Shot List)
        ↓
Character Confirmation (Context Mode) → Single Image Generation → Quality Gates → Save & Deliver
```

**Step 1: Mode Confirmation**
Checks for reference images in `assets/ip-reference/` and asks your preference.

**Step 2: Dialect Selection**
Presents the 10-dialect menu; you respond with a number or dialect name.

**Step 3: Content Digestion**
Analyzes core arguments, cognitive turning points, and which sections benefit from visual support.

**Step 4: Visual Script (Shot List)**
Outputs a detailed plan for each image: placement, theme, structure type, character action, suggested elements, and Chinese annotation keywords. Default: 4-8 images per article.

**Step 5: Character Confirmation (Context Mode)**
Presents 2-3 character concepts and awaits your selection.

**Step 6: Single Image Generation**
Generates each image sequentially with prompts containing: 16:9 declaration, dialect injection, character description, composition instructions, and constraint rules.

**Step 7: Quality Gates**
Checks against the quality checklist: character centrality, whitespace ratio, PPT avoidance, annotation readability, color discipline, and style consistency.

**Step 8: Save & Deliver**
Images saved to `assets/<article-slug>-illustrations/` with sequential naming `01-topic-name.png`.

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
    ├── assets/
    │   └── ip-reference/
    │       └── character-3view.png    ← Brand Anchor reference (optional)
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
3. For Brand Anchor mode, place your character turnaround in `assets/ip-reference/character-3view.png`

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

### Specify Dialect

```
Use Cyber-Neon dialect for this article.   ← Direct dialect selection
Use Article Image Generator with Ink-Wash Zen style.  ← By dialect name
```

### Complete Example

```
Use Article Image Generator, Context Anchor mode, Cyber-Neon dialect,
to generate 6 illustrations for:

[article text...]
```

---

## Visual Genome

The foundational DNA shared across all dialects:

- **16:9 horizontal** format for article embedding
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
| `assets/ip-reference/` | Brand Anchor mode reference image storage |
| `references/visual-genome/` | Base visual DNA and 10 dialect definitions |
| `references/character-anchors/` | Brand Anchor and Context Anchor mode specifications |
| `references/concept-forge/` | Heterogeneous Synthesis matrix and Cognitive Displacement methods |
| `references/narrative-structures.md` | 8 narrative composition patterns |
| `references/generation-protocols.md` | Prompt templates for both modes and all dialects |
| `references/quality-gates.md` | Post-generation quality checklist and iteration methods |

---

## FAQ

**Q: The character in Brand Anchor mode doesn't match my reference image.**

A: Current environment limitations. Improve by: (1) strengthening character keywords in prompts, (2) ensuring a clear, complete, white-background reference, (3) simplifying character design. True reference-image support is planned for future updates.

**Q: Can I save a Context Anchor character for future use?**

A: Yes. Save the character description as an image and place it in `assets/ip-reference/character-3view.png` to convert it to Brand Anchor mode.

**Q: Are generated images commercially usable?**

A: Depends on your underlying image generation model's terms. GPT Image 2 outputs are generally commercially usable; verify OpenAI's current usage policy.

**Q: Does it support English articles?**

A: Currently optimized for Chinese content (annotation conventions, layout habits). English articles work but annotations may feel less natural.

**Q: How long does one image take?**

A: GPT Image 2 typically 5-15 seconds per image; 4K resolution may take 20-30 seconds.

---

## Changelog

### v1.0 (2026-06-18)
- Initial release
- Dual Character Anchor Modes (Brand + Context)
- 10 Visual Dialects
- Four Concept Forge methodologies
- 8-step standardized workflow
- User confirmation flow
- Multi-language documentation (EN/ZH/JA/KO)

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
