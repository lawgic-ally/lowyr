# Control-surface matrix

What to look for in code and on-chain state, and why it matters legally.

| Pattern / signal | Where to find it | What to verify on-chain | Legal relevance |
|---|---|---|---|
| `Ownable` / `owner()` | OpenZeppelin `Ownable`, custom `onlyOwner` modifiers | Current owner; EOA vs contract; renounced? | Identifiable controller; Recital 22 intermediary; issuer identification |
| `AccessControl` roles (`DEFAULT_ADMIN_ROLE`, `MINTER_ROLE`, `PAUSER_ROLE`…) | `grantRole`, `hasRole` | Role members via events (`RoleGranted`) | Who can mint/pause/upgrade — supply and asset control |
| Upgradeable proxy (UUPS, Transparent, Beacon, Diamond/EIP-2535) | `upgradeTo`, `ProxyAdmin`, EIP-1967 storage slots, `diamondCut` | Admin address; timelock in front? | Logic can change → "immutable" claims false; continuing control |
| Pause / freeze | `whenNotPaused`, `pause()`, `freeze(address)` | Holder; past use | Asset control; sanctions capability; custody arguments |
| Mint / burn authority | `mint()`, `burnFrom()`, supply caps | Holder; cap enforced in code? | Supply disclosure (Annex I Part F/G); dilution; misleading "fixed supply" |
| Blacklist / allowlist | `blacklist`, transfer hooks | Holder; list contents | Transferability statements (Art 6(5)(b)); sanctions compliance |
| Fee switch / parameters | `setFee`, fee recipients | Holder; current values | Revenue to identifiable persons → intermediary, possible profit-expectation signals |
| Oracle selection | `setOracle`, price feeds | Holder; feed source | Manipulation risk; control of outcomes |
| Emergency withdraw / sweep | `emergencyWithdraw`, `rescueTokens` | Holder | Ability to move user funds → custody characterisation |
| Multisig (Safe etc.) | Owner is a Safe | Threshold m-of-n; signer identities; signer independence | Degree of control; who are the "persons" |
| Timelock | `TimelockController` | Min delay; proposer/executor roles | Mitigates but does not remove control |
| Governance | Governor contracts, Snapshot + executor | Quorum, proposal thresholds, token concentration, delegate concentration | Real vs nominal decentralisation; governance-participant liability |
| Bridge validators / relayers | Validator set contracts, signature thresholds, off-chain relayers | Set membership; threshold; operator identities | Custody/transfer-service characterisation; exploit liability |
| Sequencer / off-chain infra | L2 sequencer, keepers, APIs | Operator | Censorship/ordering control; service provider identification |
| Front-end / domain | Hosting, ENS, geoblocking | Operator | Access control; marketing and reverse-solicitation footprint |
