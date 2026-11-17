---
name: ai-governance-builder
description: Draft or review an organisation's AI governance framework — AI code of ethics, AI acceptable-use policy, AI tool approval procedure, AI inventory and risk classification, vendor AI due-diligence questionnaire, AI literacy programme — aligned with the EU AI Act (Regulation (EU) 2024/1689 as amended by the Digital Omnibus on AI, Regulation (EU) 2026/1744), GDPR, confidentiality/privilege duties and sector rules (e.g. financial services outsourcing and ICT risk). Use when the user asks to "write an AI policy", "update our AI usage policy", "create an AI code of ethics", "classify our AI use cases under the AI Act", "assess this AI vendor", or "what does the AI Act require of us as a deployer".
---

# AI Governance Builder

Produces governance that people actually follow: principles-based where judgement is needed, rule-based where the law or confidentiality requires bright lines, and proportionate to the organisation's real AI use.

## Operating standard

- Read the current consolidated AI Act text on EUR-Lex before citing, and confirm the application dates as amended by Regulation (EU) 2026/1744. Baseline (verify): prohibited practices (Art 5) and AI literacy (Art 4) apply from 2 February 2025; the Omnibus reworded Art 4 into a duty to take measures to support AI literacy and added two prohibitions applicable from 2 December 2026; GPAI obligations from 2 August 2025; general application and Art 50 transparency from 2 August 2026; high-risk obligations deferred to 2 December 2027 (Annex III) and 2 August 2028 (Annex I).
- Distinguish legal obligations from good practice; label each policy clause with its driver (law / regulator expectation / internal choice).
- Fit the organisation: size, sector, regulated status, actual tools in use.

## Step 1 — Discovery

- **AI inventory:** tools in use (general-purpose assistants, coding assistants, embedded AI in SaaS, private/self-hosted models, agents with tool access), who uses them, for what, with what data.
- **Role under the AI Act** per system: provider (Art 3(3)), deployer (Art 3(4)), importer, distributor — note that substantially modifying or rebranding a system can make a deployer a provider.
- **Data:** personal data, special categories, client confidential data, privileged material, trade secrets, regulated data (e.g. financial supervisory information).
- **Existing frameworks:** information security, data protection, outsourcing/ICT third-party risk (e.g. DORA for financial entities), records retention, code of conduct.

## Step 2 — Risk classification of use cases

For each use case: prohibited (Art 5)? high-risk (Art 6 with Annexes I/III — e.g. employment/worker management, creditworthiness, access to essential services)? transparency obligations (Art 50 — chatbots, synthetic content, deepfakes)? GPAI integration? Otherwise minimal risk. Record reasoning and owner.

## Step 3 — Framework design

Recommend the document set and draft them:

1. **AI Code of Ethics (principles):** human accountability, lawfulness, transparency, fairness, privacy, security, confidentiality and privilege, accuracy and verification ("AI output is a draft until a human verifies it"), environmental awareness, and escalation. Each principle with *what it means in practice* and *examples*.
2. **AI Acceptable-Use Standard (rules):** approved-tools list and approval route; data classification matrix (what data may go into which tool tier — public, internal, confidential, restricted); prohibited uses; verification duties (citations, figures, code); disclosure of AI use to clients/counterparties where required; IP and output ownership; record-keeping.
3. **AI Tool Approval Procedure:** intake form, risk triage, vendor due diligence (training on customer data, retention, sub-processors, data location, security certifications, model-change notifications, audit rights, incident notification), DPIA trigger, sign-offs.
4. **AI Literacy Programme (Art 4):** role-based training, attestation, refresh cadence, evidence retention.
5. **Governance:** AI owner/committee, inventory maintenance, incident reporting, periodic review, link to enterprise risk register.

## Step 4 — Legal cross-checks

- GDPR: lawful basis, Art 22 automated decisions, DPIAs, transfers, processor terms.
- Confidentiality/privilege: legal team use of AI — privilege preservation, client consent where required.
- Employment law and works-council consultation where AI monitors or evaluates staff.
- Sector rules: financial-services outsourcing and ICT third-party risk; consumer-facing disclosures.
- Contract: customer contracts that restrict AI use on their data.

## Output

1. **Gap analysis** of the current policy (if provided) — clause | issue | driver | fix.
2. **Drafted documents** — Code of Ethics, Acceptable-Use Standard, Approval Procedure, Vendor DDQ, Literacy plan.
3. **AI use-case register** template pre-filled from discovery.
4. **Implementation plan** with owners and dates.
5. **Sources** (articles and dates verified).

## Boundaries

Not a conformity assessment for high-risk systems. Employment and works-council requirements are jurisdiction-specific — flag for local counsel.
