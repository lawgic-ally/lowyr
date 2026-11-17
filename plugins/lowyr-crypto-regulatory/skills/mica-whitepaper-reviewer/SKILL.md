---
name: mica-whitepaper-reviewer
description: Review a MiCA crypto-asset white paper (Title II "other crypto-assets", and with adaptations ART/EMT white papers) line by line against Art 6 and Annex I of Regulation (EU) 2023/1114 and the ITS templates in Implementing Regulation (EU) 2024/2984, then output a gap table with severity, the provision breached and a proposed fix. Use when the user uploads or pastes a white paper draft and asks to "review", "QA", "check compliance", "is this ready to notify", "find gaps", or wants a pre-notification review before submitting to an NCA, or a post-publication check before an Art 12 modification.
---

# MiCA White Paper Reviewer

A pre-notification quality gate. It does not draft the white paper; it tests a draft against the law and the ITS template and returns a **defect list a drafter can action**.

Primary sources to open before reviewing (re-verify; baseline in the repo citation register):
- MiCA Arts 4–15 (Title II), Art 19 (ART), Art 51 (EMT), Annexes I–III — EUR-Lex / ESMA Interactive Single Rulebook.
- Commission Implementing Regulation (EU) 2024/2984 — templates (Annex, Tables 1–4) and iXBRL format (Art 2). ESMA states the format requirements applied from 23 December 2025.
- ESMA MiCA Q&As touching Title II white papers (search the ESMA Q&A tool for the latest).

## Step 1 — Establish the review frame

Confirm (ask if unclear):
- Token category: Title II / ART / EMT → selects Art 6 + Annex I, Art 19 + Annex II, or Art 51 + Annex III.
- Who draws it up: offeror, person seeking admission, or trading-platform operator (Art 6(1) second subparagraph cases; Annex I Part C).
- Purpose: offer to the public, admission to trading, or both. Home Member State / NCA.
- Stage: first notification or modification under Art 12.
- Utility token for a service not yet in operation? (Art 4(6) 12-month offer limit; Art 6(5)(d) statement.)

## Step 2 — Mandatory front-matter (Art 6(3)–(8))

| Check | Provision | Test |
|---|---|---|
| "Not approved by any competent authority" statement on first page, naming the responsible person | Art 6(3); ITS field 02 | Exact wording against ITS predefined text for the right role (offeror / admission / platform operator) |
| No assertions on future value | Art 6(4) | Scan entire document, incl. summary and project sections, for price/return/appreciation language |
| Risk statements: may lose value in part or in full; may not always be transferable; may not be liquid | Art 6(5)(a)–(c); ITS field 04 | Present, clear, unambiguous |
| Utility token statement (if applicable) | Art 6(5)(d); ITS field 05 | Present where token is a utility token |
| Management-body compliance statement | Art 6(6); ITS field 03 | Placed after the Art 6(3) statement; matches predefined text |
| Summary — brief, non-technical; key info on the offer/admission; warnings | Art 6(7) | Placed after the Art 6(6) statement; readable standalone; consistent with body |
| Date of notification and table of contents | Art 6(8) | Present |
| Language | Art 6 (language paragraph — confirm number in the current text) | Official language of home MS or a language customary in international finance; consider host MS |

## Step 3 — Annex I disclosure walk-through (Title II)

Go item by item through Annex I. The part summaries below are an index only — the Annex I text and the ITS template are authoritative. For each item record **Present / Partial / Missing / Inconsistent**:

- **Part A** — offeror or person seeking admission (identity, legal form, addresses, LEI where applicable, management body, business activity, financial condition as Annex I specifies).
- **Part B** — issuer, if different from the offeror.
- **Part C** — trading-platform operator where it draws up the white paper, and the reason.
- **Part D** — crypto-asset project (name/ticker, persons involved, milestones, resources, planned use of funds).
- **Part E** — offer to the public / admission to trading (amount, price, subscription period, Art 10 safeguarding, withdrawal right under Art 13, CASP placing, trading platforms, applicable law and court).
- **Part F** — the crypto-asset (type, characteristics, functionality).
- **Part G** — rights and obligations (procedures and conditions for exercising rights, modification, future offers, supply adjustment, quality of service, complaint handling, protection schemes).
- **Part H** — underlying technology (DLT, consensus, incentive mechanisms, audits).
- **Part I** — risks (offer-related, issuer-related, crypto-asset-related, project-implementation, technology, mitigation).
- **Part J** — sustainability indicators on adverse climate and environment-related impacts of the consensus mechanism (check against the applicable RTS on sustainability indicators).

Use the ITS Annex table for Title II as the authoritative field list and data-type constraints (e.g. `{ALPHANUM-n}` limits, predefined text, date format `YYYY-MM-DD`).

## Step 4 — Substantive quality tests (Art 6(2))

- **Fair, clear, not misleading:** promotional tone, unexplained jargon, buried risks, selective metrics.
- **No material omissions:** cross-check against what the facts disclose (e.g. admin keys, mint authority, treasury holdings, lock-ups, insider allocations, related-party arrangements) — if it exists in the smart contract or tokenomics and is absent from Parts F–I, flag it.
- **Internal consistency:** numbers (supply, price, allocation) identical across summary, Part E and Part F; risk factors mirror Part H technology choices.
- **Consistency with marketing communications** (Art 7(1)(c)) if drafts are supplied.
- **Liability lens (Art 15):** for each defect, note whether it would plausibly ground a holder's claim for incomplete/unclear/misleading information. Contractual exclusions of that liability are void — flag any disclaimer that attempts one.

## Step 5 — Format and filing readiness

- iXBRL/XHTML per ITS Art 2; fields map to the ITS template; taxonomy elements limited to template fields.
- Notification to the home NCA at least 20 working days before publication, accompanied by the explanation of why the crypto-asset is not an excluded asset, an EMT or an ART (Art 8 — confirm paragraph numbers); publication on website (Art 9); machine-readability.
- For modifications: Art 12 triggers, time-stamping, reasons for modification published.

## Output

1. **Readiness verdict:** Ready to notify / Ready subject to minor fixes / Not ready.
2. **Defect table:** # | Location (section/field) | Issue | Provision | Severity (Blocking / Material / Minor / Drafting) | Proposed fix (redline text where possible).
3. **Liability hot-spots** (Art 15) — top five statements most exposed.
4. **Facts to confirm with the business/tech team** before sign-off.
5. **Sources** — provisions and ITS fields relied on.

Severity guide: *Blocking* = mandatory statement/field missing or wrong; *Material* = omission or inconsistency that could mislead; *Minor* = incomplete but not misleading; *Drafting* = clarity/style.

## Boundaries

- Does not certify compliance; output supports the management body's own Art 6(6) statement.
- Does not generate iXBRL — use a dedicated conversion tool for that, then re-run Step 5 on the output.
