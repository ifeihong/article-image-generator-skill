---
name: article-image-generator
description: AI-powered article illustration generator for Codex, Trae, and Claude Code. Creates illustrations with configurable aspect ratios (16:9, 9:16, 4:3, 3:4, 1:1, 21:9) and quantity (1-9 images). Features dual Character Anchor Modes (Brand Anchor with fixed character reference or Context Anchor with custom per-article character) and 10 Visual Styles. Generates creative, hand-drawn style illustrations for blog posts, reports, and social media content with consistent character branding and visual storytelling.
keywords: AI image generator, article illustration, Codex skill, Trae skill, Claude Code skill, content creation, 16:9 illustration, 9:16 illustration, character consistency, visual style, GPT Image 2, blog illustration generator, WeChat article images, visual storytelling, content branding, aspect ratio configurable
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

## Dual Anchor System

### Mode Selection Rules

| Trigger Condition | Mode Used |
|------------------|-----------|
| User explicitly says "use my character" / "brand mode" / "fixed character" | Brand Anchor Mode |
| Character reference image exists in `assets/ip-reference/` | Default to Brand Anchor Mode |
| User says "context mode" / "custom character" / "free form" / "max creativity" | Context Anchor Mode |
| No reference image and user unspecified | Context Anchor Mode (default) |

### Mode Switching Commands
- "Switch to Brand Anchor mode" → Check `assets/ip-reference/` for reference image; switch if exists, prompt for upload if not
- "Switch to Context Anchor mode" → Switch directly
- "Use Brand Anchor this time, Context Anchor next time" → Execute as single-task override without changing default

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

### Mode-Specific References
- **Brand Anchor Mode**: `references/character-anchors/brand-anchor.md` — Character locking specification, reference image usage rules, character description template
- **Context Anchor Mode**: `references/character-anchors/context-anchor.md` — Character generation rules, type library, design methodologies, mandatory user confirmation workflow

## Workflow

### Step 1: Mode Confirmation
Determine which mode to use:
- Check if image files exist in `assets/ip-reference/`
- Ask user preference if not explicitly stated
- Read the corresponding mode reference document after confirmation

### Step 2: Aspect Ratio Selection
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

### Step 3: Quantity Confirmation
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
- Default: 4-8 images for medium-length articles
- Short articles: 1-3 images
- Long articles: maximum 9 images
- User says "default" / "standard" / "no preference" → Use recommended value

### Step 4: Style Selection
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

Reply with a number (e.g., "3") or style name.
```

- Confirm user selection
- Inject corresponding style declaration into all subsequent prompts
- User says "default" / "base" / "no preference" → Use [0] Base Sketch

### Step 5: Content Digestion
Read the user's article text, links, Markdown, Notion, or screenshots. Extract:
- What is the core argument?
- Which paragraphs carry cognitive turning points?
- Which content benefits from visual explanation?
- Which sections are text-only and do not need images?

Do not distribute images evenly. Prioritize "cognitive anchors": core judgments, breakpoints, closed loops, divergences, before/after contrasts, continuation paths, character state changes.

### Step 6: Visual Script (Shot List)
If the user says "analyze illustration strategy," output a Visual Script first. For each image, specify:
- Placement: after which paragraph
- Theme: what the image is about
- Core idea: what concept it communicates
- Narrative structure type
- Character action (Brand Anchor) / Character design direction (Context Anchor)
- Suggested elements
- Suggested Chinese annotation keywords

Quantity must match the user-confirmed number from Step 3.

**Context Anchor Mode Additional Step:**
Before outputting the Visual Script, **MUST confirm character design direction with the user**:
1. Based on article theme, provide 2-3 character concepts (each including: character name, visual description, personality traits, thematic connection logic)
2. Explain the generation method for each concept (Direct Translation / Heterogeneous Synthesis / Cognitive Displacement / Random Trigger)
3. Wait for user selection or modification suggestions
4. After user confirmation, output the Visual Script and begin generation

**Prohibited**: Generating characters and images without user confirmation

### Step 7: Single Image Generation
If the user explicitly requests "generate," do not stop for confirmation; generate each image individually.

**Brand Anchor Mode Generation Parameters:**
```
- Prompt: Must include complete character description (from brand-anchor.md)
- Reference image: Pass character image from assets/ip-reference/
- Reference strength: 0.6-0.8 (high consistency, preserving creative space)
- Character must perform the core conceptual action in every image
- Style declaration: Inject user-selected style (see dialect-atlas.md)
- Aspect ratio: Inject user-selected ratio (see base-genome.md)
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
```

Every image prompt must include:
- Aspect ratio declaration (from base-genome.md)
- Style declaration (from dialect-atlas.md)
- Black hand-drawn lines (Base Sketch) or corresponding style line definition
- Sparse red/orange/blue Chinese handwritten annotations (adjusted per style)
- Generous negative space (adjusted per style and aspect ratio)
- Character as the core action subject
- Prohibition: PPT, commercial illustration, childish/cute, complex architecture, top-left corner type titles

### Step 8: Quality Gates
After generation, check against `references/quality-gates.md`. Common issues:
- Aspect ratio consistency: All images use the same ratio as selected in Step 2
- Character is merely decorative (not performing core action)
- Image too crowded
- Too much like a flowchart/PPT
- Too much text or severe typos
- Top-left corner type title appears
- Style too cute, childish, or rigid
- Background not clean white (for Base Sketch)
- **Brand Anchor Mode extra check**: Does character match reference image? Do signature features appear?

### Step 9: Save & Deliver
Save final images to:
```text
assets/<article-slug>-illustrations/
```
Name sequentially:
```text
01-topic-name.png
02-topic-name.png
```

## Output Style
Before generation: Visual Script should be short and precise.
After generation: Report number of images generated, each image's purpose, save path, aspect ratio used, which images are most stable / optional.
Do not write lengthy style theory explanations; let the images speak for themselves.
