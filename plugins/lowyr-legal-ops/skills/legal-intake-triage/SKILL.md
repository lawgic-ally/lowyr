---
name: legal-intake-triage
description: Triage incoming requests to an in-house legal team (from Slack, email, tickets or forms) — classify the matter type, extract facts, rate risk and urgency, set an SLA, identify missing information, route to the right owner or specialist skill, and draft the first response to the requester. Designed for fast-moving regulated tech/crypto businesses. Use when the user pastes a business request and asks "triage this", "what is this and who should handle it", "how urgent is this", "draft a reply to the business", or wants to design or run a legal intake/ticketing process.
---

# Legal Intake Triage

The front door of an in-house legal function. Goal: every request gets a consistent classification, a risk-based priority, a named owner and a useful first reply within minutes — and the legal team spends time only where it matters.

## Step 1 — Extract

From the request, extract: requester and team; what they want to do (in one sentence); counterparties; products, tokens or features involved; jurisdictions and users affected; money/value at stake; deadlines (real vs stated); documents attached; whether anything has already happened (signed, launched, published, sent).

## Step 2 — Classify

Assign one primary and any secondary categories:

| Category | Examples | Typical route |
|---|---|---|
| Contract — standard | NDA, standard vendor terms on our paper | Self-serve template / paralegal |
| Contract — negotiated | Partnership, licence, listing, MoU | `web3-commercial-drafter` |
| Contract — market making / liquidity | MM agreements, token loans | `market-maker-agreement-reviewer` |
| Regulatory — classification / perimeter | New token, new feature, new market | `mica-token-classifier`, `casp-perimeter-mapper`, `web3-regulatory-expert` |
| Regulatory — disclosure | White paper, modifications | `mica-whitepaper-reviewer` |
| Marketing / promotions | Campaigns, giveaways, influencers | `crypto-promotions-checker` |
| Distribution mechanics | Airdrops, rewards, staking, loyalty | `token-distribution-analyser` |
| Corporate / structuring | New entity, reorganisation, governance | `web3-entity-structurer` |
| Protocol / technical | Smart-contract change, admin keys, bridge | `protocol-legal-review` |
| Regulator interaction | Consultation, information request, inspection | `consultation-response-drafter` / senior counsel |
| Data protection | DSAR, new processing, breach | Privacy owner |
| AI governance | New AI tool, AI use case | `ai-governance-builder` |
| Disputes / incidents | Complaint, threat of claim, exploit, enforcement | Senior counsel immediately |

## Step 3 — Risk and urgency

**Risk (impact × likelihood):**
- *Critical* — regulatory breach in progress, enforcement contact, incident/exploit, sanctions hit, imminent publication of non-compliant material, litigation threat.
- *High* — new regulated activity, new jurisdiction, token issuance/distribution, material contract value, public statements about the product's regulatory status.
- *Medium* — negotiated contracts within policy, marketing within established patterns.
- *Low* — templates, routine questions.

**Urgency:** driven by real external deadlines (regulator, launch with legal effect, contract signature), not internal enthusiasm. Flag when an internal deadline creates legal risk.

**SLA suggestion:** Critical — same hour; High — 1 business day for first substantive view; Medium — 3 business days; Low — self-serve or 5 business days. Adjust to the team's own SLAs if provided.

## Step 4 — Information gaps

List the minimum questions needed to progress, in the requester's language (no legalese). Never ask for information already in the request.

## Step 5 — First response to the requester

Draft a short reply (Slack or email tone as appropriate): acknowledgement, what legal will do, by when, what is needed from them, and any **immediate stop/hold instruction** where risk is Critical or High (e.g. "please don't publish/sign/launch until we've reviewed X").

## Output

```
Ticket: <one-line title>
Category: <primary> (+ secondary)
Risk: <Critical/High/Medium/Low> — <one-line reason>
Urgency / SLA: <...>
Owner / route: <person or skill>
Facts: <bullets>
Missing info: <bullets>
Hold instruction: <yes/no + text>
Draft reply: <text>
```

For batch triage, output a table sorted by risk then deadline.

## Boundaries

Triage is not advice; it routes work. Anything Critical goes to a human lawyer immediately regardless of the suggested route.
