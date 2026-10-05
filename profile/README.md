<div align="center">

<img src="https://raw.githubusercontent.com/transhumanists/.github/main/profile.svg" alt="transhumanists" width="460">

# 🧬 transhumanists

### **Human Progress. Quantified.**

[![Live dashboard](https://img.shields.io/badge/live%20dashboard-transhumanists.github.io-7C4DFF?style=for-the-badge&logo=githubpages)](https://transhumanists.github.io)
[![Status](https://img.shields.io/website?down_message=down&up_message=up&url=https%3A%2F%2Ftranshumanists.github.io)](https://transhumanists.github.io)
[![Organization](https://img.shields.io/badge/org-GitHub%20transhumanists-181717?style=for-the-badge&logo=github)](https://github.com/transhumanists)
[![Pipeline](https://img.shields.io/badge/pipeline-every%206%20hours-00E5FF?style=for-the-badge)](https://github.com/transhumanists/apis)

</div>

---

<div align="center">

> ### “The intellectual and cultural movement that affirms the possibility and desirability of fundamentally improving the human condition through applied reason, especially by developing and making widely available technologies to eliminate aging and to greatly enhance human intellectual, physical, and psychological capacities.”
>
> 📖 [**The Transhumanist FAQ**](https://www.humanityplus.org/transhumanist-faq) — Humanity+, formerly the World Transhumanist Association

</div>

<div align="center">

**We are an open, independent watchtower on the breakthroughs that shape the human
condition.** Around eighty sources — Nature, Science, arXiv, IEEE Spectrum, Reuters,
NVD, ISW — are scraped every six hours, scored against a fixed rubric, and pinned to
the place they happened. Free, no login, no paywall.

</div>

---

## 🚀 Come and look at the map

<div align="center">

### 🌐 **[transhumanists.github.io](https://transhumanists.github.io)**

[![The dashboard](https://raw.githubusercontent.com/transhumanists/.github/main/dashboard.svg)](https://transhumanists.github.io)

</div>

One page, no login, no paywall:

| What you will find | Why it is worth a visit |
| --- | --- |
| 🗺 **Interactive world map** | Every record pinned to the place it happened — a fusion lab in Livermore, a launch complex in Boca Chica |
| 🏆 **Category leaderboards** | Who currently holds each record, how big it is, and when it landed |
| 📈 **Activity timeline** | A rolling 30-day view of which fields are accelerating |
| 🔍 **Per-category drill-down** | Ten tracked subcategories per vertical, with sources |
| ⚡ **Live heartbeat** | The dashboard refreshes itself — the pipeline runs every 6 hours |

> The dashboard is the front door. The map, the data and the leaderboards live at
> **[transhumanists.github.io](https://transhumanists.github.io)**.

---

## 🗂 The seven verticals

| # | Vertical | What we watch | Current record holder |
| - | -------- | ------------- | --------------------- |
| 🧬 | [Biotechnology](https://github.com/transhumanists/milestones/blob/main/Milestones.md#1-biotechnology) | Gene editing, implants, microscopy, longevity, synthetic biology, neuroscience | CRISPR in-vivo editing efficiency — 94.2% · Broad Institute |
| 🧠 | [Computing & AGI](https://github.com/transhumanists/milestones/blob/main/Milestones.md#2-computing--agi) | Frontier benchmarks, agentic AI, GPU efficiency, inference cost | MMLU — 94.7% · OpenAI |
| ⚛️ | [Quantum Physics](https://github.com/transhumanists/milestones/blob/main/Milestones.md#3-quantum-physics) | Qubit counts, error correction, time crystals, networking | 4,158 physical qubits · IBM Condor 2 |
| ⚡ | [Renewable Energy](https://github.com/transhumanists/milestones/blob/main/Milestones.md#4-renewable-energy) | Fusion, solar efficiency, battery density, wind, storage | Fusion gain Q = 17.6 · NIF, Livermore |
| 🛡️ | [Cybersecurity](https://github.com/transhumanists/milestones/blob/main/Milestones.md#5-cybersecurity) | Exploits, mitigations, encryption, threat intel, zero-days | Highest active CVSS 10.0 CRITICAL · NVD / CISA |
| 🚀 | [Spaceflight & Aeronautics](https://github.com/transhumanists/milestones/blob/main/Milestones.md#6-spaceflight--aeronautics) | Launch, payload, deep space, hypersonics, reusability | 156 t to LEO · SpaceX |
| 🌍 | [Military & Defense](https://github.com/transhumanists/milestones/blob/main/Milestones.md#7-military--defense) | Range, fleet movements, contracts, air defense, naval, cyber ops | NATO rapid reaction force — 300,000 personnel |

<sub>Snapshot from the last pipeline run. The live values on
[transhumanists.github.io](https://transhumanists.github.io) are always the freshest.</sub>

---

## 🔬 How the map stays honest

```text
80+ RSS feeds → LLM scorer → milestones.json → world map + daily digest
                     ↑
            self-healing source checker
```

Every **6 hours** a GitHub Action runs:

1. **`scrapers/rss_fetcher.py`** — pulls 80+ sources (Nature, Science, arXiv, IEEE Spectrum, Phys.org, Reuters, SpaceNews, The Hacker News, Bellingcat, ISW, NATO, CISA …)
2. **`llm/score_milestone.py`** — sends titles and summaries to a JSON-mode LLM and extracts a structured `{category, subcategory, value, unit, source_url, geolocation}`
3. **`self_healer/source_checker.py`** — validates every feed URL, drops dead ones, finds replacements
4. **`github/dashboard_updater.py`** — regenerates `milestones.json`, `events.json` and `activity.json`, then commits
5. **`social/facebook_poster.py`** — posts the daily digest to [facebook.com/transhumanistsBE](https://facebook.com/transhumanistsBE)

**Every claim on the map keeps its source and its date.** If the source cannot be
reached, the record leaves the map. No score without a citation.

---

## 🤝 Take part

This is a movement, not a committee. There is room for you whether you are a
researcher, a scroller, a skeptic or a builder.

- 📣 **Spotted a record we missed?** [Open an issue](https://github.com/transhumanists/milestones/issues) with the source, the category, the value + unit, and the date. That is the whole checklist.
- 🔧 **Got a feed we should be reading?** Add it — [open an issue on `apis`](https://github.com/transhumanists/apis/issues) or send a PR.
- 💬 **Want to argue about the map?** [Discussions are open](https://github.com/transhumanists/milestones/discussions), and issue trackers are open on every repo below.
- 🔭 **Just want the signal?** Follow the daily digest on [Facebook](https://facebook.com/transhumanistsBE), or bookmark [transhumanists.github.io](https://transhumanists.github.io) and come back when a vertical moves.
- 💖 **Want to pay for the scrapers?** The 6-hourly pipeline runs on LLM API and hosting costs — [sponsor it](https://github.com/sponsors/neohiro).

**Our ground rules**, borrowed from [The Transhumanist Declaration](https://www.humanityplus.org/the-transhumanist-declaration):
autonomy and wide personal choice over how you enable your life · the well-being of all
sentience · progress pursued with responsibility · reduction of existential risk as an
urgent priority. Curiosity, not certainty, is the entry fee.

---

## 🧩 Repositories

| Repo | What it holds |
| --- | ------------- |
| [`transhumanists.github.io`](https://github.com/transhumanists/transhumanists.github.io) | The live world-map dashboard at [transhumanists.github.io](https://transhumanists.github.io) |
| [`milestones`](https://github.com/transhumanists/milestones) | Canonical milestone database — `Milestones.md` plus `data/*.json` |
| [`apis`](https://github.com/transhumanists/apis) | RSS scraper, LLM scorer, self-healer, dashboard updater, Facebook poster |
| [`.github`](https://github.com/transhumanists/.github) | Organization profile, community health files and the cross-profile branding SVGs |

---

## 🌐 Part of the neohiro network

| Site | What it is |
| --- | ---------- |
| **[transhumanists.github.io](https://transhumanists.github.io)** | Human progress, quantified — *this is us* |
| **[frenzypenguin.media](https://frenzypenguin.media)** | 🎛️ FrenzyPenguin Media — the studio: artist videos, livestreams, captation, art visuals |
| **[openstageisland.github.io](https://openstageisland.github.io)** | 🏝️ Open Stage Island — a free 24/7 open-air music stage in Second Life |
| **[github.com/neohiro](https://github.com/neohiro)** | 👽 The developer account — open-source hardening and privacy tooling |

---

<div align="center">

[![Sponsor on GitHub](https://img.shields.io/badge/Sponsor%20on%20GitHub-%E2%9D%A4-EA4AAA?logo=githubsponsors&style=for-the-badge)](https://github.com/sponsors/neohiro)&nbsp;&nbsp;
[![Patreon](https://img.shields.io/badge/Patreon-frenzypenguin__media-F96854?logo=patreon&style=for-the-badge)](https://www.patreon.com/frenzypenguin_media)&nbsp;&nbsp;
[![Linktree](https://img.shields.io/badge/Links-frenzypenguin.media-2BE295?logo=linktree&logoColor=white&style=for-the-badge)](https://linktr.ee/frenzypenguin.media)&nbsp;&nbsp;
[![Visitors](https://api.visitorbadge.io/api/visitors?path=github.com%2Ftranshumanists&label=Visitors&countColor=%23263759)](https://visitorbadge.io/status?path=github.com%2Ftranshumanists)

---

Made with ♥ by **[FrenzyPenguin Media](https://frenzypenguin.media)** —
a [neohiro](https://github.com/neohiro) project · powered by [`transhumanists/apis`](https://github.com/transhumanists/apis)

</div>