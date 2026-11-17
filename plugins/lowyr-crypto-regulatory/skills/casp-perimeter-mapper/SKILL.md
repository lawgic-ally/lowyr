---
name: casp-perimeter-mapper
description: Map a crypto product or feature set, function by function, onto the ten MiCA crypto-asset services (Art 3(1)(16)) to decide whether CASP authorisation is required, which services must be on the licence, what passporting and reverse-solicitation constraints apply, and which service-specific conduct rules bite (Arts 66–82). Optional UK overlay under the FSMA 2000 (Cryptoassets) Regulations 2026. Use when the user asks "do we need a CASP licence for this", "which MiCA services does this feature trigger", "can we serve EU users from outside the EU", "is this custody", "is our wallet/bridge/swap a regulated service", or is scoping a licence application or variation.
---

# CASP Perimeter Mapper

Turns a product description into a **service map**: each user-facing function → the MiCA service it constitutes (or not) → why → what follows. The value is in decomposition: products are bundles, and authorisation attaches to each service in the bundle.

## Operating standard

- Read the Art 3(1) definitions (points 15–26) and the relevant service articles in the current text before applying them. Check the ESMA Q&A tool for service-classification Q&As (e.g. distinguishing exchange vs execution vs RTO; custody commingling; transfer services) issued since the baseline.
- Distinguish *legal text*, *ESMA/NCA interpretation*, and *your inference*.
- "Fully decentralised" claims are tested, not accepted (Recital 22). Hand off deep protocol analysis to `protocol-legal-review`.

## Step 1 — Decompose the product

Produce a function inventory from the user's description, docs, UI flows or architecture diagram. For each function capture: who initiates, who holds keys/assets at each point, who sets prices/routes orders, whether the provider acts on behalf of a client or on own account, revenue model, and whether any part runs through admin-controlled smart contracts.

## Step 2 — Map each function to the ten services (Art 3(1)(16)(a)–(j))

| Service | Definition point | Typical triggers | Conduct article |
|---|---|---|---|
| (a) Custody and administration on behalf of clients | 3(1)(17) | Holding private keys or means of access; omnibus wallets; MPC where provider can move funds | Art 75 |
| (b) Operation of a trading platform | 3(1)(18) | Multilateral matching of third-party interests; shared order books | Art 76 |
| (c) Exchange for funds | 3(1)(19) | Buy/sell vs. fiat using own capital | Art 77 |
| (d) Exchange for other crypto-assets | 3(1)(20) | Crypto-crypto conversion using own capital | Art 77 |
| (e) Execution of orders on behalf of clients | 3(1)(21) | Concluding agreements to buy/sell on client's behalf | Art 78 |
| (f) Placing | 3(1)(22) | Marketing crypto-assets to purchasers on behalf of/for offeror | Art 79 |
| (g) Reception and transmission of orders | 3(1)(23) | Routing client orders to third parties | Art 80 |
| (h) Advice | 3(1)(24) | Personalised recommendations | Art 81 |
| (i) Portfolio management | 3(1)(25) | Discretionary management mandates | Art 81 |
| (j) Transfer services on behalf of clients | 3(1)(26) | Moving crypto-assets between addresses for a client | Art 82 |

**Verify the definition points (17)–(26) against the current text before citing them in the output** — the mapping above is a baseline (points 15, 16, 17 and 26 confirmed; confirm the others).

For each function state: *Service triggered? (Yes / No / Arguable)* + reasoning + the counter-argument.

## Step 3 — Exemptions and carve-outs

- **Entity-based:** Art 60 (credit institutions, CSDs, investment firms, EMIs, UCITS ManCos/AIFMs, market operators — notification route, service-by-service equivalence). Art 2(2) person exclusions (e.g. intragroup-only).
- **Asset-based:** services relating to out-of-scope assets (NFTs, financial instruments → MiFID II instead).
- **Art 4(5):** custody/transfer of crypto-assets whose offer is exempt under Art 4(2)/(3) — no Art 59 authorisation unless the conditions in that paragraph are met.
- **Recital 22:** fully decentralised provision without any intermediary — apply a control test (admin keys, upgradeability, fee switch, front-end gating, governance concentration). Partial decentralisation does not take the activity out of scope.
- **Self-hosted software:** non-custodial wallets/tools where the provider never controls assets — assess carefully; front-end providers can still provide RTO/placing/transfer depending on facts.

## Step 4 — Territorial reach

- **Art 59:** only CASPs with a registered office in a Member State (or Art 60 entities) may provide services in the Union.
- **Art 61 / Recital 75 / ESMA Guidelines on reverse solicitation (ESMA35-1872330276-1899):** exclusive initiative of the client only; no solicitation by any means (incl. social media, sponsorships, affiliates, influencers); cannot use it to market new types of crypto-assets or services. Treat any marketing footprint in the EU as defeating the exemption.
- **Art 65:** passporting notification — list Member States, services, start date.

**Transitional regime:** the MiCA transitional period for pre-existing providers ended on 1 July 2026 (ESMA Public Statement ESMA75-113276571-1710, 23 June 2026). Unauthorised providers are expected to be in orderly wind-down — there is no grandfathering to rely on.

## Step 5 — Obligations that follow

Summarise, per triggered service, the headline obligations: Art 66 (conduct, information, marketing), Art 67 (prudential), Art 68 (governance), Art 70 (safekeeping of clients' crypto-assets and funds), Art 71 (complaints), Art 72 (conflicts), Art 73 (outsourcing), Art 74 (orderly wind-down), plus the service-specific article. Add cross-regime overlays: TFR (Regulation (EU) 2023/1113) travel rule for transfers; AMLR (Regulation (EU) 2024/1624) and national AML law; DORA (Regulation (EU) 2022/2554) for ICT risk; PSD2/EMD2 where fiat flows or EMTs are involved.

## Step 6 (optional) — UK overlay

If the user wants the UK view: map the same functions against the new regulated activities created by the Financial Services and Markets Act 2000 (Cryptoassets) Regulations 2026 (SI 2026/102; full commencement 25 October 2027) and the FCA's final rules and perimeter guidance. Note the authorisation gateway timing and the existing MLR registration position. Do this as a separate analysis — never blend UK and EU conclusions.

## Output

1. **Licence scope recommendation** — services to apply for (or vary), by entity.
2. **Function → service map** (table) with Yes / No / Arguable and reasoning.
3. **Grey zones** — ranked by enforcement risk, each with a de-risking option (product change, contractual structuring, partner CASP, geo-fencing).
4. **Territorial plan** — home MS, passporting list, reverse-solicitation exposure.
5. **Obligations matrix** per service.
6. **Sources.**

## Boundaries

Not an authorisation application. Licensing strategy (which home Member State) → combine with `web3-entity-structurer`.
