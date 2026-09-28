# World's News Refresher (every hour)

Worldwide business news across every industry — markets, tech & AI, retail & fashion, food & beverage, energy, industrials, healthcare, finance & deals, media, real estate — written as one-line bullets.

**Live page:** https://claude.ai/artifact/DwBVguupTdBWZu2qRa5wdF

## How it works

A scheduled Claude task runs every hour (at :08). Each run:

1. Searches the web for new business stories from the last few hours.
2. Adds the ones not already listed, in its own words, with a source link.
3. Drops stories older than 48 hours from the page.
4. Republishes the live page and commits the update to this repo.

## Files

| Path | What it is |
|---|---|
| `business-wire.html` | The page itself. Open it in a browser; the news is in the `news-data` JSON block. |
| `data/news.json` | The current 48-hour feed. |
| `data/archive/YYYY-MM-DD.json` | Every story added on that day (America/Chicago). Kept permanently. |
| `refresh-prompt.md` | The instructions the hourly task follows. |

Summaries are based on public news reports. Not investment advice.
