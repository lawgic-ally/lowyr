---
name: protocol-legal-review
description: Read smart-contract code (Solidity/Vyper/Rust) or protocol documentation and translate technical control features — admin/owner keys, upgradeability proxies, pause/freeze, mint/burn authority, blacklists, fee switches, oracles, bridge validators/relayers, multisigs, governance and timelocks, front-end gating — into legal consequences, namely decentralisation claims (MiCA Recital 22), custody and transfer-service characterisation, issuer/offeror identification, white-paper and marketing disclosure gaps, sanctions/AML capability, and liability. Use when the user shares a contract address, repo, audit report or docs and asks "is this really decentralised", "who controls this protocol", "does the bridge operator custody funds", "are our disclosures accurate", or "what's our legal exposure from this contract design".
---

# Protocol Legal Review

Regulators and courts look past architecture to **who can do what**. This skill builds a control map from the code and docs, then tests every legal claim the project makes against it.

## Operating standard

- **Evidence from code first.** Prefer verified source (block explorer, repo at a pinned commit) and on-chain state (current owner/admin addresses, multisig thresholds, timelock delays) over documentation. Record commit hashes, addresses and block numbers.
- If code or on-chain state cannot be accessed, say so and mark findings as *documentation-based only*.
- This is a **legal** review of control and disclosure, not a security audit. Note obvious security issues and route them to `web3-legal-expert` (audit mode).
- Legal citations verified at run time against primary sources.

## Step 1 — Scope

Contracts and chains in scope; deployed addresses; repo/commit; audits available; documentation (white paper, docs site, terms of use, governance forum); the legal question(s) being asked; jurisdictions.

## Step 2 — Control-surface inventory

Load `references/control-surface-matrix.md`. For each contract, enumerate privileged functions and roles:

| Contract | Function / role | Who holds it (address, EOA vs multisig m-of-n, DAO, timelock) | Delay | What it can do to users/assets | Legal relevance |
|---|---|---|---|---|---|

Cover: ownership/admin roles (`Ownable`, `AccessControl`), proxy upgrade authority (UUPS/Transparent/Beacon/Diamond), `pause`/`freeze`, `mint`/`burn`, blacklist/allowlist, fee parameters and recipients, oracle selection, emergency withdrawals, bridge validator/relayer sets and signature thresholds, governance proposal/execution rights and quorum, token-holder concentration, and off-chain controls (front-end, API, sequencer).

## Step 3 — Control assessment

Rate decentralisation on four axes, with evidence: **(1) Code control** (can anyone change logic?), **(2) Asset control** (can anyone move, freeze or mint user assets?), **(3) Parameter control** (fees, collateral, oracles), **(4) Access control** (who can use it; front-end gating; geoblocking). Identify the persons/entities behind each key (team, foundation, service provider) — these are candidate "intermediaries".

## Step 4 — Legal mapping

| Question | Analysis |
|---|---|
| Fully decentralised without any intermediary? (MiCA Recital 22) | Any retained control by an identifiable person over the service → partial decentralisation is in scope. Name the persons. |
| Custody? (MiCA Art 3(1)(17), Art 75) | Does anyone hold private keys or means of access enabling control of users' assets (incl. bridge multisigs, MPC shares, upgradeable vaults)? |
| Transfer services? (Art 3(1)(26), Art 82) | Does an operator effect transfers on behalf of users (relayers, bridges, gasless meta-tx)? |
| Other services (exchange, execution, RTO, platform)? | Route to `casp-perimeter-mapper` with the control map. |
| Issuer / offeror identification | Who can mint, who deployed, who markets — for white-paper responsibility and Art 15 liability. |
| Disclosure accuracy | Compare control map with white paper (Annex I Parts F–I), docs, marketing ("immutable", "non-custodial", "trustless", "community-owned"). Each mismatch is a misleading-statement risk. |
| Sanctions / AML capability | If the team *can* freeze or block, regulators may expect it to; if it cannot, document why. Consider TFR obligations of any CASP in the flow. |
| Liability and governance | Unincorporated-association/partnership risk for governance participants; duty-of-care arguments against key holders; DAO wrapper adequacy (route to `web3-legal-expert`). |
| Data protection | Personal data written on-chain; controller identification; erasure conflict. |

## Step 5 — Remediation options

For each material finding: technical options (renounce/burn roles, timelocks, raise multisig thresholds and diversify signers, governance migration, immutable deployment, on-chain disclosure of roles) and legal options (accurate disclosure, licensing the controlling entity, contractual allocation, terms-of-use updates, insurance). Show the trade-off between decentralisation and the ability to respond to exploits/sanctions.

## Output

1. **Bottom line** — who controls the protocol, and the three most important legal consequences.
2. **Control map** (table + Mermaid diagram of roles and keys).
3. **Legal mapping table** with risk ratings.
4. **Disclosure gap list** — statement | where | reality per code | fix.
5. **Remediation plan** (technical + legal).
6. **Evidence log** — addresses, commits, block numbers, sources.

## Boundaries

Not a security audit or a guarantee of code behaviour. Findings are as of the block/commit reviewed.
