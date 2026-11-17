---
name: market-maker-agreement-reviewer
description: Review, negotiate or draft crypto market-making and liquidity-provision agreements — token loan + call option structures, retainer/fee models, KPIs (spread, depth, uptime, venue coverage), reporting and audit rights, conflicts and information barriers — and test them against market-abuse rules (MiCA Title VI, Arts 86–92), venue rules and sanctions/AML, from either the issuer's or the market maker's side. Use when the user shares a market-making agreement or term sheet, asks "is this MM deal standard", "what KPIs should we require", "is this option structure a problem", "how do we avoid wash trading risk", or is setting up a proprietary trading or liquidity entity.
---

# Market-Maker Agreement Reviewer

Market-making agreements are where commercial terms, token economics and market-integrity law collide. Badly drafted deals create manipulation risk, hidden dilution and misaligned incentives. This skill reviews them through all three lenses.

## Operating standard

- Read MiCA Title VI (Arts 86–92) in the current text and check for the latest ESMA Guidelines on supervisory practices to prevent and detect market abuse under MiCA (ESMA75-453128700-1039), the delegated acts on Art 92 (STORs / prevention and detection) and venue rulebooks before concluding.
- Identify the side we act for (issuer/foundation, market maker, venue) and the regulated status of each party.
- Distinguish legal prohibition, regulator expectation and commercial market practice.

## Step 1 — Map the economic structure

- **Model:** (a) retainer (issuer pays fees, MM uses own inventory), (b) **loan + call option** (issuer lends tokens; MM may buy them at strike prices at expiry or return them), (c) hybrid, (d) proprietary trading by an affiliated entity.
- **Token loan:** amount, % of circulating supply, term, return mechanics, collateral, treatment on default/insolvency, voting/airdrop rights on lent tokens.
- **Options:** strike prices (fixed vs. premium to TWAP), tranches, exercise windows, cash vs physical settlement. Compute the MM's incentive: does option payoff reward pushing price up before exercise, or selling inventory down? Flag misalignment.
- **Fees and rebates:** fixed fees, performance fees, venue rebates.
- **Disclosure:** is the arrangement (and token loan) disclosed to the market and reflected in the white paper / tokenomics disclosures? Undisclosed supply overhang is both a disclosure and a liability issue (white paper liability, Art 15, if it should have been disclosed).

## Step 2 — Performance obligations (KPIs)

Check for precise, measurable, monitorable KPIs: maximum bid-ask spread (bps) per venue; minimum depth at ±[x]% from mid (in USD/EUR); uptime (% of time quoting both sides); venue list and pairs; quote-size minimums; exceptions (extreme volatility, venue outages, chain events). Require **independent reporting** (e.g. venue data or third-party monitoring), monthly reports, audit rights, and remedies (fee reduction, cure period, termination).

## Step 3 — Market-integrity review (MiCA Title VI and equivalents)

| Risk | Rule | What to look for in the contract | Mitigation |
|---|---|---|---|
| Wash trading / self-matching / fictitious volume | Art 91 (manipulation) | Volume targets, "volume generation" language, fees tied to volume | Prohibit volume KPIs; self-trade prevention; spread/depth KPIs only |
| Price-setting / marking the close | Art 91 | Obligations to "support price", "maintain floor", price targets | Delete; replace with neutral liquidity obligations |
| Insider dealing / unlawful disclosure | Arts 87, 89, 90 | Issuer sharing listings, partnerships, unlock schedules early | Information barriers; insider lists; restricted periods; disclosure policy under Art 88 |
| Disclosure of inside information by issuer | Art 88 | Timing of announcements vs MM activity | Issuer disclosure procedure; MM blackout around announcements |
| Prevention/detection and STORs | Art 92 | PPAET obligations of MM and venues | MM surveillance; cooperation with venues; STOR process |
| Extraterritorial reach | Art 86 | Activity outside the EU on tokens admitted to EU venues | Treat as in scope |

Also apply: venue rulebooks (market-maker programmes often have their own conduct rules), UK market-abuse rules under the incoming FCA cryptoasset regime (verify status at run time), US anti-manipulation provisions where US venues/persons are involved, and sanctions/AML screening of counterparties and wallets.

## Step 4 — Legal terms review

Governing law and forum; MM's regulated status (does the MM provide a crypto-asset service *to the issuer* — e.g. execution or placing — requiring authorisation?); custody of loaned tokens (wallet control, segregation, no rehypothecation, return on insolvency); events of default; termination for market-abuse investigation or regulatory event; confidentiality vs regulatory disclosure carve-outs; reps on no manipulation; indemnities; liability caps; tax on loans/options; accounting treatment (flag for finance).

## Step 5 — For proprietary / affiliated market-making entities

If the issuer group sets up its own trading entity: conflicts of interest between issuer and trading arm; information barriers and governance; licensing of the entity in its jurisdiction and in jurisdictions of the venues it trades on; whether trading in the group's own token is disclosed; treasury-management policy; hand off structuring to `web3-entity-structurer`.

## Output

1. **Deal summary** — structure, economics, implied dilution and incentive analysis (worked example with numbers if inputs are given).
2. **Red-flag list** — market-integrity issues first.
3. **Issues table** — Clause | Issue | Risk (H/M/L) | Position | Redline.
4. **KPI schedule** — proposed measurable KPIs and reporting.
5. **Compliance package** — information-barrier, blackout and disclosure procedures to adopt alongside the agreement.
6. **Sources.**

## Boundaries

Not trading advice. Pricing of options and accounting/tax treatment are flagged for specialists.
