# lowyr-legal-ops

Legal operations for in-house teams: AI governance (EU AI Act-aligned code of ethics, acceptable use, vendor due diligence) and risk-based legal intake triage that routes work to the right skill.

Part of the [lowyr](../../README.md) marketplace by Bastien Choquez.

## Install

```
/plugin marketplace add lawgic-ally/lowyr
/plugin install lowyr-legal-ops@lowyr
```

## Skills

| Skill | Purpose |
|---|---|
| `ai-governance-builder` | Draft or review an organisation's AI governance framework — AI code of ethics, AI acceptable-use policy, AI tool approval procedure, AI inventory and risk classification, vendor AI due-diligence questionnaire, AI literacy programme — aligned with the EU AI Act (Regulation (EU) 2024/1689 as amended by the Digital Omnibus on AI, Regulation (EU) 2026/1744), GDPR, confidentiality/privilege duties and sector rules (e.g. financial services outsourcing and ICT risk). |
| `legal-intake-triage` | Triage incoming requests to an in-house legal team (from Slack, email, tickets or forms) — classify the matter type, extract facts, rate risk and urgency, set an SLA, identify missing information, route to the right owner or specialist skill, and draft the first response to the requester. |

Every skill re-verifies statutory references against primary sources at run time. The verified baseline is in [docs/citation-register.md](../../docs/citation-register.md). Not legal advice; see [DISCLAIMER.md](../../DISCLAIMER.md).
