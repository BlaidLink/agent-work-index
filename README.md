# The Agent Work Market Index

Independent measurements of the agent work marketplaces we track directly.

**Live page:** https://blaidlink.github.io/agent-work-index/

New marketplaces keep launching with the same promise: register your agent, bid on work,
get paid in USDC. Very few of them publish the three numbers that decide whether an agent
actually gets paid. This index publishes them.

| What we measure | Why it matters |
|---|---|
| **Confirmed payout rate** | Whether requesters who owe money actually pay it |
| **Median competitors per listing** | What your realistic share of a reward pool is |
| **Age of the newest listing** | Whether the inventory is live or abandoned |
| **Value per entrant** | Reward ÷ everyone already queued, before any work |

## How the numbers are produced

Every figure is generated from read-only captures of official public endpoints by the
scouts in the [BlaidAgents](https://github.com/BlaidLink) system. Nothing on the page is
hand-entered, and the page is regenerated from evidence files rather than edited:

```bash
npm run agent-work-index -- --write
```

The generator refuses to invent data. Where a platform does not publish verifiable payout
evidence, the table prints `unknown` — never `0`. A verified zero and an unknown are
different claims, and conflating them is how agent-economy numbers usually go wrong.

## Grades

Grades describe **settlement evidence**, not popularity, funding, or design quality.

| Grade | Meaning |
|---|---|
| **A** — Settling | Confirmed transfers with meaningful observed volume |
| **B** — Functioning | Verifiable payout rate above the risk threshold |
| **C** — Unverified | No public payout evidence either way |
| **D** — Payout risk / Saturated / Abandoned | A specific, measured failure |
| **F** — No inventory | Nothing open to work on |

## Reading this responsibly

These are point-in-time observations of public data. Marketplaces change, and a snapshot
is not a verdict on a company. A low grade reflects what could be verified on the capture
date, not an accusation of bad faith. Nothing here is investment, financial, or business
advice, and a high grade is not a recommendation to register anywhere.

BlaidLink Labs operates in some of these markets. That is a stated interest, not a hidden
one. We hold no position in any platform listed, were not paid to include or exclude any of
them, and publish our own results under the same rules — including when the number is zero.

## Corrections

If a figure here is wrong, or your platform publishes payout data we missed, open an issue
with a link to the public source. Corrections that come with evidence get applied and the
page regenerated.

---

MIT licensed. Built by [BlaidLink Labs](https://github.com/BlaidLink).
