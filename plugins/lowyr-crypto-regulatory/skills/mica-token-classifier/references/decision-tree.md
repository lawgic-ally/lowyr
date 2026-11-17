# MiCA classification decision tree (baseline)

Baseline verified 17 November 2026 against EUR-Lex and the ESMA Interactive Single Rulebook. Re-verify each node before relying on it.

```mermaid
flowchart TD
    A["Digital asset"] --> B{"Crypto-asset?<br/>Art 3(1)(5)"}
    B -- No --> Z0["Outside MiCA<br/>check e-money / PSD / consumer law"]
    B -- Yes --> C{"Unique and non-fungible?<br/>Art 2(3), Rec. 10-11"}
    C -- Yes --> Z1["Outside MiCA<br/>re-test fractionalisation and series"]
    C -- No --> D{"Financial instrument?<br/>Art 2(4)(a), Art 2(5)<br/>ESMA75453128700-1323"}
    D -- Yes --> Z2["MiFID II / Prospectus / MAR regime"]
    D -- No --> E{"Other Art 2(4) exclusion?<br/>deposit, funds, securitisation, pension/insurance"}
    E -- Yes --> Z3["Sectoral regime"]
    E -- No --> F{"Stable value by reference<br/>to ONE official currency?<br/>Art 3(1)(7)"}
    F -- Yes --> G["EMT - Title IV<br/>Art 48 issuer restriction; Art 51 white paper"]
    F -- No --> H{"Stable value by reference to<br/>other value/right/combination?<br/>Art 3(1)(6)"}
    H -- Yes --> I["ART - Title III<br/>Art 16 authorisation; Art 19 white paper"]
    H -- No --> J["Other crypto-asset - Title II"]
    J --> K{"ONLY access to issuer's<br/>good or service?<br/>Art 3(1)(9)"}
    K -- Yes --> L["Utility token<br/>check Art 4(3)(c) / Art 4(6)"]
    K -- No --> M["Other Title II crypto-asset"]
    L --> N{"Offer to the public?<br/>Art 3(1)(12)"}
    M --> N
    N -- Yes --> O{"Art 4(2) / 4(3) exemption?<br/>lost under Art 4(4)"}
    O -- No --> P["White paper Arts 6, 8, 9<br/>marketing Art 7; offeror Art 14"]
    O -- Yes --> Q["Exempt offer - document basis<br/>monitor Art 4(4) triggers"]
    N -- No --> R["No Title II offer duties<br/>check admission to trading (Art 5)<br/>and CASP services"]
```

## Node checklist

| Node | Key evidence to collect |
|---|---|
| Crypto-asset | DLT record, transferability, storage |
| Unique/non-fungible | Uniqueness of token AND of underlying right; series size; fractionalisation; secondary-market behaviour |
| Financial instrument | Profit/revenue rights, voting on issuer, repayment claims, negotiability, standardisation, derivatives features |
| EMT | Peg target, redemption promise, marketing language |
| ART | Basket/commodity/crypto reference, reserve, stabilisation mechanism |
| Utility token | Exclusivity of access function; good/service live or not |
| Offer to the public | Communication + sufficient information to decide to purchase; persons targeted; Member States |
| Exemptions | Counting persons per MS, consideration over 12 months, qualified investors, free vs data/fees, limited network size |
