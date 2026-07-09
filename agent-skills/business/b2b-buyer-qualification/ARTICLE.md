# B2B Buyer Qualification — a portable agent skill for export sellers

Most export sellers have the opposite of a lead problem. They have too many:
inbound inquiries from unknown mailboxes, a spreadsheet of trade-show
contacts, a handful of "distributors" who never shared a website. The real
problem is **prioritization** — deciding who to call, who to verify, and who
to quietly drop.

`b2b-buyer-qualification` is a small, portable agent skill that turns a rough
lead into a one-page buyer brief: who they are, whether they match your offer,
what risks exist, and what to do next.

> This is not a "dig up dirt" tool. It evaluates **fit and priority** from
> public or user-provided information. It does not accuse anyone of fraud.

## Why it exists

A good sales rep already does this work mentally: check the website, see if
they actually sell the category, notice the Gmail address on a "large
distributor," weigh whether the order is real. The problem is that this
judgment is slow, inconsistent, and lives only in someone's head.

The skill makes the process:

- **Repeatable** — same steps every time, not vibes.
- **Evidence-based** — every score point traces to a source.
- **Portable** — plain Markdown an agent can load and follow.
- **Safe** — it marks uncertainty instead of inventing facts.

## What it does

Given a company name (and whatever else you have), the skill produces a
structured **Buyer Qualification Brief**:

- **Verdict** — a 0–100 score, a priority band, and a one-line reason.
- **Company snapshot** — name, domain, market, likely role, categories.
- **Evidence** — the public signals it found (or a clear "no public evidence found").
- **Fit analysis** — product, channel, market, and order potential.
- **Risk check** — legitimacy confidence, risk signals, missing confirmations.
- **Recommended next action** — outreach, verification questions, sample/RFQ response, or "monitor / avoid".
- **Outreach angle** — a short, buyer-specific first message.

## The workflow

1. **Normalize the lead** — pin down the real company entity; mark lookalikes as `Unconfirmed`.
2. **Build an evidence map** — website, catalog, LinkedIn, marketplace, trade-show pages, public reviews. No fabricated shipments, revenue, or contacts.
3. **Evaluate business fit** — product, channel, market, order potential, positioning, timing.
4. **Check legitimacy and risk** — separate normal uncertainty from real red flags. Use `risk signal`, `unverified`, `needs confirmation` — never accuse without strong evidence.
5. **Produce a buyer score** — 100 points, explainable (see rubric).
6. **Recommend the next action** — always one clear, immediate step.

## The scoring rubric

| Dimension | Weight | What it measures |
|---|---:|---|
| Product fit | 25 | They already sell, buy, or distribute related products. |
| Channel & market fit | 20 | Right channel type and a market you can serve. |
| Order potential | 20 | Evidence of scale, catalog breadth, retail reach, or distribution capacity. |
| Legitimacy confidence | 20 | Public evidence supports a real, active company. |
| Outreach readiness | 15 | Enough verified info to contact now — a contact, a clear angle, no blocking gaps. |

**Bands:** `80–100` Strong target · `65–79` Worth outreach · `50–64` Research more · `30–49` Low priority · `0–29` Avoid / verify carefully.

If no public evidence exists, the skill says so and scores mainly on missing
confirmations and legitimacy gaps — it does not invent facts or score down on
assumptions.

## Example

A US outdoor-furniture retailer with a private-label program, 18 stores, a
recent sourcing-manager hire, and a trade-show booth scores ~86 and gets a
"send first outreach" with a private-label angle. An inquiry from a
three-week-old domain, a free Gmail address, and an early request for
WireTransfer bank details scores ~34 and gets "ask verification questions" —
clearly flagged as *unverified*, never called a scam.

See [`EXAMPLES.md`](agent-skills/business/b2b-buyer-qualification/EXAMPLES.md)
for three worked, fictional examples (strong buyer, questionable inquiry, and
batch prioritization).

## Use it with your agent

Copy the folder `agent-skills/business/b2b-buyer-qualification/` into your
project, then reference `SKILL.md`:

- **Codex** — load the `SKILL.md` before acting.
- **Claude Code** — reference it from `CLAUDE.md`, copy into a Claude skills setup, or open `SKILL.md` as context.
- **Cursor** — point Cursor rules / chat context at the folder.
- **Other agents** — read the narrowest matching skill first, then follow its steps.

## Safety & privacy

- Public or user-provided information only.
- No private personal data; no fabricated contacts, shipments, certifications, or financials.
- Legal, sanctions, and compliance issues are signals for professional review, not final conclusions.
- For controlled / restricted / dual-use / medical / chemical goods, do a compliance check before outreach or quotation.

## License

[MIT](LICENSE) — free to use, copy, modify, and ship.
