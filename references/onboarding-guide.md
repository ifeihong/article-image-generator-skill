# First-Time Onboarding Guide (首次使用引导)

## Overview

When a new user invokes the skill for the first time (no `session-history.json` exists), the skill automatically enters **Guided Expert Mode** — a walkthrough that explains each step before proceeding. This ensures new users understand the full capability without feeling overwhelmed.

## Detection

```text
IF assets/session-history.json does NOT exist:
    → First-time user detected
    → Enter Guided Expert Mode
ELSE:
    → Returning user
    → Use their saved defaults (Quick Mode or Expert Mode)
```

## Guided Expert Mode: Step-by-Step Walkthrough

### Welcome Message

```
🎨 Welcome to Article Image Generator!

This is your first time using this skill. I'll walk you through 
each step so you can get the most out of it.

You can always say "skip guide" to jump to Quick Mode, 
or "don't show this again" to disable the guide permanently.

Let's get started! ↓
```

### Step 1: Mode Selection (Explained)

```
━━━ Step 1: Choose Your Character Mode ━━━

There are two ways to use characters in your illustrations:

🧑‍🎨 Brand Anchor Mode
   Upload a character reference image (like a turnaround sheet).
   The same character appears in EVERY illustration.
   Best for: Personal brand, recurring column, IP character.

🎭 Context Anchor Mode (Recommended for first-timers)
   I design a unique character tailored to your article's theme.
   All illustrations in one article use the SAME character.
   Best for: One-off articles, varied topics, maximum creativity.

💡 Tip: You can switch modes anytime. Start with Context Anchor 
   to explore, then switch to Brand Anchor once you find a 
   character you love.

Which mode would you like? (Press Enter for Context Anchor)
```

### Step 2: Language Selection (Explained)

```
━━━ Step 2: Annotation Language ━━━

Your illustrations can include handwritten labels/annotations.
I'll auto-detect the language from your article, or you can choose:

[1] Auto-detect (recommended) — I'll match your article's language
[2] Chinese (中文) — Horizontal, 2-8 characters per label
[3] English — Horizontal, 1-3 words per label
[4] Japanese (日本語) — Horizontal or vertical, brief phrases
[5] Korean (한국어) — Horizontal, short phrases

💡 Tip: If your article is in English but your audience reads Chinese,
   you can mix — just tell me!

Press Enter for auto-detect.
```

### Step 3: Aspect Ratio (Explained)

```
━━━ Step 3: Aspect Ratio ━━━

Choose the shape of your illustrations. This affects where 
they look best:

[1] 16:9 ▬▬▬▬▬▬▬▬▬ Horizontal (Default)
    → Blog posts, articles, YouTube thumbnails

[2] 9:16 ▬▬▬ Vertical
    → Xiaohongshu, Douyin, Instagram Reels, TikTok

[3] 4:3 ▬▬▬▬▬ Horizontal
    → PPT slides, course materials, reports

[4] 3:4 ▬▬ Vertical
    → Instagram feed, social media graphics

[5] 1:1 ⬛ Square
    → Social media, avatars, product shots

[6] 21:9 ▬▬▬▬▬▬▬▬▬▬▬ Ultra-wide
    → Banners, website covers, headers

💡 Tip: Not sure? Go with [1] 16:9 — it works for most content.
   You can always change it next time.

Press Enter for 16:9, or type a number.
```

### Step 4: Quantity (Explained)

```
━━━ Step 4: How Many Illustrations? ━━━

Based on your article length, I'll recommend a number.
Here's the general guide:

Article Length          Recommended Images
─────────────────────────────────────────
Short (<1000 words)     1-3 images
Medium (1000-3000)      4-6 images
Long (>3000 words)      7-9 images

💡 Tip: More images ≠ better. Each image should serve a purpose:
   - Opening scene-setter
   - Core concept visualizer
   - Before/after comparison
   - Emotional anchor point
   - Closing memory hook

I'll analyze your article and suggest the optimal number.
Press Enter for my recommendation, or type a number (1-9).
```

### Step 5: Style Selection (Explained)

```
━━━ Step 5: Visual Style ━━━

This is where the magic happens! Choose an aesthetic style 
that transforms the base illustration:

[0] ✏️ Base Sketch — Clean white, black lines, absurd clarity
    The default. Works for everything. Think: New Yorker diagram.

[1] 📐 Retro-Tech — Yellowed paper, mechanical drafting
    Like a vintage engineering manual. Great for tech topics.

[2] 🌿 Organic Warmth — Plant veins, watercolor bleeding
    Natural, warm, alive. Great for wellness, growth, nature.

[3] 🔷 Minimal Geometry — Bauhaus grids, precise divisions
    Clean, modern, architectural. Great for business, design.

[4] 📷 Mixed Media — Photo + hand-drawn overlays
    Real objects meet illustration. Great for product, food.

[5] 🖌️ Ink-Wash Zen — Eastern ink painting, negative space
    Meditative, elegant. Great for philosophy, culture, AI.

[6] 💜 Cyber-Neon — Glowing lines, dark backgrounds
    Futuristic, electric. Great for tech, gaming, sci-fi.

[7] 🪵 Woodcut Print — Bold black-white, knife-cut texture
    Folk art energy. Great for opinion, commentary, history.

[8] 🏺 Clay Stop-Motion — 3D clay, hand-sculpted
    Playful, tactile. Great for education, children, fun topics.

[9] ⚡ Glitch Art — Digital corruption, data decay
    Edgy, experimental. Great for digital art, music, subculture.

💡 First time? Start with [0] Base Sketch — it's the most versatile.
   You can always try other styles later!

Type a number or style name. Press Enter for Base Sketch.
```

### Step 5b: Hybrid Mode (Mentioned, Not Forced)

```
💡 Advanced: Want to mix two styles? Say "Hybrid Mode" to combine 
   any two styles (e.g., Ink-Wash Zen + Cyber-Neon = "Neon ink painting").
   Available in Expert Mode after you're comfortable with the basics.
```

### Step 6: Content Analysis (Explained)

```
━━━ Step 6: Content Analysis ━━━

Now paste your article! I'll analyze it to find the best 
places for illustrations.

You can provide:
- Direct text (paste or type)
- A file path to a .md, .txt, or .docx file
- A URL (if I can access it)

💡 Tip: The best illustrations come from articles with clear 
   structure — headings, arguments, examples. Don't worry about 
   formatting; I'll extract the key ideas.

Please provide your article content:
```

### Strategy Report Offer

```
━━━ Optional: Illustration Strategy Report ━━━

Before generating images, I can show you a "Strategy Report" 
that explains:
- Where I plan to place each illustration and why
- What cognitive role each image serves
- Why I chose this character and style

This is especially useful for your first time — it helps you 
understand the visual thinking process.

Would you like to see the strategy report? (y/n, default: n)
```

### Step 7: Character Confirmation (Context Anchor)

```
━━━ Step 7: Character Design ━━━

Based on your article, I've designed 2-3 character concepts.
Each one is a visual metaphor that extends your article's ideas.

Let me introduce them:

[Character A: Name]
Visual: [description]
Personality: [traits]
Why it works: [thematic connection]

[Character B: Name]
Visual: [description]
Personality: [traits]
Why it works: [thematic connection]

💡 Tip: Don't overthink it! Pick the one that "feels right." 
   You can always ask me to tweak it.

Which character do you prefer? (A/B/modify)
```

### Completion Message

```
━━━ Generation Complete! ━━━

✅ Generated [N] illustrations in [Style] style
✅ Aspect ratio: [ratio]
✅ Annotation language: [language]
✅ Saved to: assets/[article-slug]-illustrations/

💡 Tips for next time:
- Say "same as last time" to reuse these settings
- Say "save as default" to make this your go-to configuration
- Say "quick mode" to skip all questions next time
- Say "expert mode" to get full control again

Your session has been saved. Welcome aboard! 🎨
```

## Skip Commands

| User Says | Action |
|-----------|--------|
| "skip guide" / "跳过引导" | Exit guided mode, enter normal Expert Mode |
| "don't show this again" / "不再显示" | Create `session-history.json` with defaults, never show guide again |
| "quick mode" / "快速模式" | Exit guided mode, enter Quick Mode immediately |
| "help" / "帮助" | Re-show the current step explanation |

## Returning User Detection

```text
IF session-history.json EXISTS:
    → "Welcome back! Using your saved preferences."
    → Load user_defaults
    → Enter their preferred mode (Quick or Expert)
    → Only show changes/new features since last session
```
