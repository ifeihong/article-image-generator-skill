# Error Handling Guide (错误处理指南)

## Overview

This document covers common error scenarios and recovery strategies. When an error occurs, the skill should provide clear, actionable guidance to the user rather than failing silently.

## Error Categories

### 1. Reference Image Issues (Brand Anchor Mode)

#### Error: No Reference Image Found
```
⚠️ Brand Anchor Mode requires a character reference image.

Expected location: assets/ip-reference/character-3view.png

Options:
[1] Upload your character turnaround sheet to the above path
[2] Switch to Context Anchor Mode (I'll design a character for you)
[3] Provide a different image path

Which option? (Press Enter for [2] Context Anchor)
```

#### Error: Reference Image Too Small / Low Resolution
```
⚠️ The reference image appears to be low resolution ([width]x[height]).

For best character consistency, use an image that is:
- At least 1024x1024 pixels
- Clear, well-lit, with a white or light background
- Shows the character from multiple angles (front, side, back)

Current image quality issues:
- [specific issue: blurry / too small / dark / cluttered background]

Suggestions:
[1] I'll try my best with this image (character may not match perfectly)
[2] Provide a higher quality image
[3] Switch to Context Anchor Mode

Which option?
```

#### Error: Reference Image Not Recognizable as Character
```
⚠️ The reference image doesn't appear to be a character turnaround sheet.

What I expected: A clean image showing a character from multiple angles 
(front view, side view, back view) on a white background.

What I see: [description of what's actually in the image]

This could be:
- A photograph of a person (works, but less consistent)
- A landscape/scene (not suitable as character reference)
- A logo or icon (too simple for character generation)

Options:
[1] Try anyway (results may vary)
[2] Provide a proper character turnaround sheet
[3] Switch to Context Anchor Mode

💡 Tip: For best results, use a simple character design with clear 
   outlines, shown from 3 angles on a white background. 
   Avoid: photos with busy backgrounds, complex 3D renders, 
   multiple characters in one image.
```

#### Error: Reference Image Has Multiple Characters
```
⚠️ The reference image contains multiple characters.

I can only lock onto ONE character for consistency. 

I see approximately [N] character(s) in the image.

Options:
[1] Use the character on the [left/center/right] — describe which one
[2] Crop and provide a single-character image
[3] Switch to Context Anchor Mode

Please specify which character to use, or choose another option.
```

### 2. Article Content Issues

#### Error: Article Too Short
```
⚠️ The article appears to be very short ([word count] words).

For meaningful illustrations, I recommend at least 500 words.
With shorter content, illustrations may feel forced or unnecessary.

Options:
[1] Generate 1 illustration anyway (best for a cover/hero image)
[2] Provide more article content
[3] Cancel

💡 Tip: Even short articles benefit from ONE strong opening image.
   Think of it as a "visual headline."
```

#### Error: Article Too Long
```
⚠️ The article is very long ([word count] words).

Generating 9+ illustrations for a single article may:
- Take a long time (5-15 seconds per image)
- Result in repetitive visuals
- Exceed quality control thresholds

Recommendation: Split into sections and generate illustrations 
for the most important sections only.

Options:
[1] Generate 9 illustrations (maximum) for key sections
[2] Let me analyze and pick the best sections (recommended)
[3] Generate for specific sections only (tell me which)

Which option?
```

#### Error: Cannot Parse Article Content
```
⚠️ I couldn't extract readable content from the input.

The article content appears to be:
- [empty / corrupted / in an unsupported format / behind a paywall]

Supported formats:
- Direct text (paste or type)
- .md, .txt, .docx files (provide file path)
- URLs to publicly accessible pages

Options:
[1] Paste the article text directly
[2] Provide a file path
[3] Provide a different URL

💡 Tip: For best results, paste the article text directly.
   This avoids format parsing issues.
```

### 3. Generation Quality Issues

#### Error: Character Inconsistency Across Images
```
⚠️ The character appears inconsistent across illustrations.

Detected issues:
- [specific issue: different hair color / different body shape / 
  different clothing / missing signature feature]

This is a known limitation in the current environment. The 
GenerateImage tool doesn't support reference_image parameters yet.

Improvement strategies:
[1] Regenerate with enhanced character description (recommended)
    → I'll strengthen the character keywords in the prompt
[2] Regenerate the inconsistent images only
[3] Accept current results (minor variations add charm)

💡 Tip: Simpler character designs are more consistent. 
   If your character is very detailed, consider simplifying 
   the key features to 3-5 distinctive traits.
```

#### Error: Style Not Applied Correctly
```
⚠️ The generated image doesn't match the selected style "[style name]".

Expected style elements: [list key style features]
What I see: [description of actual output]

Options:
[1] Regenerate with stronger style injection
[2] Try a different style
[3] Accept current result

💡 Tip: Some styles work better with certain content types.
   For example, Cyber-Neon works great for tech but may 
   feel odd for a nature article.
```

#### Error: Aspect Ratio Mismatch
```
⚠️ The generated image doesn't match the selected aspect ratio [ratio].

Expected: [ratio] (e.g., 16:9 = 1280x720)
Actual: [actual dimensions]

This can happen due to model limitations.

Options:
[1] Regenerate (sometimes the model gets it right on retry)
[2] Crop to correct ratio (may lose some content)
[3] Accept current ratio

💡 Tip: 16:9 and 1:1 are the most reliably generated ratios.
   Unusual ratios like 21:9 may occasionally deviate.
```

#### Error: Annotations in Wrong Language
```
⚠️ The annotations appear to be in [wrong language] instead of [expected language].

This can happen when:
- The article contains mixed languages
- The auto-detection was confused by code/numbers

Options:
[1] Regenerate with explicit language declaration
[2] Manually specify: "Use [language] annotations"
[3] Accept current result
```

### 4. System/Environment Issues

#### Error: Image Generation Failed
```
⚠️ Image generation failed.

Error: [specific error message]

Common causes:
- Rate limiting (too many requests in a short time)
- Model temporarily unavailable
- Image size exceeds limits
- Content policy violation (rare)

Options:
[1] Retry after a few seconds (recommended)
[2] Reduce image count and retry
[3] Try a different aspect ratio
[4] Skip this image and continue with the rest

💡 Tip: If you hit rate limits, wait 30 seconds before retrying.
   Generating images one at a time (sequentially) is more 
   reliable than batch generation.
```

#### Error: File Save Failed
```
⚠️ Failed to save image to [path].

Possible causes:
- Directory doesn't exist
- Permission denied
- Disk full

Attempting to save to alternative location: assets/

Options:
[1] Retry save
[2] Save to desktop/user-specified location
[3] Display image directly (no file save)
```

### 5. User Input Errors

#### Error: Invalid Style Name
```
⚠️ "[user input]" is not a recognized style name.

Available styles:
[0] Base Sketch    [5] Ink-Wash Zen
[1] Retro-Tech    [6] Cyber-Neon
[2] Organic Warmth [7] Woodcut Print
[3] Minimal Geometry [8] Clay Stop-Motion
[4] Mixed Media   [9] Glitch Art
[H] Hybrid Mode

Did you mean one of these? Type the number or name.
```

#### Error: Invalid Aspect Ratio
```
⚠️ "[user input]" is not a recognized aspect ratio.

Available ratios:
16:9 | 9:16 | 4:3 | 3:4 | 1:1 | 21:9

Did you mean one of these? Type the ratio or number (1-6).
```

#### Error: Quantity Out of Range
```
⚠️ Please choose between 1 and 9 illustrations.

You entered: [user input]

💡 Guide:
- 1-3: Short articles or focused topics
- 4-6: Standard articles
- 7-9: Long, comprehensive articles

Please enter a number between 1 and 9.
```

## Error Recovery Principles

1. **Never fail silently**: Always explain what went wrong and why
2. **Always provide options**: Give the user 2-3 actionable next steps
3. **Preserve progress**: If one image fails, continue with the rest
4. **Educate**: Use errors as teaching moments (tips and explanations)
5. **Be encouraging**: Errors are normal, not the user's fault
