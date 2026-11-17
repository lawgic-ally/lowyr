---
name: token-distribution-analyser
description: Analyse the legal characterisation of token distribution and engagement mechanics — airdrops, giveaways, quests/points-to-token conversions, staking and holding rewards, loyalty and cashback, burn-to-redeem, referral bonuses, retroactive rewards — across jurisdictions. Tests whether each mechanic is an "offer to the public", whether exemptions apply (e.g. MiCA Art 4(2)/(3)), and the AML/KYC, consumer, gambling, securities and tax touchpoints, then proposes a de-risked design. Use when the user asks "is this airdrop regulated", "can we reward users in tokens", "does staking need a licence", "is our points programme a crypto-asset offer", or is designing a launch, campaign or rewards programme in one or more countries (EU, UK, APAC, Middle East, US).
---

# Token Distribution Analyser

Distribution mechanics are where token projects most often stumble into regimes they never intended to trigger. This skill analyses each mechanic as a legal event and proposes design changes that preserve the commercial goal.

## Operating standard

- Characterise **per mechanic, per jurisdiction**. Never conclude "airdrops are fine" in the abstract.
- For each jurisdiction, locate and read the primary text and the regulator's own guidance; if a local rule cannot be confirmed from an official source, mark it **Unverified — local counsel required**.
- Distinguish text / regulator guidance / your reasoning.

## Step 1 — Mechanic inventory

For each mechanic, record: eligibility criteria; what the user gives (money, crypto, personal data, attention/tasks, KYC, holding requirement, referrals); what the user gets (token, points, NFT, discount); vesting/lock-up; transferability; secondary-market expectation; geography and age gating; who operates it (issuer, CASP, partner).

## Step 2 — EU analysis (MiCA baseline)

1. **Classify the distributed asset first** — run `mica-token-classifier` if not done.
2. **Offer to the public?** (Art 3(1)(12)) — a communication with sufficient information to enable a decision to purchase. Analyse whether a "free" distribution conditional on actions is in substance a purchase.
3. **Exemptions:**
   - Art 4(3)(a) free offer — **not free** if purchasers provide or undertake to provide personal data, or the offeror receives fees, commissions, monetary or non-monetary benefits in exchange (Art 4(3), second subparagraph). KYC data collection, email capture, social-follow requirements and referral tasks must be analysed against this.
   - Art 4(3)(b) automatic creation as a reward for maintaining the DLT or validating transactions — protocol-level validator/miner rewards, not discretionary "staking rewards" paid by an operator.
   - Art 4(3)(c) utility token for an existing/operating good or service; Art 4(6) cap if not yet operating.
   - Art 4(3)(d) limited network of merchants; notification above EUR 1,000,000 over 12 months.
   - Art 4(2) small-offer thresholds (<150 persons per MS; ≤ EUR 1,000,000 over 12 months; qualified investors only).
   - **Art 4(4):** every exemption is lost if the offeror or anyone on its behalf communicates an intention to seek admission to trading (ESMA Q&A: on an EU CASP-operated platform). Audit all comms (Discord, X, decks, FAQs).
4. **CASP touchpoints:** does the operator custody, transfer, exchange or place on behalf of users (e.g. custodial staking, conversion of points)? → `casp-perimeter-mapper`. Custodial staking is commonly analysed as custody + transfer; check current ESMA/NCA views.
5. **Marketing** of the campaign → `crypto-promotions-checker`.
6. **AML:** TFR (Regulation (EU) 2023/1113) on transfers by CASPs; AMLR (Regulation (EU) 2024/1624) and national AML law; sanctions screening of recipients.
7. **Consumer law / gambling:** chance-based allocation (lotteries, raffles, mystery boxes) + any consideration → gambling/lottery law risk under national law. Minors.
8. **Data protection:** lawful basis for data collected for eligibility; wallet addresses as personal data where linkable.

## Step 3 — Other jurisdictions (run separately for each)

For each jurisdiction in scope, answer the same questions using local law. Typical lines of inquiry (verify each against primary sources at run time):
- **UK:** whether the activity falls within new regulated activities and the public offers / admissions regime under the FSMA 2000 (Cryptoassets) Regulations 2026 (full commencement 25 October 2027) and FCA rules; financial promotions restriction for any communication inviting engagement; staking as a specified activity.
- **US:** investment-contract analysis for airdrops/rewards (current SEC/CFTC posture and any federal market-structure legislation in force at run time — search, do not assume), state money-transmission for custody/transfer, sweepstakes law for chance-based mechanics, OFAC.
- **Asia-Pacific / Middle East (e.g. Indonesia, Singapore, Hong Kong, Japan, UAE):** identify the competent authority and the instrument governing crypto-asset trading/distribution and advertising (e.g. in Indonesia, the OJK framework following the transfer of crypto supervision from Bappebti; in the UAE, VARA in Dubai and ADGM/DIFC frameworks), whether only licensed entities may distribute or market to residents, and whether "free" distributions count as offering or trading. Read the regulator's own text.

## Step 4 — Tax and accounting flags (flag, do not opine)

Recipient taxation on receipt vs disposal, issuer's VAT/withholding position, accounting for token incentives. Recommend specialist input.

## Step 5 — De-risked design

Propose concrete changes, mapped to the risk each removes, e.g.: remove personal-data or task conditions for the "free" route; separate eligibility snapshot from any sale; geo-fence non-target jurisdictions with layered controls (IP, KYC country, T&Cs, wallet screening); time the admission-to-trading communications; route custody/conversion through an authorised CASP; replace chance mechanics with skill or fixed allocation; add free-entry routes; cap value per user.

## Output

1. **Executive summary** — per jurisdiction: Green / Amber / Red, with one-line reason.
2. **Mechanic × jurisdiction matrix** — characterisation, exemption relied on, conditions, risk.
3. **Design recommendations** — change → risk removed → commercial impact.
4. **Communications guardrails** (Art 4(4) and promotions).
5. **Open points** requiring local counsel or regulator engagement.
6. **Sources** per jurisdiction.

## Boundaries

Tax is flagged, not advised. Where a jurisdiction's position cannot be verified from an official source, say so and do not fill the gap from memory.
