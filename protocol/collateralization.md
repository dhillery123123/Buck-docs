---
description: How BUCK is backed by STRC
---

# How Buck is Backed

## STRC: The Sole Collateral

BUCK is backed by **STRC** — Strategy's perpetual preferred stock (NASDAQ: STRC). The protocol holds STRC in its treasury and maintains a USDC liquidity reserve for instant redemptions, when approved.

## Backing Structure

| Component             | Purpose                       | Composition                     |
| --------------------- | ----------------------------- | ------------------------------- |
| **STRC Treasury**     | Yield generation + collateral | STRC (Strategy preferred stock) |
| **Liquidity Reserve** | Instant redemptions           | USDC                            |

### How BUCK is Valued

```
BUCK NAV = f(STRC Treasury Value, Accrued Yield)
```

BUCK's price reflects the value of the underlying STRC holdings plus accrued yield from the yield stream. BUCK holders have full exposure to STRC price movements — when STRC rises, BUCK's NAV rises; when STRC falls, BUCK's NAV falls.

STRC is Strategy's perpetual preferred stock — SEC-regulated, NASDAQ-listed, with $2.25B in cash reserves covering 77+ years of dividends. For full STRC details, see [Yield Overview](../yield/overview.md#what-is-strc).

### Layered Protection

```
Layer 1: STRC dividends are contractually obligated (preferred equity)
         ↓
Layer 2: Strategy has $2.25B cash to cover 77+ years of dividends
         ↓
Layer 3: Strategy holds $60B+ in Bitcoin (backing for STRC)
         ↓
Layer 4: Buck Protocol maintains USDC liquidity reserve for redemptions
```

## Independent Verification

### The Network Firm (Monthly Attestations)

Buck's reserves are independently verified monthly by The Network Firm:

| Verified Item        | Description               |
| -------------------- | ------------------------- |
| **STRC Holdings**    | Quantity and USD value    |
| **USDC Reserve**     | Liquidity reserve balance |
| **BUCK Supply**      | Total outstanding tokens  |
| **Backing Ratio**    | Calculated and confirmed  |

For on-chain verification and key addresses, see [Independent Reserve Attestations](reserve-attestations.md) and [Smart Contracts](../technical/contracts.md).

## Security

| Measure             | Details                                           |
| ------------------- | ------------------------------------------------- |
| **STRC Custody**    | Alpaca brokerage account (entity: Buck Assets Ltd.) |
| **On-chain Control**| MPC wallet with ADMIN_ROLE verified on-chain      |
| **Audits**          | Cyfrin, Spearbit, SSC                             |
| **Attestations**    | Monthly by The Network Firm                       |
| **Smart contracts** | UUPS proxy with 48-hour timelock                  |

***

_Next:_ [_Risk Framework →_](risks.md)
