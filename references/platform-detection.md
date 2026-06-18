# Platform Keyword Detection (平台关键词检测)

## Overview

Quick Mode auto-detects the optimal aspect ratio from platform keywords mentioned by the user. This document defines the keyword-to-ratio mapping rules.

## Detection Rules

| Platform Keywords | Detected Aspect Ratio | Confidence |
|:---|:---|:---:|
| **小红书 / Xiaohongshu / 小红书图文 / 红薯** | 3:4 (vertical, social media graphics) | High |
| **抖音 / Douyin / TikTok / 短视频 / 手机壁纸** | 9:16 (vertical, short video) | High |
| **公众号 / 微信 / WeChat / 订阅号 / 朋友圈** | 16:9 (horizontal, article body) | High |
| **博客 / Blog / Medium / 文章配图 / 正文** | 16:9 (horizontal, default) | High |
| **PPT / 课件 / 幻灯片 / 演示 / 报告** | 4:3 (horizontal, presentation) | High |
| **Instagram / IG /  ins** | 1:1 (square, feed) or 9:16 (Reels) | Medium |
| **YouTube / 油管 / 视频封面** | 16:9 (horizontal, video thumbnail) | High |
| **B站 / Bilibili / 哔哩哔哩 / 头图** | 21:9 (ultra-wide, banner) | High |
| **横幅 / Banner / 网站封面 / 首页** | 21:9 (ultra-wide) | High |
| **头像 / Avatar / 社交 / 产品图** | 1:1 (square) | High |
| **Instagram Reels / YouTube Shorts / 竖版视频** | 9:16 (vertical) | High |

## Fallback Logic

1. If multiple platform keywords are detected, use the **first mentioned** platform's ratio.
2. If no platform keyword is detected, default to **16:9**.
3. If the user explicitly specifies a ratio (e.g., "use 4:3"), override auto-detection.

## Multi-Language Support

Keywords are matched in all supported languages:
- **Chinese**: 小红书, 抖音, 公众号, PPT, 博客, B站, 横幅, 头像
- **English**: Xiaohongshu, TikTok, Douyin, WeChat, Blog, PPT, Instagram, YouTube, Bilibili, Banner, Avatar
- **Japanese**: 小红书, TikTok, ブログ, Instagram, YouTube
- **Korean**: 샤오홍슈, 틱톡, 블로그, 인스타그램, 유튜브
