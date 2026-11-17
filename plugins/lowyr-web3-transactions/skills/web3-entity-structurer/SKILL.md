---
name: web3-entity-structurer
description: Design or review the corporate and regulatory structure of a blockchain group — where to place the token issuer/foundation, operating company, licensed CASP/VASP, IP holder, treasury, proprietary trading or market-making entity, and service companies — comparing jurisdictions (e.g. EU Member States under MiCA, Switzerland, Cayman Islands, BVI, UAE (VARA, ADGM, DIFC, free-zone DAO regimes), Singapore, UK) on licensing, substance, governance, banking, and flagged tax touchpoints, and produce a structure chart and memo. Use when the user asks "which jurisdiction should we use", "how should we structure the group", "do we need a foundation", "where should the trading entity sit", or is setting up, reorganising or licensing a web3 business.
---

# Web3 Entity Structurer

Structuring is about allocating **functions, risk and regulatory perimeter** to the right entities in the right places — and being able to defend that allocation to regulators, banks, auditors and counterparties.

## Operating standard

- **Function before jurisdiction.** Decide what each entity must do, then where it can lawfully and practically do it.
- **Substance is non-negotiable.** Every recommendation states the people, decision-making and premises each entity needs to be credible (regulatory, tax and banking).
- Jurisdictional facts (licence types, capital, timelines, regulator) must be verified from the regulator's or legislator's own site at run time; mark anything unverified. Tax is **flagged for specialist advice**, not concluded.
- Separate the analysis per jurisdiction before comparing.

## Step 1 — Functional map

List the group's functions and assign each a regulatory characterisation:
- Token issuance/offering (Title II offeror, ART/EMT issuer?), protocol development, IP ownership and licensing, front-end operation, custody, exchange/brokerage, trading platform, transfer services, proprietary trading / market making, treasury management, staking/validation, payments/fiat on-ramp, marketing to end-users, partnerships (e.g. sports/media), employment.
Use `casp-perimeter-mapper` for licence triggers and `mica-token-classifier` for the token.

## Step 2 — Constraints and objectives

Target markets and users (EU passport needed? UK? US excluded?); regulatory appetite (licensed vs unlicensed functions); banking access; investor requirements; timeline; budget; founders' locations; existing entities and contracts (migration cost); exit/listing plans; reputational sensitivity.

## Step 3 — Jurisdiction comparison (per candidate)

For each candidate jurisdiction and function, assess and source:

| Dimension | Questions |
|---|---|
| Regulatory regime | Licence(s) required; regulator; capital; fit-and-proper; timelines; local director/officer requirements; ongoing reporting |
| Market access | Passporting (e.g. MiCA Art 65 for EU CASPs), recognition, reverse-solicitation limits (MiCA Art 61), local marketing restrictions |
| Entity form | Company, foundation company, foundation, association, DAO-specific regime; ownerless structures; governance flexibility |
| Substance | Minimum people/decision-making on the ground; economic-substance rules |
| Banking and custody | Practical availability of fiat banking and custodians for crypto businesses |
| Legal system | Courts, insolvency treatment of crypto-assets, enforceability of on-chain governance |
| Tax (flag only) | Corporate tax, token-issuance treatment, VAT, withholding, CFC/transfer-pricing exposure — specialist sign-off required |
| Reputation | Perception by regulators, banks, partners in target markets; FATF lists |

## Step 4 — Option design

Present 2–3 structures (e.g. "EU-licensed hub + offshore foundation", "single EU group", "Middle East hub + EU CASP subsidiary"). For each: Mermaid structure chart (entities, ownership %, licences, functions, intra-group agreements), flows of tokens/fiat/IP, regulatory perimeter per entity, pros/cons, set-up timeline and cost drivers, key risks (e.g. mind-and-management, permanent establishment, regulatory arbitrage perception, conflicts between trading entity and issuer).

## Step 5 — Intra-group architecture

List the intra-group agreements required (IP licence, services, cost-sharing, token-management, treasury, data-sharing, market-making/liquidity), their arm's-length basis (flag transfer pricing), and governance (board composition, conflicts policy, information barriers — especially between issuer/treasury and any trading entity).

## Step 6 — Implementation roadmap

Sequenced steps: incorporations, licence applications (with dependencies), banking, hiring for substance, contract migration, token-related disclosures (white paper updates where an offeror/issuer changes), regulator notifications, and decision points.

## Output

1. **Recommendation** (one paragraph) and why it beats the alternatives.
2. **Options comparison table.**
3. **Structure charts** (Mermaid).
4. **Per-entity perimeter and substance sheet.**
5. **Intra-group agreements list.**
6. **Roadmap** with critical path.
7. **Specialist inputs required** (tax, local counsel per jurisdiction).
8. **Sources.**

## Boundaries

Does not give tax advice or opinions on local corporate law; it frames the questions and flags the dependencies.
