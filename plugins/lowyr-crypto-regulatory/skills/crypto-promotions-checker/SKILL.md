---
name: crypto-promotions-checker
description: Review crypto marketing — campaigns, social posts, influencer briefs, partner/sponsorship activations (e.g. sports clubs, brands), giveaways, emails, landing pages, app push notifications — against MiCA marketing-communication rules (Arts 7, 29, 53, 66), the UK financial promotions regime, and the frequently missed overlays (prize-draw/gambling, consumer protection, sponsorship and influencer disclosure). Returns a RAG-rated claim-by-claim review with compliant rewrites. Use when the user asks "can we say this", "review this campaign", "is this promo compliant", "check this influencer script", or shares any crypto marketing copy or promotion mechanics.
---

# Crypto Promotions Checker

Built for the reality of crypto marketing: fast-moving campaigns, partner co-branding, social-first formats and promotional mechanics (giveaways, contests, rewards). The output is something a marketing team can act on the same day.

## Operating standard

- Open the current text of the provisions applied (EUR-Lex / ESMA Interactive Single Rulebook / FCA Handbook) before citing.
- Separate **binding rules**, **regulator guidance/expectations**, and **judgement calls**.
- The test is the communication as the *average target consumer* would perceive it, across the whole format (visual, audio, caption, link-out), not the legal disclaimer in isolation.

## Step 1 — Classify the communication

1. **Asset type** → regime: Title II crypto-asset → Art 7 (with Art 9 publication); ART → Art 29; EMT → Art 53. CASP's own service promotion → Art 66 (information to clients, incl. marketing communications, fair, clear and not misleading). Out-of-scope asset (NFT, financial instrument) → say so and switch regime.
2. **Is a white paper required?** If yes, no marketing communication may be disseminated before its publication (Art 7(2) for Title II; Art 29(6) for ARTs; the equivalent paragraph of Art 53 for EMTs). Check timeline.
3. **Audience and territory:** EU Member States targeted; UK users reachable? (UK: s 21 FSMA financial promotion restriction; cryptoasset promotions regime incl. COBS 4.12A; confirm approver/exemption route.) Other jurisdictions with crypto-advertising rules — list and hand off to `web3-regulatory-expert` if material.
4. **Who is the communicator:** offeror, CASP, partner (club/brand), influencer, affiliate. Responsibility under MiCA sits with the offeror / person seeking admission / CASP, but partners create attribution and reverse-solicitation risk.

## Step 2 — MiCA content tests (Title II baseline; adapt for ART/EMT)

| Test | Source |
|---|---|
| Clearly identifiable as marketing | Art 7(1)(a) |
| Fair, clear and not misleading | Art 7(1)(b) |
| Consistent with the white paper (where required) | Art 7(1)(c) |
| States clearly that a white paper has been published and gives the website address, plus contact details | Art 7(1)(d) |
| Mandatory statement: "This crypto-asset marketing communication has not been reviewed or approved by any competent authority in any Member State of the European Union", plus the responsible-person statement | Art 7(1)(e) and following subparagraph — copy the wording from the current text |
| No dissemination before white paper publication | Art 7(2) (ART: Art 29(6); EMT: equivalent paragraph in Art 53 — market soundings permitted) |
| No assertions on future value (mirrors Art 6(4) for the white paper) | Art 6(4) + Art 7(1)(b) |
| ART/EMT specifics, e.g. EMT redemption-at-par statement | Arts 29, 53 |
| NCA notification and supervisory powers; no prior approval may be required | Art 8 (incl. 20-working-day notification of the white paper); Art 7 NCA-assessment paragraph; check home/host NCA practice |

## Step 3 — Claim-by-claim review

Extract every claim, visual and mechanic. Rate each:
- **RED** — prohibited or plainly misleading (price predictions, "guaranteed", "risk-free", "safe as a bank", unbalanced returns, implied regulator endorsement, FOMO countdowns tied to price, missing mandatory statements, pre-white-paper dissemination).
- **AMBER** — needs substantiation, balance or reframing (APYs without conditions, "regulated" without scope, comparisons, celebrity/athlete endorsement implying financial advice, "utility" claims for services not yet live).
- **GREEN** — compliant as drafted.

For every RED/AMBER item give: the issue, the rule, and a **compliant rewrite**.

## Step 4 — Overlays commonly missed

- **Promotional mechanics (giveaways, prize draws, contests, "win tokens"):** classify under local law — prize draw vs skill contest vs gambling (consideration + chance + prize). Purchase-required or token-holding-required entries can turn a giveaway into unlicensed gambling or a lottery in some Member States/UK. Free-entry routes and T&Cs needed. Also MiCA Art 4(3)(a): a giveaway is not "free" if personal data or other benefits are received — hand off to `token-distribution-analyser`.
- **Consumer protection:** Unfair Commercial Practices Directive 2005/29/EC (as amended) and national law; dark patterns; minors (exclude under-18 targeting; club/sports audiences skew young).
- **Influencers/affiliates:** ad disclosure (#ad), platform policies (Meta, Google, X, TikTok each have crypto-ad policies requiring authorisation proof), contractual controls and approval rights, record-keeping.
- **Sports and partner marketing:** league/federation rules on crypto sponsorship, broadcaster and stadium advertising codes, partner brand guidelines, club's own regulator-facing commitments.
- **Data protection:** consent for marketing communications (ePrivacy), lead capture for giveaways.

## Output

1. **Go / Go with changes / No-go** headline.
2. **RAG table:** # | Claim or element | Rating | Rule | Rewrite.
3. **Mandatory statements block** — ready-to-paste text for the regime and language.
4. **Mechanics assessment** (if any promotion).
5. **Pre-flight checklist** — white paper published, NCA notification, approvals log, influencer brief, T&Cs, geo-targeting.
6. **Sources.**

## Boundaries

Not a substitute for an FCA s 21 approval where required. Local gambling/prize-promotion law varies by country — flag where local counsel is needed rather than concluding.
