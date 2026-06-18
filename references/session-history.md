# Session History & Reuse (历史记录与复用)

## Overview

The skill automatically saves generation parameters and user preferences to `assets/session-history.json` after each successful generation. This enables quick reuse of proven configurations and personalized defaults.

## History File Format

`assets/session-history.json`:

```json
{
  "version": "1.3",
  "last_updated": "2026-06-18T14:30:00Z",
  "sessions": [
    {
      "session_id": "sess_20260618_001",
      "timestamp": "2026-06-18T14:30:00Z",
      "article_title": "光芯片行业深度分析",
      "mode": "context_anchor",
      "aspect_ratio": "16:9",
      "quantity": 6,
      "style": "base_sketch",
      "language": "zh",
      "character_name": "光之搬运工",
      "character_description": "一个由光纤编织而成的人形...",
      "generation_method": "heterogeneous_synthesis"
    }
  ],
  "user_defaults": {
    "preferred_mode": "context_anchor",
    "preferred_aspect_ratio": "16:9",
    "preferred_style": "base_sketch",
    "preferred_language": "auto",
    "expert_mode": false
  },
  "series_characters": {
    "ai_weekly": {
      "series_name": "AI Weekly",
      "character_name": "数据精灵",
      "character_description": "...",
      "created_at": "2026-06-18T10:00:00Z",
      "last_used": "2026-06-18T14:30:00Z",
      "article_count": 3
    }
  }
}
```

## Auto-Save Rules

After each successful generation, append to history:
- Session ID (timestamp-based)
- All generation parameters
- User rating (if provided)


## Reuse Commands

| User Says | Action |
|-----------|--------|
| "Use the same settings as last time" / "和上次一样" | Load last session parameters |
| "Use my default settings" / "用默认设置" | Load `user_defaults` |
| "Save this as my default" / "保存为默认" | Save current params to `user_defaults` |
| "Show my history" / "查看历史" | List last 10 sessions with IDs |
| "Reuse session 3" / "复用第3次" | Load session by index |
| "I liked the character from the AI article" / "喜欢上次AI文章的角色" | Search history by article title/tag |

## Default Parameters

**Default values** (stored in `user_defaults`):
- Mode: Context Anchor
- Aspect Ratio: 16:9
- Quantity: auto-recommended
- Style: Base Sketch
- Language: auto-detect
- Expert Mode: false

## Privacy Note

History is stored locally in `assets/session-history.json`. No data leaves the user's machine. Users can delete the file at any time to clear history.
