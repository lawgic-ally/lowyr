---
name: mica-token-classifier
description: Classify a token or digital asset under EU MiCA (Regulation (EU) 2023/1114) through a fixed, auditable decision tree — out of scope (NFT, financial instrument, other Art 2(4) exclusions), EMT, ART, or "other crypto-asset" (incl. utility token) — then test the Title II offer exemptions. Use whenever the user asks "is this token in scope of MiCA", "is this an EMT/ART/utility token", "is this a financial instrument or a crypto-asset", "how do we classify this token in the EU", or needs a classification memo for a token, stablecoin, NFT collection, loyalty point, fan/membership token or tokenised right.
---

# MiCA Token Classifier

Produces a reasoned, step-by-step classification of a digital asset under MiCA. The output is a **classification memo** in which every branch of the decision tree is answered, reasoned and sourced — so a reviewer (regulator, auditor, GC) can follow the path and challenge any single step.

## Operating standard

- **Read before you cite.** Before relying on any article, open the current text on EUR-Lex (`eur-lex.europa.eu/eli/reg/2023/1114/oj/eng`) or the ESMA Interactive Single Rulebook. Do not infer an article's content from its number or title. Baseline references are in `references/decision-tree.md`; re-verify them.
- **Three registers, never blended:** (1) what the text says, (2) what ESMA/EBA/NCAs say about it (guidelines, Q&As), (3) your own reasoning. Label each.
- **Substance over form.** Marketing labels ("utility", "governance", "NFT", "points") are evidence, not conclusions. Classify on rights, functions, transferability and economic reality.
- **Currency check.** Confirm whether any ESMA Q&A, guideline or NCA statement issued after this skill's citation baseline changes a branch.

## Step 0 — Fact intake (ask only for what is missing)

Build a fact sheet before classifying. If any of the following are unknown and outcome-determinative, ask (concisely, in one list) before proceeding:

1. **Technical form:** chain/standard (ERC-20, ERC-721, ERC-1155, SPL…), transferability (free, whitelisted, soulbound), divisibility, supply mechanics (fixed, mintable, burnable), admin controls.
2. **Rights attached:** profit share, dividends, revenue, interest, redemption, voting (on what), access to goods/services, discounts, rewards, ownership/claims on assets, debt-like claims.
3. **Value reference:** pegged or stabilised? Against one official currency, a basket, commodities, other crypto?
4. **Issuer and distribution:** identifiable issuer/offeror? Sale, free distribution, rewards, airdrop? Target persons and Member States? Trading-platform admission sought?
5. **Fungibility:** unique items vs series/collections; fractionalisation.
6. **Function today:** is the good/service the token gives access to already in operation?

## Step 1 — Is it a "crypto-asset" at all?

Test the Art 3(1)(5) definition: a digital representation of a value or a right, transferable and storable electronically using DLT or similar technology. Flag edge cases: non-transferable tokens, purely off-chain ledgers, "points" never recorded on DLT. If not a crypto-asset → MiCA does not apply; note any adjacent regime (e-money, payment services, consumer law) and stop.

## Step 2 — Scope exclusions (Art 2)

Answer each in order; the first "yes" ends the MiCA analysis (but record the remaining answers for robustness):

**2a. Unique and non-fungible (Art 2(3), Recitals 10–11).**
- Is each token genuinely unique *and* are the rights/assets represented unique? A unique identifier alone is not enough.
- Fractional parts of a unique asset → not unique. Large series/collections may indicate fungibility — weigh de facto features (Recital 11).
- Read the ESMA Guidelines on qualification (ESMA75453128700-1323) section on unique/non-fungible assets.

**2b. Financial instrument (Art 2(4)(a), Art 2(5)).**
- Apply the ESMA Guidelines on the conditions and criteria for the qualification of crypto-assets as financial instruments (ESMA75453128700-1323), which operate by reference to MiFID II Art 4(1)(15) and Annex I Section C.
- Transferable securities test (MiFID II Art 4(1)(44)): negotiable on the capital market? Class of securities? Rights comparable to shares/bonds (profit, voting on the issuer, repayment)? Note: lock-ups do not of themselves exclude negotiability.
- Also test money-market instruments, units in CIUs, derivatives, emission allowances.
- Remember that national transposition of MiFID II can differ — flag Member State–specific divergences as a risk.

**2c. Other Art 2(4) exclusions:** deposits (incl. structured deposits), funds (unless they qualify as EMTs), securitisation positions, and the insurance/pension products listed in Art 2(4). Also check the *person*-based exclusions in Art 2(2) where relevant (e.g. intragroup-only service providers, insolvency administrators, the ECB and national central banks, public international organisations).

## Step 3 — EMT? (Art 3(1)(7), Title IV)

Does it purport to maintain a stable value by referencing the value of **one** official currency? If yes → EMT. Consequences: only credit institutions or e-money institutions may offer to the public / seek admission (Art 48); EMTs deemed e-money; white paper under Art 51. Note the anti-avoidance logic: a token functionally pegged to one currency is not rescued by calling it an ART.

## Step 4 — ART? (Art 3(1)(6), Title III)

Does it purport to maintain a stable value by referencing another value or right or a combination (including one or more official currencies, commodities, crypto-assets), and is it not an EMT? If yes → ART; authorisation under Art 16; white paper under Art 19. Test "purports to": stabilisation mechanism, reserve, marketing claims. Algorithmic "stablecoins" — analyse what is purported, not what is achieved.

## Step 5 — "Other crypto-asset" (Title II) and the utility-token sub-type

Residual category. Then test whether it is a **utility token** (Art 3(1)(9)): *only* intended to provide access to a good or service supplied by its issuer. Any additional relevant function (investment expectation, governance over third-party matters, yield) defeats the "only" condition — say so explicitly.

## Step 6 — Title II regime consequences

For Title II crypto-assets, determine the regime that attaches to the planned activity:

| Question | Provision |
|---|---|
| Is there an "offer to the public"? | Art 3(1)(12) |
| Small-offer exemptions (white paper not required): <150 persons per MS; ≤ EUR 1,000,000 total consideration over 12 months; qualified investors only | Art 4(2)(a)–(c) |
| Title II disapplied: free offer; automatic validation reward; utility token for an **existing/operating** good or service; limited network of merchants | Art 4(3)(a)–(d) |
| "Free" fails if personal data or fees/commissions/benefits are received | Art 4(3), 2nd subpara |
| Limited network > EUR 1,000,000 in 12 months → notify NCA | Art 4(3), 3rd subpara |
| Exemptions lost if intention to seek admission to trading is communicated (ESMA Q&A: EU CASP-operated platform) | Art 4(4) |
| Utility token for goods/services not yet in operation → offer period ≤ 12 months | Art 4(6) |
| Admission to trading → Art 5 white paper duties (incl. trading-platform operator) | Art 5 |

Hand off to `token-distribution-analyser` for detailed airdrop/rewards mechanics, and to `mica-whitepaper-reviewer` if a white paper is required.

## Step 7 — Robustness and counter-classification

For the conclusion reached, write the **strongest argument for the next most likely classification** and explain why it fails (or doesn't). Rate classification confidence: **High** (text + guidance align), **Medium** (text supports, guidance silent), **Low** (reasonable contrary view; NCA engagement advisable). Identify what fact change would flip the result (e.g. "adding a buy-back from treasury revenue moves this toward a transferable security").

## Output — classification memo

1. **Bottom line** (2–3 sentences): classification, regime, confidence.
2. **Facts relied on / assumptions** (flag each assumption).
3. **Decision path table** — Step | Test | Answer | Reasoning | Source.
4. **Regime consequences** — who may offer, white paper, marketing, CASP touchpoints.
5. **Counter-classification and flip factors.**
6. **Open points / NCA engagement** — where a Member State view or ESMA Q&A is pending.
7. **Sources** — article numbers, guideline references with dates, URLs.

Use a Mermaid flowchart of the path actually taken when the reader is non-legal.

## Boundaries

- EU only. For multi-jurisdiction classification, run this tree for the EU and hand off other jurisdictions to `web3-regulatory-expert`.
- Not a tax characterisation. Flag tax only where it affects regulatory status.
- Not legal advice; the memo supports a qualified lawyer's review.
