---
description: How BUCK is backed by STRC
---

# How Buck is Backed

## STRC: The Sole Collateral

BUCK is backed by **STRC** — Strategy's perpetual preferred stock (NASDAQ: STRC). The protocol holds STRC in its treasury and maintains a USDC liquidity reserve for instant redemptions, when approved.&#x20;

## Backing Structure

| Component             | Purpose                       | Composition                     |
| --------------------- | ----------------------------- | ------------------------------- |
| **STRC Treasury**     | Yield generation + collateral | STRC (Strategy preferred stock) |
| **Liquidity Reserve** | Instant redemptions           | USDC                            |

### Collateralization Ratio

```
Collateralization Ratio = (STRC Treasury Value + USDC Reserve) / (BUCK Supply x BUCK Price)

Current Target: 100%+
```

STRC is Strategy's 10% perpetual preferred stock — SEC-regulated, NASDAQ-listed, with $2.25B in cash reserves covering 77+ years of dividends. For full STRC details, see [Yield Overview](../yield/overview.md#what-is-strc).

### Layered Protection

```
Layer 1: STRC dividends are contractually obligated (preferred equity)
         ↓
Layer 2: Strategy has $2.25B cash to cover 77+ years of dividends
         ↓
Layer 3: Strategy holds $60B+ in Bitcoin (5x overcollateral for STRC)
         ↓
Layer 4: Buck Protocol maintains 100%+ collateral ratio on top of all this
```

## Independent Verification

### The Network Firm (Monthly Attestations)

Buck's reserves are independently verified monthly by The Network Firm:

| Verified Item        | Description               |
| -------------------- | ------------------------- |
| **STRC Holdings**    | Quantity and USD value    |
| **USDC Reserve**     | Liquidity reserve balance |
| **BUCK Supply**      | Total outstanding tokens  |
| **Collateral Ratio** | Calculated and confirmed  |

For on-chain verification and key addresses, see [Independent Reserve Attestations](reserve-attestations.md) and [Smart Contracts](../technical/contracts.md).

## Security

| Measure             | Details                                           |
| ------------------- | ------------------------------------------------- |
| **Custody**         | Fireblocks institutional custody                  |
| **Multi-sig**       | Treasury controlled by multi-signature MPC wallet |
| **Audits**          | Cyfrin, Halborn, Spearbit                         |
| **Attestations**    | Monthly by The Network Firm                       |
| **Smart contracts** | UUPS proxy with 48-hour timelock                  |

***

_Next:_ [_Risk Framework →_](risks.md)
