<!-- transhumanists / org profile -->

<div align="center">

# 🧬 transhumanists

### **Human Progress. Quantified.**

Tracking breakthroughs in **biotechnology, AGI, quantum physics, renewable energy, cybersecurity, spaceflight, and defense** — scraped, scored, and pinned on a live world map.

</div>

---

## 📊 The Dashboard

<div align="center">

[![Dashboard](https://raw.githubusercontent.com/transhumanists/.github/main/dashboard.svg)](https://transhumanists.github.io)

</div>

The world map and full dashboard live at:

🌐 **[transhumanists.github.io](https://transhumanists.github.io)** — interactive world map, leaderboards, activity timeline, per-category drill-down.

---

## 🗂 The 7 Categories

| # | Category | Top Score | Leader | When |
|---|----------|-----------|--------|------|
| 🧬 | [Biotechnology](https://github.com/transhumanists/milestones/blob/main/Milestones.md#1-biotechnology) | 94.2% (CRISPR in-vivo) | Broad Institute | 2026-08-25 |
| 🧠 | [Computing & AGI](https://github.com/transhumanists/milestones/blob/main/Milestones.md#2-computing--agi) | 94.7% MMLU | OpenAI GPT-6 | 2026-08-19 |
| ⚛️ | [Quantum Physics](https://github.com/transhumanists/milestones/blob/main/Milestones.md#3-quantum-physics) | 4,158 qubits | IBM Condor 2 | 2026-08-22 |
| ⚡ | [Renewable Energy](https://github.com/transhumanists/milestones/blob/main/Milestones.md#4-renewable-energy) | Q=17.6 (fusion gain) | NIF Livermore | 2026-08-20 |
| 🛡️ | [Cybersecurity](https://github.com/transhumanists/milestones/blob/main/Milestones.md#5-cybersecurity) | CVSS 10.0 (CISA) | NVD | 2026-08-24 |
| 🚀 | [Spaceflight](https://github.com/transhumanists/milestones/blob/main/Milestones.md#6-spaceflight--aeronautics) | 156t to LEO | SpaceX | 2026-08-23 |
| 🌍 | [Defense](https://github.com/transhumanists/milestones/blob/main/Milestones.md#7-military--defense) | 15,000 km ICBM | USAF | 2026-07-01 |

---

## 🔬 The Pipeline

1. **[`transhumanists/apis`](https://github.com/transhumanists/apis)** — RSS scraper engine + LLM milestone-scorer + self-healing checker
2. **[`transhumanists/milestones`](https://github.com/transhumanists/milestones)** — Categorized milestone database (`Milestones.md`, `data/milestones.json`, `data/events.json`)
3. **[`transhumanists/transhumanists.github.io`](https://github.com/transhumanists/transhumanists.github.io)** — Live world map dashboard
4. **`.github`** — This profile + cross-profile branding SVGs

Every 6 hours, a GitHub Action runs:
- `scrapers/rss_fetcher.py` — pulls 80+ sources (Nature, Science, arXiv, IEEE Spectrum, Phys.org, Reuters, SpaceNews, The Hacker News, Bellingcat, ISW, NATO, CISA, ...)
- `llm/score_milestone.py` — sends titles + summaries to a JSON-mode LLM, extracts structured `{category, subcategory, value, unit, source_url, geolocation}`
- `self_healer/source_checker.py` — validates RSS URLs, removes dead ones, finds replacements
- `social/facebook_poster.py` — calls Meta Graph API to post to [`facebook.com/transhumanistsBE`](https://facebook.com/transhumanistsBE)
- `github/dashboard_updater.py` — regenerates `data/milestones.json`, `data/activity.json`, `data/events.json`, then commits + pushes

---

## 🔗 Cross-Profile Branding

All SVGs across the transhumanists, FrenzyPenguin Media, and neohiro readmes/profile pages share a uniform design system: dark background, JetBrains Mono + Space Grotesk typography, color-coded category dots, and a tiny **`FrenzyPenguin Media`** watermark in the bottom-right corner that links back to [frenzypenguin-media.github.io](https://frenzypenguin-media.github.io).

---

<div align="center">

Made with ♥ by **[FrenzyPenguin Media](https://frenzypenguin-media.github.io)**

A [neohiro](https://github.com/neohiro) project · Powered by neohiro/apis

</div>
