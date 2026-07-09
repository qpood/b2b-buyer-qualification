---
name: b2b-buyer-qualification
description: Research and qualify B2B export buyers, distributors, importers, and trade leads before outreach or follow-up.
---

# B2B Buyer Qualification

Use this skill when the user needs to research, verify, score, or prioritize a potential B2B buyer, importer, distributor, wholesaler, retailer, sourcing agent, or trade lead for an export business.

This skill turns a rough lead into a practical buyer brief: who they are, what they sell or buy, whether they match the supplier, what risks exist, and what outreach angle to use next.

This file stays in English so any agent can load it. See `EXAMPLES.md` for worked, fictional examples.

## Good use cases

- Qualify a company before sending an outreach email.
- Check whether an inbound inquiry looks legitimate.
- Compare several potential buyers and decide who to contact first.
- Prepare for a sales call, trade show meeting, RFQ, or sample discussion.
- Build a short account brief for a salesperson or founder.

## Inputs

Ask for the minimum missing information only:

- buyer company name
- website or marketplace profile, if available
- country or target market
- product category the user sells
- known contact name, email, or social profile, if available
- the user's goal: outreach, verification, meeting prep, RFQ review, or prioritization

If the user has a list of companies, process them in a table and keep the output compact.

## Core workflow

### 1) Normalize the lead

Identify the likely company entity before evaluating it.

Check:

- official company name
- website domain
- country and city
- company type: importer, distributor, retailer, brand owner, wholesaler, manufacturer, agent, or unknown
- product category and market positioning
- obvious duplicate names or lookalike companies

If the identity is uncertain, mark it as `Unconfirmed` and explain what evidence is missing.

### 2) Build an evidence map

Collect only evidence that helps business judgment.

Useful evidence:

- official website pages
- product catalog or category pages
- about/company profile pages
- LinkedIn company page or employee signals
- marketplace profiles
- import/export databases when the user provides access
- trade show exhibitor pages
- public reviews, complaints, or legal notices
- email domain and contact consistency

Avoid pretending certainty from weak sources. Do not invent shipment history, revenue, employee count, certifications, or contacts.

### 3) Evaluate business fit

Score the company against the user's export offer.

Fit dimensions:

- **Product fit**: Do they already sell, buy, or distribute related products?
- **Channel fit**: Are they the right channel type for the user's goal?
- **Market fit**: Are they active in a country or segment the user can serve?
- **Order potential**: Is there evidence of scale, catalog breadth, retail reach, or distribution capacity?
- **Positioning fit**: Do their price level, quality level, brand style, and customer base match the user's product?
- **Timing fit**: Is there a current trigger such as new category expansion, trade show activity, hiring, or recent product launch?

Use plain reasoning. Do not over-score because a company simply exists.

### 4) Check legitimacy and risk

Separate normal uncertainty from real red flags.

Common red flags:

- no official website or only a thin landing page
- free email address for a supposedly established company
- mismatched company name, domain, address, or contact identity
- copied content, broken pages, or generic stock-heavy site
- unrealistic order request without company context
- pressure for unusual payment, samples, commissions, or documents
- negative public records, scam reports, unresolved complaints, or impersonation signals

Do not accuse a company of fraud without strong evidence. Use terms like `risk signal`, `unverified`, or `needs confirmation`.

### 5) Produce a buyer score

Use a 100-point score, but keep it explainable.

Default rubric (weights sum to 100):

- Product fit (25): they already sell, buy, or distribute related products.
- Channel and market fit (20): right channel type and a market you can serve.
- Order potential (20): evidence of scale, catalog breadth, retail reach, or distribution capacity.
- Legitimacy confidence (20): public evidence supports a real, active company.
- Outreach readiness (15): enough verified info to contact now — a contact, a clear angle, and no blocking gaps.

Rating bands:

- 80-100: Strong target
- 65-79: Worth outreach
- 50-64: Research more before outreach
- 30-49: Low priority
- 0-29: Avoid or verify carefully

Always include a short reason for the score.

If you find no public evidence, say "no public evidence found" and score mainly on missing confirmations and legitimacy gaps — do not invent facts or score down on assumptions.

### 6) Recommend the next action

The output should help the user act immediately.

Choose one primary next action:

- send first outreach
- ask verification questions
- request buyer details before quoting
- prepare sample/RFQ response
- find a better contact
- monitor but do not contact yet
- avoid for now

Then provide the next message angle in one or two sentences.

## Output format

Use this structure by default:

```md
# Buyer Qualification Brief

## Verdict
- Score: <number>/100
- Priority: <Strong target | Worth outreach | Research more | Low priority | Avoid/verify carefully>
- One-line reason: <clear business judgment>

## Company snapshot
- Company: <name>
- Website/domain: <domain or unknown>
- Country/market: <market>
- Likely role: <importer/distributor/retailer/etc.>
- Relevant categories: <categories>

## Evidence
- <source/evidence point 1>
- <source/evidence point 2>
- <source/evidence point 3>

## Fit analysis
- Product fit: <short assessment>
- Channel fit: <short assessment>
- Market fit: <short assessment>
- Order potential: <short assessment>

## Risk check
- Legitimacy confidence: <High | Medium | Low>
- Risk signals: <none found / list>
- Missing confirmations: <list>

## Recommended next action
<one recommended action>

## Outreach angle
<short, buyer-specific angle for first message or follow-up>
```

## Batch output format

For multiple leads, use a compact table first:

```md
| Company | Market | Role | Score | Priority | Main reason | Next action |
|---|---:|---|---:|---|---|---|
```

Then expand only the top 3 or the riskiest leads.

## Outreach rules

When drafting outreach from this research:

- Keep it short.
- Mention one buyer-specific observation.
- Connect that observation to the user's product category.
- Avoid exaggerated claims.
- Do not pretend to know internal buyer needs.
- Do not say "I noticed you are looking for..." unless there is evidence.

Good opener pattern:

```txt
I saw that your company works with <category/channel>. We manufacture <product type> for <use case/market>. If you are reviewing suppliers for this category, I can send a short catalog and recent project examples.
```

## Safety and privacy boundaries

- Use public or user-provided information only.
- Do not generate private personal data.
- Do not infer sensitive attributes about individuals.
- Do not fabricate contacts, shipment records, certifications, or financials.
- Treat legal, sanctions, and compliance issues as signals for professional review, not final legal conclusions.
- If the user plans to export controlled goods, restricted goods, dual-use items, medical products, chemicals, or regulated products, recommend a compliance check before outreach or quotation.

## Acceptance checks

Before finishing, verify:

- The company identity is not confused with a similarly named company.
- The score is supported by evidence, not vibes.
- Missing information is clearly marked.
- The next action is specific.
- The output helps the user decide whether to contact, verify, prioritize, or avoid the lead.
