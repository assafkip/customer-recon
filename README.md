# customer-recon

A threat-intelligence approach to knowing your market. Runs in Claude Code, reads what your buyers actually say on Reddit, and links every quote.

I spent 12 years doing threat intelligence. The work was reconnaissance. Build a picture of a target from what they say in the open, before you make contact.

Knowing your customer is the same work.

Most founders research the market by reading their own assumptions back to themselves. That is a mirror, not research.

Your buyers are already talking. On Reddit, in the threads where they complain about the tools they pay for. They use specific words. They name the thing they hate. It is public.

So stop guessing. Run recon.

## The rule that matters

This reads real Reddit threads through the Reddit tools and links every quote. It does not invent sentiment or paraphrase a "people say" without a source. If the tools come back empty, it tells you. A gap is intel. A made-up quote is a liability.

This is why it runs in Claude Code with a real Reddit connection, not a chat box. A plain chat cannot reach Reddit, so it guesses, and you cannot tell. The grounding is the product.

## What it produces

- **Where your buyers live.** The subreddits they actually gather in, ranked.
- **Voice of customer.** Real quotes, linked, in their words.
- **Pain map.** Recurring pains ranked by how often and how hard they hit.
- **Competitor read.** What people say about the alternatives, and the gap across all of them.
- **The objection.** Why they will not switch, even when they hate what they have.
- **The wedge.** The gap nobody fills, and the exact language to use.

## Setup (one time)

1. You need a paid Claude plan (Pro or higher). Claude Code lives inside the Claude desktop app and will not open on free Claude.
2. Download the Claude desktop app from claude.com/download, install, and sign in. Click the Code tab. Choose "Local", click "Select folder", pick a new empty folder. That is where your reports save. (Windows: Git must be installed.)
3. Install `uv` (the Reddit connection runs through it). This is the one Terminal step:
   - Mac/Linux: `curl -LsSf https://astral.sh/uv/install.sh | sh`
   - Windows: `powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"`
4. Install this plugin:
   ```
   /plugin install github:assafkip/customer-recon
   ```

## Use it

Run `/customer-recon` in any Claude Code session. It asks about your market, finds the threads, and writes a linked report.

## Who built this

I build custom AI systems for founders and small teams. This is the free, lighter version of the work I do paid. If you want market recon wired into your GTM, or a different operational problem an AI system should handle, reach me at assaf@askconsulting.io.

## License

MIT. See [`LICENSE`](LICENSE).
