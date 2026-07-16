---
name: customer-recon
description: Recon on a market by reading what buyers actually say on Reddit. Finds where they gather, pulls real threads and verbatim quotes with links, maps the recurring pains, reads the competitors, finds the objection that keeps them stuck, and names the wedge. Every quote links to a real thread. Use to understand a market, validate a product, or write copy in the customer's own words.
argument-hint: "[market-or-product]"
allowed-tools: Bash, Write, Read, Glob
---

# Customer Recon

Read the market the way an analyst reads a target. People tell the truth when they think they are talking to each other, not to you. A complaint thread is more honest than any survey.

## The rule that matters

This uses real Reddit data through the canonical Reddit tooling (reddit-build-radar's arctic-shift/pullpush mirror — a script/ingestion path, NOT an MCP). It does not invent quotes, threads, or sentiment.

- Every quote must come from a real thread you pulled, with a link. No paraphrased "people say" without a source.
- If a search returns nothing, say so. Gaps are intel. Do not pad.
- Distinguish a widely-held view (many threads) from a one-off complaint (one person).
- If the canonical Reddit tooling is unavailable or blocked, STOP and tell the user. Do not fall back to guessing what the market thinks.

## Step 1: Intake

Ask the user and wait:

1. **Your market or product.** Who is the buyer (role, what they do), and what you sell or plan to sell.
2. **Keywords** your buyers use for this space.
3. **Competitors** to track, if any.
4. **Known communities** where they gather, if any (you will find more).

If passed as `$ARGUMENTS`, use it as a starting point but still confirm.

## Step 2: Find the watering holes

1. Fetch threads for the product/market terms and top keywords via the canonical Reddit tooling (reddit-build-radar arctic-shift/pullpush), sorted by relevance then top. Run up to 5 searches.
2. From results, identify the 5-8 subreddits where real discussion happens.
3. Pull recent posts from the top subreddits (same canonical tooling) to gauge activity.
4. Fetch threads for each competitor name if provided (same canonical tooling).

**Checkpoint:** Tell the user which subreddits look most active, how many relevant threads you found, and any surprise communities. Ask before the deep dive.

## Step 3: Deep dive (real threads, real quotes)

1. Search the top 3-5 subreddits for pain keywords, the product name, and competitor comparisons via the canonical Reddit tooling (reddit-build-radar arctic-shift/pullpush).
2. For the 5-10 highest-signal threads, fetch the full comment thread via reddit-build-radar (arctic-shift/pullpush).
3. Pull verbatim quotes. Keep the link with each one. Do not clean up how people talk.

## Step 4: Synthesis

Build, each item linked to its source:

- **Voice of customer.** 10-15 real quotes, each with a link and the emotion behind it.
- **Pain map.** Recurring pains ranked by frequency times intensity, each with a representative quote.
- **Competitor read.** What people praise and complain about for each alternative, plus the workarounds. The gap that shows up across all of them.
- **The objection.** The reason buyers will not switch even when they hate what they have, in their words.
- **The wedge.** The gap nobody fills, and the exact language buyers use (so the user writes copy in their words, not their own).

## Step 5: Report

Write to `output/customer-recon-YYYY-MM-DD.md` (create `output/` if needed):

1. Executive summary, 3-5 bullets.
2. Where your buyers live (subreddits ranked, with activity).
3. Voice of customer (quotes + links).
4. Pain map (ranked).
5. Competitor landscape.
6. The objection.
7. The wedge and the buyer's own language.
8. Threads worth engaging honestly (link + why + angle, not a script).
9. What you could not find (gaps as intel).

Every finding links to a real thread. Tell the user where it saved.

## Rules recap

- Public Reddit data only, every quote linked.
- A real "nothing found" beats invented sentiment.
- Many threads = a pattern. One thread = a data point. Say which.
- Tools down or blocked: stop and say so. Never guess the market.
- When the user engages in threads: be useful, do not pitch. Do not poison the well you are reading from.
