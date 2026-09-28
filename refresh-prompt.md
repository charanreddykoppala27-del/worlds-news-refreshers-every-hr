# Hourly refresh instructions

This is what the scheduled task does every hour. Kept here for reference; the live copy lives in the scheduled task's settings.

1. Read the live page (https://claude.ai/artifact/DwBVguupTdBWZu2qRa5wdF). The news lives only in the JSON inside `<script id="news-data" type="application/json">`.
2. Search 8–12 angles of worldwide business news from the last few hours: markets & macro (US, Europe, Asia), tech & AI, retail & fashion, food & beverage, energy & commodities, industrials & autos, healthcare & pharma, finance & M&A, media & entertainment, real estate. Prefer original reporting.
3. Add only stories not already listed. Each item: `t` (ISO timestamp), `cat` (category), `text` (1–2 sentences in original wording, with numbers and company names), `src` (outlet), `url` (article link).
4. Drop items older than 48 hours; set `updated` to now.
5. Republish the live page.
6. In this repo: write `business-wire.html`, `data/news.json`, append the hour's new items to `data/archive/YYYY-MM-DD.json`, commit as `News update <date time CT> (+N items)`, push to `main`.
