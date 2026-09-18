# 🔍 Deal Screener

> Paste in a business-for-sale listing, get a fit score. Deal Screener reads the listing like a skeptical analyst — checking it against your buy criteria, flagging red flags, and telling you what to ask the broker before you waste a weekend on it.

🚧 **Status: building in the open, spec first.** The full product spec lives below. Working code is coming next — the thinking is published before the code.

## The Problem

Buying a small business starts with drowning in listings. BizBuySell, BizQuest, brokers — hundreds of listings, most with thin or embellished numbers. A first-time buyer has no pattern recognition: they can't tell a fairly priced $400k-revenue plumbing company from a money pit with "huge upside potential." So they either analyze everything and burn out, or fall in love with the first decent listing and overpay.

## The Solution

Paste a listing's text. Deal Screener extracts the key facts (revenue, cash flow, asking price, industry, location, years in business), scores the deal against your personal buy criteria, and hands you three things: a fit score, the biggest red flags, and five questions to ask the broker. Ten minutes per listing instead of a lost weekend.

## Planned Demo

"Marcus wants to buy a business within 30 minutes of Minneapolis. He pastes three listings…"

The demo will show three listings scored side by side — one flagged for declining revenue the listing buried in paragraph four — and the tailored question list he'd take into the broker call.

## How It Will Work

- **Listing parser** — extracts structured facts from pasted listing text: revenue, SDE/cash flow, asking price, industry, location, years in business, employee count.
- **Fit scoring** — your criteria (price range, cash-flow multiple cap, distance, industry likes/dislikes, owner-involvement needs) weighted into a 0–100 score, with the math shown.
- **Red-flag detector** — declining revenue trends, vague financials, absentee-owner claims that don't match the numbers, multiples way off market.
- **Broker question generator** — five sharp questions aimed at each listing's weak spots.

## Decisions So Far

- **Pasted text first, URL scraping later.** Scraping listing sites breaks constantly; paste works everywhere on day one.
- **Score with the math shown.** A black-box score earns no trust on a $500k decision — every point must trace to a visible reason.
- **Skeptical by default.** The tool's job is to talk the buyer *out* of bad deals, not to sell them on listings.

## Roadmap

- [x] Product spec (this README)
- [ ] Working demo — paste a listing, get a score
- [ ] Saved buy-criteria profiles (score every listing against your thesis)
- [ ] Side-by-side comparison of multiple listings
- [ ] Exportable broker question packs for calls

## Built With (planned)

Plain HTML/CSS/JS — no build step, no backend, no API keys for the demo. A zero-cost, zero-friction portfolio demo.

## Why This Exists

Part of a build-in-public series: practical AI tools for the "silver tsunami" — the wave of small businesses changing hands as baby-boomer owners retire. This one is the front end of the acquisition: finding the deals worth your weekends.
