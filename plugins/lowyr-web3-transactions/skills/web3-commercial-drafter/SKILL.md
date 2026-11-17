---
name: web3-commercial-drafter
description: Draft, review and negotiate commercial and technology agreements for blockchain businesses — MoUs and term sheets, strategic partnership and co-marketing agreements (incl. sports, media and brand partnerships), token listing agreements, technology/IP licences, SaaS and API agreements with on-chain components, validator/node operator and infrastructure agreements, integration and white-label agreements — using a web3-specific clause library (token volatility, regulatory change, chain events, smart-contract failure, sanctions, custody, data on-chain). Use when the user asks to "draft an MoU/partnership/listing/licence agreement", "review this contract with a crypto counterparty", "add web3 protections", "mark up this term sheet", or shares an agreement involving tokens, wallets, chains or crypto payments. For market-making agreements use market-maker-agreement-reviewer; for SAFTs/token purchase agreements use web3-legal-expert.
---

# Web3 Commercial Drafter

Standard commercial templates miss the risks that are unique to blockchain counterparties. This skill drafts or reviews with those risks built in, and keeps the business deal in front.

## Operating standard

- Start from the **commercial objective** and the **deal tension** (who needs what, who has leverage). Clauses serve the deal.
- Identify the governing law early; flag where a clause's effect depends on it (e.g. penalty doctrine, limitation of liability, implied terms, binding nature of MoUs).
- Regulatory touchpoints are flagged and routed (e.g. if the deal involves offering tokens, custody, exchange, promotions or market-making, call the relevant skill) — do not let a commercial agreement silently commit a party to a regulated activity it is not licensed for.
- Distinguish market-standard positions from aggressive/defensive ones and say which side each favours.

## Step 1 — Deal intake

Parties and roles (incl. regulated status of each: CASP, EMI, investment firm, unregulated); deal type; value flows (fiat, tokens, revenue share, equity); token involvement (which tokens, who issues/holds/transfers them, in which jurisdictions); data flows (on-chain/off-chain, personal data); IP; term and exit; governing law and forum; drafting posture (first draft for us / review counterparty paper / negotiation round).

## Step 2 — Structure the document

Use the right instrument for the stage: **MoU/term sheet** (state explicitly which clauses are binding — confidentiality, exclusivity, costs, governing law — and which are not; avoid accidental agreements to agree that a court might enforce), **definitive agreement**, or **side letter**. Produce a definitions block that pins down token-specific terms (e.g. "Token", "Network", "Wallet", "Chain Event", "Regulatory Event", "Applicable Crypto Regulation").

## Step 3 — Web3 clause library (apply what fits)

Load `references/clause-library.md` for model clauses and negotiation notes. Headline topics:

1. **Token-denominated consideration:** valuation date and source (oracle/benchmark, VWAP across named venues), volatility collars, fiat fallback, lock-ups/vesting, tax gross-up, transfer mechanics and wallet verification.
2. **Regulatory change / regulatory event:** definition tied to change in law, regulator guidance or enforcement affecting the arrangement; obligations to renegotiate in good faith; suspension; termination without liability; no obligation to perform a regulated activity without authorisation.
3. **Licensing representations and covenants:** each party's authorisations; maintenance; notification of loss/suspension; reverse-solicitation and marketing restrictions where a party is not authorised in a market.
4. **Chain events:** forks, airdrops to holders, network halts, consensus failures, bridge exploits, token migration/redenomination — who decides which chain is canonical, effect on deliverables and consideration.
5. **Smart-contract and technology risk:** audits, upgrade governance, admin keys, bug bounties, incident response, allocation of exploit losses, no warranty of uninterrupted operation.
6. **Sanctions and AML:** reps, screening (wallet screening tools), travel-rule cooperation, termination for sanctions exposure, no facilitation.
7. **Custody and asset handling:** who holds what, segregation, no rehypothecation, insolvency remoteness, proof of reserves where relevant.
8. **Marketing and brand:** joint marketing approvals, compliance with crypto promotion rules in each target market (route to `crypto-promotions-checker`), regulator-facing statements, no investment advice, partner reputational events (e.g. counterparty enforcement action).
9. **Data:** controller/processor allocation, on-chain data minimisation, cross-border transfers.
10. **IP:** ownership of smart contracts, front-ends, brand assets; open-source components and licence compatibility; NFT/digital collectible IP grants.
11. **Liability:** caps calibrated to fees vs token value; carve-outs (fraud, wilful misconduct, confidentiality, data, IP, sanctions breach); exclusion of consequential loss including loss of tokens' market value.
12. **Termination and exit:** for regulatory event, insolvency, sanctions, change of control, reputational event; transition assistance; token/asset return.

## Step 4 — Review mode (counterparty paper)

Produce: (a) issues list — Clause | Issue | Risk to us (H/M/L) | Proposed position | Fallback; (b) redline text for every High and Medium item; (c) missing protections (from the clause library) to add; (d) points to escalate to the business.

## Output

- **Drafting mode:** full clause-level draft with definitions, bracketed commercial variables, and drafting notes in footnotes or comments.
- **Review mode:** issues list + redlines + negotiation strategy (must-haves vs tradeables).
- Always: one-paragraph business summary of what the document does and the top three risks.

## Boundaries

Not for SAFTs/token purchase agreements (`web3-legal-expert`) or market-making (`market-maker-agreement-reviewer`). Governing-law-specific enforceability points should be confirmed by counsel qualified in that law.
