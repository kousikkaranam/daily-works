# Daily Works

Automated daily content engine powered by GitHub Actions. Fetches live investment data, curates anime quotes, tech headlines, and Java tips — committed daily to keep the contribution graph active.

## What This Does

| Section | Source | Schedule |
|---------|--------|----------|
| **Investment Snapshot** | Top 3 Indian + International stocks, BTC, ETH, Gold | Every morning ~6:30 AM IST (never skipped) |
| **Anime Quotes** | 30 curated quotes from top anime | 2-3 times daily |
| **Tech News** | Developer-focused headlines | 2-3 times daily |
| **Java Tips** | Modern Java snippets (10-24) | 2-3 times daily |

## Project Structure

```
.github/workflows/daily-all.yml   # Automation engine
data/investments.json              # Dynamic stocks, crypto, gold prices
content/anime-quotes.md            # Daily anime quote log
content/tech-news.md               # Daily tech headline log
content/java-tips.md               # Daily Java tip log
docs/index.html                    # Live glassmorphism dashboard
```

## Schedule

- **6:30 AM IST** — Morning investment snapshot (always runs)
- **7:50 AM IST** — Content update (30% skip chance)
- **2:20 PM IST** — Content update (30% skip chance)
- **8:45 PM IST** — Content update (30% skip chance)
- **Saturday 10:30 AM IST** — Weekly burst (4-5 commits)

## Investment Data

Live prices fetched every morning before markets open:

- **Crypto**: Bitcoin (USD), Ethereum (USD) via CoinGecko
- **Gold**: Price in INR/10g via gold-api.com + exchange rate
- **Indian Stocks**: Top 3 most active (dynamic, INR) via Yahoo Finance
- **International Stocks**: Top 3 most active (dynamic, USD) via Yahoo Finance

## Dashboard

Live dashboard at `docs/index.html` (GitHub Pages):

- Dynamic stock cards with country flags (🇮🇳 Indian / 🌍 International)
- BTC, ETH, Gold cards with sparkline history charts
- Glass navigation for Anime & Java: `◀ 3/48 ▶ ✨ Shuffle`
- Glassmorphism UI with animated background glow
- Pill toggle between Investments and Content views

## Roadmap

- [x] Automated daily commits with varied content
- [x] Live investment snapshot (crypto + stocks + gold)
- [x] Natural commit pattern (skip logic + weekly bursts)
- [x] Dashboard UI on GitHub Pages (`docs/index.html`)
- [x] Category selector: quotes carousel, news feed, tip-of-the-day
- [x] Investment charts with historical price trends
- [x] Glass navigation with shuffle for Anime & Java

## Tech Stack

- **GitHub Actions** — Cron-based automation
- **Bash + jq + curl** — Data fetching and processing
- **CoinGecko API** — Cryptocurrency prices
- **Yahoo Finance** — Dynamic top stocks (India + International)
- **GitHub Pages** — Glassmorphism dashboard (zero cost)

---

*Built by Kousik — automated content + investment intelligence feed.*
