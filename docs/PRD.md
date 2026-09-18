# Deal Screener — Mini-PRD (pre-build spec)

Status: spec approved 2026-09-18. Decisions: pasted-text input first (no URL scraping), transparent scoring with the math shown, skeptical-by-default positioning. Code build paused — spec published first.

## Problem
First-time buyers drown in business-for-sale listings with thin or embellished numbers and no pattern recognition to separate fairly priced businesses from money pits. They either analyze everything and burn out, or fall for the first decent listing and overpay.

## Target user
First-time buyers searching for a small business to acquire. Analytical, motivated, but no deal experience. The bar: "can I triage a listing in 10 minutes?"

## Solution
Paste a listing's text. Get back the extracted facts, a 0–100 fit score against your buy criteria with the breakdown visible, the top red flags, and five tailored questions for the broker.

## Demo story
"Marcus wants to buy within 30 minutes of Minneapolis. He pastes three listings…" Show: side-by-side scores, one listing flagged for declining revenue buried in paragraph four, and the question list for the broker call.

## Scope — in for v1
- Paste listing text; extract revenue, cash flow/SDE, asking price, industry, location, years in business, employees
- Buy-criteria input: price range, cash-flow multiple cap, distance, industry preferences, owner-involvement needs
- 0–100 fit score with visible per-factor breakdown
- Top 3 red flags with plain-language explanations
- 5 broker questions tailored to the listing's weak spots

## Scope — out for v1
- URL scraping of listing sites (paste is robust on day one)
- Saved deal pipeline / CRM features
- Automated broker outreach
- Valuation modeling (covered by the Valuation Gut-Check sibling idea)

## What "working" looks like
1. A buyer pastes a real listing and gets a score, flags, and questions in under a minute.
2. Every point of the score traces to a visible reason — no black box.
3. The broker questions reference specific weak spots in that listing.

## Open questions
1. Listing input: paste vs. URL? Proposal: paste for v1, URL scraping later.
2. Should it learn from the buyer's past likes/dislikes? Proposal: v2 — v1 is transparent rules and weights.
3. Multi-listing comparison in v1? Proposal: single-listing scoring first, comparison as a fast follow.

## Initial tradeoffs
- Paste over scrape: robust on day one, slightly more user effort per listing.
- Transparent rules-based scoring over ML: trust beats sophistication when the decision is $500k.
- Skeptical positioning: the tool earns trust by killing bad deals, not by hyping listings.
