# The Recon System

Six prompts. Run them in order. Each one feeds the next.

Replace the `[BRACKETS]` with your inputs. This works best in Claude Code with web access on, so it can pull live threads. If your Claude cannot browse, paste in threads you find yourself when a prompt asks for them.

Run all six in a single session so the model keeps context between steps.

---

## Prompt 1 — Watering holes

```
You are a research analyst mapping where a specific buyer gathers online before I build for them.

My customer: [WHO THEY ARE: role, company type, what they do all day]
What I sell or plan to sell: [ONE PARAGRAPH]

Find where these people actually talk to each other.
- The subreddits they live in (rank by how on-target, not by size)
- Other communities: forums, Slack/Discord groups, review sites
- The adjacent communities where they show up that I would not expect

Skip the generic business subs. I want the specific places my buyer complains, asks, and recommends. For each, one line on why it is on-target.
```

---

## Prompt 2 — Voice of customer

```
Go to the watering holes from the previous step.

Pull real threads where my buyer talks about the problem I solve, the tools they use, or what frustrates them.

For each thread:
- Link it
- Quote the exact line that matters, word for word
- Note the emotion behind it (annoyed, resigned, desperate, smug)

I want their language, not a summary. Give me 10-15 quotes I could paste into a doc. Do not clean up how they talk.
```

---

## Prompt 3 — Pain map

```
From the quotes and threads, build a pain map.

List the recurring pains. For each:
- The pain in one line
- How often it shows up (frequent / occasional / rare)
- How much it stings (mild annoyance / real cost / dealbreaker)
- A representative quote

Rank by frequency times intensity. The top of this list is what I lead with. The bottom I ignore.
```

---

## Prompt 4 — Competitor read

```
My buyer already uses something today, even if it is a spreadsheet or nothing.

From the threads, tell me what people actually say about the alternatives:
- Named competitors and what people praise them for
- What people complain about for each
- The workarounds people invent when no tool fits
- The thing every option seems to miss

Quote real lines. I want the gap that shows up across all of them.
```

---

## Prompt 5 — The objection

```
Find the reason my buyer will NOT switch, even when they hate what they have.

From how these people talk:
- What makes them stick with the painful status quo?
- What kills new tools for them (price, trust, switching cost, "good enough")?
- What language do they use when they dismiss something new?

Give me the objection in one sentence, the way my buyer would say it to a colleague.
```

---

## Prompt 6 — The wedge

```
Synthesize everything into a one-page brief.

Include:
- The single sharpest pain to lead with, and the quote that proves it
- The gap no current option fills (my wedge)
- The exact words my buyer uses for this problem (so I can write copy in their language, not mine)
- The objection and the one thing that would overcome it
- The 3 threads worth engaging in honestly (where I could be useful, not salesy)

Keep it to one page. This is the brief I build my messaging from.
```

---

## How to use the output

The voice-of-customer quotes are the most valuable part. Write your landing page, your cold email, your post hooks in their words. Not yours.

Run this fresh per market or per segment. The pain that matters to one buyer is noise to another. That is the point.

One rule: when you engage in the threads, be useful. Answer the question. Do not pitch. The recon only works if you do not poison the well you are reading from.
