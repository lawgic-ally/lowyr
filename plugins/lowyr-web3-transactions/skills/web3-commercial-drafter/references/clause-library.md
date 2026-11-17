# Web3 clause library

Model clauses for adaptation. Square brackets are commercial variables or options. Each clause is followed by negotiation notes. These are starting points — adapt to the governing law and the deal; do not paste unreviewed.

---

## 1. Definitions (extract)

**"Applicable Crypto Regulation"** means any law, regulation, rule, guidance or binding requirement of a Regulator applicable to crypto-assets, crypto-asset services or distributed ledger technology in any jurisdiction relevant to the performance of this Agreement, including [Regulation (EU) 2023/1114 (MiCA)] [and the Financial Services and Markets Act 2000 and instruments made under it], each as amended or replaced from time to time.

**"Chain Event"** means any (a) hard fork, soft fork or chain split of the Network; (b) suspension, halt, reorganisation or material degradation of the Network; (c) exploit, hack or unauthorised minting affecting the Token or any bridge or smart contract on which performance depends; or (d) migration, redenomination or replacement of the Token.

**"Regulatory Event"** means (a) any change in, or change in the interpretation or application of, Applicable Crypto Regulation; (b) any statement, guidance, warning, enforcement action or request of a Regulator; or (c) the refusal, suspension, withdrawal or variation of any Authorisation, in each case which [makes it unlawful for a Party to perform] [materially adversely affects a Party's ability to perform] any obligation under this Agreement.

## 2. Token-denominated consideration

> The [Fee] shall be paid in [Token] in an amount equal to [EUR amount] divided by the Reference Price. "Reference Price" means the [24-hour volume-weighted average price] of [Token] against [EUR/USD] on [named venues] for the [period] ending on [the Business Day before the payment date], as published by [data provider]. If the Reference Price cannot be determined, or if the [Token] has suffered a Chain Event, the Fee shall be paid in [EUR] [within [10] Business Days].

*Notes:* Payee prefers fiat fallback and short valuation windows; payer prefers longer VWAP windows and a collar (e.g. ±[20]%) beyond which the parties renegotiate. Address lock-ups and whether the payee may hedge.

## 3. Regulatory Event

> 3.1 Each Party shall notify the other promptly on becoming aware of a Regulatory Event.
> 3.2 Following a Regulatory Event, the Parties shall negotiate in good faith for [30] days such amendments as are necessary to comply with Applicable Crypto Regulation while preserving, as far as possible, the commercial intent of this Agreement.
> 3.3 Pending such amendment, either Party may suspend performance of any affected obligation to the extent required to comply with Applicable Crypto Regulation.
> 3.4 If no amendment is agreed within that period, or if performance would be unlawful, either Party may terminate this Agreement [in respect of the affected jurisdiction] on written notice without liability other than for accrued rights.
> 3.5 Nothing in this Agreement requires a Party to carry on any activity for which it does not hold the necessary Authorisation.

*Notes:* Resist counterparty attempts to make "Regulatory Event" turn on its sole opinion; require an objective test or legal-advice threshold. Clause 3.5 prevents accidental commitment to a regulated activity.

## 4. Authorisations

> Each Party represents and warrants that it holds, and covenants to maintain, all Authorisations required for the performance of its obligations, as listed in Schedule [X], and shall notify the other Party within [2] Business Days of any refusal, suspension, withdrawal, variation or material regulatory condition relating to them.

*Notes:* For non-authorised counterparties, add a covenant not to market or solicit in jurisdictions where they are not authorised and not to rely on reverse solicitation on the other Party's behalf.

## 5. Chain Events

> Upon a Chain Event: (a) [Party A] shall, acting reasonably and after consultation, determine which chain or token is the canonical [Token] for the purposes of this Agreement, having regard to [the position adopted by the issuer, majority node operators and the principal trading venues]; (b) neither Party shall be obliged to support any fork or airdropped asset; (c) affected timelines are extended for the duration of the Chain Event; and (d) if the Chain Event continues for more than [30] days, either Party may terminate.

## 6. Smart-contract risk allocation

> [Provider] shall (a) procure an independent security audit of the Smart Contracts before deployment and after any material upgrade, (b) remediate all critical and high findings before deployment, (c) maintain [multi-signature / timelock] controls over any administrative function, and (d) notify [Customer] of any exploit within [24] hours. Losses arising from an exploit shall be borne by [the Party whose code or controls were exploited] [subject to the cap in clause [X]].

## 7. Sanctions and AML

> Each Party represents that neither it nor any of its controllers, directors or officers is a Sanctioned Person, and shall not (directly or indirectly) make any crypto-asset or funds available to or for the benefit of a Sanctioned Person. Each Party shall screen counterparty wallet addresses using a reputable blockchain analytics provider and cooperate in providing originator and beneficiary information required by applicable transfer-of-funds rules.

## 8. Marketing

> No Party shall publish any marketing communication relating to the other Party, the Token or this Agreement without the other Party's prior written approval. Each Party is responsible for ensuring that its marketing communications comply with applicable law, including rules on crypto-asset marketing communications and financial promotions in each jurisdiction where they are disseminated, and shall not make any statement as to the future value of any crypto-asset.

## 9. Liability carve-outs

> Neither Party excludes or limits liability for (a) fraud or fraudulent misrepresentation, (b) wilful misconduct, (c) breach of clause [Sanctions], (d) breach of clause [Confidentiality] or [Data Protection], or (e) [indemnified IP claims]. Subject to that, neither Party is liable for any loss of profit, loss of opportunity, or diminution in the market value of any crypto-asset.

## 10. MoU binding/non-binding split

> Save for clauses [Confidentiality], [Exclusivity], [Costs], [Governing Law and Jurisdiction] and this clause, which are legally binding, this Memorandum is a statement of the Parties' present intentions and does not create legally binding obligations. No Party shall be bound to proceed with the Transaction until definitive agreements have been executed.
