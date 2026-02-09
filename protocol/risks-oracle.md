---
description: Understanding oracle infrastructure and market hours risks
---

# Oracle & Market Hours Risk

## Market Hours Gap

STRC trades on NASDAQ during U.S. market hours only (~32.5 hours/week). DeFi operates 24/7. This creates pricing gaps, particularly over weekends and holidays.

| Period | STRC Price Source |
|--------|-------------------|
| **Market hours** | Live NASDAQ feed via RedStone |
| **Off-hours** | Last market close price (static) |

## Oracle Architecture

Buck uses RedStone oracles with custom STRC handling:

- **30-minute TWAP smoothing** — prevents flash crashes from triggering liquidations
- **Circuit breakers** — operations pause if STRC moves >25% in 24 hours or if the oracle feed goes stale >2 hours
- **NASDAQ-based pricing** — immune to DEX manipulation; NASDAQ manipulation is securities fraud

### Off-Hours Behavior

During market close, BUCK minting and redemption use the last close price. Transfers continue normally. When markets reopen, live pricing resumes and TWAP incorporates new prices within 30 minutes.

## Liquidation Protection (Morpho)

For lending integrations, Buck mitigates overnight gap risk with:

- Conservative LTV parameters accounting for overnight gaps
- TWAP smoothing prevents instant liquidations at market open
- Treasury LP provides liquidation liquidity

## Oracle Contract

| Contract | Address |
|----------|---------|
| Oracle Adapter | `0xa6c5f4D041192C2019E77f679eA02e9684235Fd9` |

---

*Next: [Smart Contract & Operational Risk →](risks-smart-contract.md)*
