# CampaignIQ — AI Marketing Analytics

> Paste your campaign data. Get Claude-powered insights, budget recommendations, and ad copy in seconds.

![Built with Claude API](https://img.shields.io/badge/Built%20with-Claude%20API-00e5a0?style=flat-square)
![No Framework](https://img.shields.io/badge/Stack-Vanilla%20JS%20%2F%20HTML-7c6dfa?style=flat-square)
![No Backend](https://img.shields.io/badge/Backend-None-ff6b35?style=flat-square)

---

## What it does

Most marketing teams still pull CSVs into spreadsheets, manually calculate ROAS and CPA per channel, then write performance summaries by hand. This takes hours.

CampaignIQ replaces that entire workflow with a single AI call.

Enter your spend, impressions, clicks, conversions, and revenue across any channels. Add context about your brand, goal, and audience. Claude analyzes everything and returns:

- **The single most important finding** from your data — no fluff
- **Top performing channel** with a clear explanation of why it's winning
- **Biggest waste** and what to do about it immediately
- **Specific budget reallocation** with dollar amounts or percentages
- **One quick win** you can execute this week
- **Channel performance scores** (0–100) with Scale / Hold / Cut / Test recommendations
- **Ready-to-use ad copy** for your best channel — headline, body, CTA

---

## Demo

| Input | Output |
|---|---|
| Multi-channel campaign data (any channels) | Key insight + channel rankings |
| Brand, goal, audience context | Budget reallocation recommendation |
| Optional competitive/seasonal notes | Live-generated ad copy |

**Live metrics update as you type** — total spend, total revenue, and blended ROAS are calculated in real time before you even run the AI analysis.

---

## How to use it

This is a single self-contained HTML file. No install, no server, no dependencies.

**Option 1 — Run locally:**
```bash
git clone https://github.com/YOUR_USERNAME/ai-marketing-tools
open ai-marketing-analyst.html
```

**Option 2 — Host it anywhere:**
Drop the HTML file into any static host (GitHub Pages, Netlify, Vercel). It works immediately.

**Option 3 — Just open the file:**
Download `ai-marketing-analyst.html` and open it in any browser. Done.

The tool calls the Anthropic Claude API directly from the browser. No API key is required in this portfolio version — it uses the session credentials provided by the Claude.ai environment.

> To deploy independently, add your Anthropic API key to the fetch headers in the script block.

---

## The workflow this replaces

**Before (manual process — ~3 hours):**
1. Export channel data from each ad platform
2. Consolidate into a spreadsheet
3. Calculate ROAS, CPA, CTR, CVR per channel manually
4. Write a performance summary
5. Draft budget reallocation recommendations
6. Write new ad copy based on findings

**After (with CampaignIQ — ~60 seconds):**
1. Paste numbers into the table
2. Add one sentence of context
3. Hit Analyze

Same output. Better reasoning. Faster decisions.

---

## Stack

| Layer | Choice | Why |
|---|---|---|
| AI | Claude API (`claude-sonnet-4`) | Best reasoning on nuanced marketing tradeoffs |
| Frontend | Vanilla HTML/CSS/JS | Zero dependencies, runs anywhere, instant load |
| Fonts | Syne + DM Sans + DM Mono | Distinctive — not another Inter/Inter/Inter stack |
| Backend | None | Single file, fully client-side |

---

## What I learned building this

**Prompt structure matters more than prompt length.** The first version returned verbose markdown paragraphs that were hard to parse into UI components. Switching to strict JSON output with a schema defined in the prompt made the responses deterministic and immediately renderable — no post-processing needed.

**Calculated context beats raw data.** Passing pre-computed metrics (ROAS, CPA, CTR, CVR) alongside the raw numbers gave Claude significantly sharper recommendations than raw numbers alone. The model reasons better when the math is already done.

**Marketing AI tools need specificity to be useful.** Generic "improve your campaigns" advice is worthless. Forcing the model to name specific channels, specific dollar amounts, and a specific action this week made the output immediately actionable rather than consultancy-speak.

---

## What's next

- [ ] CSV upload / paste support (skip manual entry)
- [ ] Multi-period comparison (this month vs last month)
- [ ] Export to PDF report
- [ ] Slack/email summary delivery via Zapier webhook
- [ ] Saved campaign history (localStorage)

---

## About this project

Built as part of a portfolio demonstrating practical AI integration for marketing teams — specifically the kind of workflow automation relevant to roles at gaming and creator-focused brands (CORSAIR, Elgato, Logitech G, Razer, etc.).

The goal isn't to replace marketing analysts. It's to eliminate the 80% of their time spent on data wrangling so they can focus on the 20% that actually requires human judgment.

---

*Built with Claude API · Single HTML file · No backend required*
