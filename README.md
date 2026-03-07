# Daily Works

Automated daily content engine powered by GitHub Actions. Fetches live investment data, curates anime quotes, tech headlines, and Java tips — committed daily to keep the contribution graph active.

## What This Does

| Section | Source | Schedule |
|---------|--------|----------|
| **Investment Snapshot** | BTC, ETH, Gold, Reliance, TCS | Every morning ~6:30 AM IST (never skipped) |
| **Anime Quotes** | 30 curated quotes from top anime | 2-3 times daily |
| **Tech News** | Developer-focused headlines | 2-3 times daily |
| **Java Tips** | Modern Java snippets (10-24) | 2-3 times daily |

## Project Structure

```
.github/workflows/daily-all.yml   # Automation engine
data/investments.json              # BTC, ETH, Gold, Reliance, TCS prices
content/anime-quotes.md            # Daily anime quote log
content/tech-news.md               # Daily tech headline log
content/java-tips.md               # Daily Java tip log
docs/                              # Future: dashboard UI
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
- **Gold**: Spot price (USD/oz) via metals.dev
- **Indian Stocks**: Reliance, TCS (INR) via Yahoo Finance

## Roadmap

- [x] Automated daily commits with varied content
- [x] Live investment snapshot (crypto + stocks + gold)
- [x] Natural commit pattern (skip logic + weekly bursts)
- [ ] Dashboard UI on GitHub Pages (`docs/index.html`)
- [ ] Category selector: quotes carousel, news feed, tip-of-the-day
- [ ] Investment charts with historical price trends
- [ ] Mobile-friendly responsive design

## Tech Stack

- **GitHub Actions** — Cron-based automation
- **Bash + jq + curl** — Data fetching and processing
- **CoinGecko API** — Cryptocurrency prices
- **Yahoo Finance** — Indian stock prices
- **GitHub Pages** — Future UI hosting (zero cost)

---

*Built by Kousik — automated content + investment intelligence feed.*
