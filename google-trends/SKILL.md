---
name: google-trends
description: Monitor Google Trends hot searches across different regions and time periods. Use when user wants to track trending topics in US, Hong Kong, Taiwan, Japan, Korea, or other countries. Supports 4-hour and 24-hour timeframes.
---

# Google Trends Monitor

## Quick Start

Use browser to fetch Google Trends data:

```bash
# URL format: https://trends.google.com/trending?geo={REGION}&sort=search-volume&hours={HOURS}
```

## Supported Regions

| Region | Code | URL |
|--------|------|-----|
| 🇺🇸 美国 | US | trends.google.com/trending?geo=US |
| 🇭🇰 香港 | HK | trends.google.com/trending?geo=HK |
| 🇹🇼 台湾 | TW | trends.google.com/trending?geo=TW |
| 🇯🇵 日本 | JP | trends.google.com/trending?geo=JP |
| 🇰🇷 韩国 | KR | trends.google.com/trending?geo=KR |
| 🇬🇧 英国 | GB | trends.google.com/trending?geo=GB |
| 🇦🇺 澳大利亚 | AU | trends.google.com/trending?geo=AU |
| 🇨🇦 加拿大 | CA | trends.google.com/trending?geo=CA |

## Time Range

| Hours | Parameter |
|-------|-----------|
| 4小时 | hours=4 |
| 24小时 | hours=24 |
| 48小时 | hours=48 |
| 7天 | hours=168 |

## Full URL Examples

- 美国 4小时: `https://trends.google.com/trending?geo=US&sort=search-volume&hours=4`
- 香港 24小时: `https://trends.google.com/trending?geo=HK&sort=search-volume&hours=24`
- 台湾 48小时: `https://trends.google.com/trending?geo=TW&sort=search-volume&hours=48`
- 日本 7天: `https://trends.google.com/trending?geo=JP&sort=search-volume&hours=168`
- 韩国 24小时: `https://trends.google.com/trending?geo=KR&sort=search-volume&hours=24`

## Usage

1. Use browser tool to open the URL:
   ```
   browser action=open profile=openclaw targetUrl="https://trends.google.com/trending?geo=US&sort=search-volume&hours=4"
   ```

2. Wait for page load, then get snapshot:
   ```
   browser action=snapshot targetId={targetId}
   ```

3. Parse the results from the snapshot to extract trending topics

4. **IMPORTANT**: Close the browser tab after use to avoid accumulation:
   ```
   browser action=close targetId={targetId}
   ```

## Workflow

1. Open browser to the Google Trends URL
2. Take snapshot
3. Extract top 25 trending items with:
   - Topic name
   - Search volume
   - Percentage change
   - Time started
   - Status (active/ended)
4. **Close the tab**
