---
name: article-image-generator
description: AI-powered article illustration generator for Codex, Trae, and Claude Code. Creates 16:9 horizontal illustrations with dual Character Anchor Modes (Brand Anchor with fixed character reference or Context Anchor with custom per-article character) and 10 Visual Dialects. Generates creative, hand-drawn style illustrations for blog posts, reports, and social media content with consistent character branding and visual storytelling.
keywords: AI image generator, article illustration, Codex skill, Trae skill, Claude Code skill, content creation, 16:9 illustration, character consistency, visual dialect, GPT Image 2, blog illustration generator, WeChat article images, visual storytelling, content branding
---

# Article Image Generator

## Core Positioning

Transform written content into compelling 16:9 horizontal illustrations. Convert key judgments, workflows, structures, states, or metaphors from articles into clean, absurd, creative, readable — yet non-instructional — hand-drawn explanatory visuals.

Supports two Character Anchor Modes:
- **Brand Anchor Mode**: Uses a user-provided character reference image. The same figure appears in every illustration, ideal for brand consistency and visual identity
- **Context Anchor Mode**: Generates a bespoke character tailored to each article's theme. **All illustrations within one article use the same character**, maximizing content-native creativity and conceptual depth

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
- `references/visual-genome/base-genome.md`: Visual DNA, color discipline, typography, prohibitions
- `references/visual-genome/dialect-atlas.md`: 10 Visual Dialect definitions and prompt-injection templates
- `references/concept-forge/heterogeneous-synthesis.md`: Cross-domain synthesis matrix for character design
- `references/concept-forge/cognitive-displacement.md`: Four types of deliberate misalignment for creative visuals
- `references/narrative-structures.md`: 8 narrative composition patterns
- `references/generation-protocols.md`: Generation prompt templates for both modes and all dialects
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

### Step 2: Dialect Selection
**Before digesting content, the user MUST select a Visual Dialect.**

Present the dialect menu:
```
Please select a Visual Dialect (enter number or dialect name):

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

Reply with a number (e.g., "3") or dialect name.
```

- Confirm user selection
- Inject corresponding dialect declaration into all subsequent prompts
- User says "default" / "base" / "no preference" → Use [0] Base Sketch

### Step 3: Content Digestion
Read the user's article text, links, Markdown, Notion, or screenshots. Extract:
- What is the core argument?
- Which paragraphs carry cognitive turning points?
- Which content benefits from visual explanation?
- Which sections are text-only and do not need images?

Do not distribute images evenly. Prioritize "cognitive anchors": core judgments, breakpoints, closed loops, divergences, before/after contrasts, continuation paths, character state changes.

### Step 4: Visual Script (Shot List)
If the user says "analyze illustration strategy," output a Visual Script first. For each image, specify:
- Placement: after which paragraph
- Theme: what the image is about
- Core idea: what concept it communicates
- Narrative structure type
- Character action (Brand Anchor) / Character design direction (Context Anchor)
- Suggested elements
- Suggested Chinese annotation keywords

Default: 4-8 images. Short articles: 1-3 images. Long articles: maximum 9 images.

**Context Anchor Mode Additional Step:**
Before outputting the Visual Script, **MUST confirm character design direction with the user**:
1. Based on article theme, provide 2-3 character concepts (each including: character name, visual description, personality traits, thematic connection logic)
2. Explain the generation method for each concept (Direct Translation / Heterogeneous Synthesis / Cognitive Displacement / Random Trigger)
3. Wait for user selection or modification suggestions
4. After user confirmation, output the Visual Script and begin generation

**Prohibited**: Generating characters and images without user confirmation

### Step 5: Single Image Generation
If the user explicitly requests "generate," do not stop for confirmation; generate each image individually.

**Brand Anchor Mode Generation Parameters:**
```
- Prompt: Must include complete character description (from brand-anchor.md)
- Reference image: Pass character image from assets/ip-reference/
- Reference strength: 0.6-0.8 (high consistency, preserving creative space)
- Character must perform the core conceptual action in every image
- Dialect declaration: Inject user-selected dialect (see dialect-atlas.md)
```

**Context Anchor Mode Generation Parameters:**
```
- Prompt: Include character description customized for the theme (same character description for all images in one article)
- No reference image: Pure text-driven
- All illustrations in one article MUST use the same character; character appearance must be consistent
- Character actions and poses may vary per image, but core appearance, material, and signature features must remain consistent
- Encourage cross-domain synthesis and cognitive displacement metaphors
- Dialect declaration: Inject user-selected dialect (see dialect-atlas.md)
```

Every image prompt must include:
- 16:9 horizontal Chinese article illustration
- Dialect declaration (from dialect-atlas.md)
- Black hand-drawn lines (Base Sketch) or corresponding dialect line definition
- Sparse red/orange/blue Chinese handwritten annotations (adjusted per dialect)
- Generous negative space (adjusted per dialect)
- Character as the core action subject
- Prohibition: PPT, commercial illustration, childish/cute, complex architecture, top-left corner type titles

### Step 6: Quality Gates
After generation, check against `references/quality-gates.md`. Common issues:
- Character is merely decorative (not performing core action)
- Image too crowded
- Too much like a flowchart/PPT
- Too much text or severe typos
- Top-left corner type title appears
- Style too cute, childish, or rigid
- Background not clean white (for Base Sketch)
- **Brand Anchor Mode extra check**: Does character match reference image? Do signature features appear?

### Step 7: Save & Deliver
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
After generation: Report number of images generated, each image's purpose, save path, which images are most stable / optional.
Do not write lengthy style theory explanations; let the images speak for themselves.
