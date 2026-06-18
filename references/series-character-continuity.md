# Series Character Continuity (系列文章角色延续)

## Overview

When a user writes a series of articles on the same theme, they can save a Context Anchor character for reuse across multiple articles. This creates a "temporary brand anchor" — brand consistency within the series, but freedom to change for new topics.

## Workflow

### Step 1: Save Series Character

After generating images for Article 1, user says:
- "Save this character for the series" / "保存这个角色用于系列文章"
- "Make this my AI Weekly character" / "设为我的AI周报角色"

The skill saves to `assets/session-history.json` → `series_characters`:

```json
{
  "series_characters": {
    "ai_weekly": {
      "series_name": "AI Weekly",
      "character_name": "数据精灵",
      "character_description": "完整角色描述...",
      "generation_method": "heterogeneous_synthesis",
      "created_from_article": "光芯片行业深度分析",
      "created_at": "2026-06-18T10:00:00Z",
      "last_used": "2026-06-18T10:00:00Z",
      "article_count": 1,
      "max_articles": 10
    }
  }
}
```

### Step 2: Reuse in Subsequent Articles

For Article 2, user says:
- "Use my AI Weekly character" / "用AI周报的角色"
- "Continue with the series character" / "延续系列角色"

The skill loads the saved character and uses it directly, skipping the character confirmation step.

### Step 3: Series Management

| User Command | Action |
|--------------|--------|
| "List my series characters" / "列出系列角色" | Show all saved series characters |
| "Update AI Weekly character" / "更新AI周报角色" | Modify description and regenerate |
| "Retire AI Weekly character" / "退役AI周报角色" | Mark as inactive (keep for archive) |
| "Clone AI Weekly character for new series" / "克隆角色到新系列" | Copy character to new series ID |

## Rules

1. **Series Scope**: A series character is tied to a user-defined series name, not automatic topic detection
2. **Character Evolution**: User can request minor updates ("make the character look more tired this week") while keeping core features
3. **Article Limit**: Default max 10 articles per series character. After that, prompt user to refresh or retire
4. **Cross-Series**: Characters from different series cannot mix unless user explicitly clones
5. **Brand Anchor vs Series Character**:
   - Brand Anchor: Permanent, across ALL content, stored in `assets/ip-reference/`
   - Series Character: Temporary, within ONE series, stored in `session-history.json`

## Comparison

| Feature | Brand Anchor | Series Character | Context Anchor (per article) |
|---------|-------------|------------------|------------------------------|
| Scope | All content | One series | One article |
| Persistence | Permanent | Semi-permanent (configurable) | Temporary |
| Storage | `assets/ip-reference/` | `session-history.json` | In-session only |
| User Confirmation | None (auto-use) | None (series mode) | Required every time |
| Flexibility | Low | Medium | High |
| Best For | Personal IP, brand | Column series, newsletters | One-off articles |
