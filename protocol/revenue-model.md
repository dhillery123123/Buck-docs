---
description: Protocol economics and value distribution
---

# Revenue Model

## Overview

Buck Protocol generates revenue through fees on minting, redemption, and transactions. This revenue is distributed across three purposes: future governance token holders, STRC accumulation, and protocol insurance.

## Revenue Allocation

```
┌─────────────────────────────────────────────────────────────────┐
│                    TOTAL PROTOCOL REVENUE                       │
│                                                                 │
│    Mint Fees  +  Redeem Fees  +  Time-Weighted Fees  +  Other  │
└─────────────────────────────────────────────────────────────────┘
                              │
                              │ 100%
                              ▼
          ┌───────────────────┼───────────────────┐
          │                   │                   │
          ▼                   ▼                   ▼
   ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
   │     25%     │     │     50%     │     │     25%     │
   │             │     │             │     │             │
   │  Governance │     │  Treasury   │     │  Insurance  │
   │   Token     │     │   (STRC     │     │    Fund     │
   │  Buyback &  │     │ Acquisition)│     │             │
   │    Burn     │     │             │     │             │
   └─────────────┘     └─────────────┘     └─────────────┘
```

## Fee Schedule

### Standard Fees

| Action | Fee |
|--------|-----|
| Mint (normal) | 10 bps |
| Redeem (normal) | 30 bps |

## 25% → Governance Token Buyback & Burn

Buck Protocol will launch a governance token. From day one, we're committing to use **25% of all protocol revenue** to:

1. **Buy** governance tokens from the open market
2. **Burn** them permanently, reducing total supply

This creates continuous buy pressure and deflation — the more the protocol earns, the more tokens get burned.

{% hint style="info" %}
**Deflationary by Design**

Unlike protocols that promise future "fee switches," we're building token burns into the protocol from launch.
{% endhint %}

### Competitive Comparison

| Protocol | Revenue to Token Holders | Mechanism |
|----------|-------------------------|-----------|
| **Buck** | **25%** | Buyback & burn |
| Maple (SYRUP) | 25% | Buybacks + staking |
| Ethena (ENA) | TBD | Fee switch pending |
| Ondo (ONDO) | 0% | None |

## 50% → Treasury (STRC Acquisition)

### Purpose

Half of protocol revenue funds **STRC accumulation**:

* **More Yield** — More STRC = more dividends = faster BUCK growth
* **Liquidity Moat** — Large position makes replication expensive
* **Stronger Backing** — Higher collateralization protects holders

### Flywheel Effect

```
Protocol Revenue
      │
      ▼
50% → Treasury → Buys More STRC
                      │
                      ▼
               More STRC Holdings
                      │
                      ▼
               Higher Dividend Income
                      │
                      ▼
               Faster BUCK Price Growth
                      │
                      ▼
               More BUCK Demand
                      │
                      ▼
               More Protocol Revenue
                      │
                      └──────────────────┐
                                         │
      ┌──────────────────────────────────┘
      │
      ▼
   (Repeat)
```

## 25% → Insurance Fund

### Purpose

The Insurance Fund provides protocol protection:

* **Redemption Backstop** — Ensure all redemptions honored
* **Price Defense** — Buy BUCK if trading below fair value
* **Black Swan Protection** — General protocol safety net

### Deployment Rules

| Trigger | Action | Limit |
|---------|--------|-------|
| Redemption stress | Provide liquidity | As needed |
| BUCK < 99% of fair value | Market buy | Up to 25% |
| Emergency | Protocol discretion | Up to 50% |

### Fund Management

* **Composition** — USDC, USDT (stablecoins only)
* **Custody** — Multi-sig controlled
* **Transparency** — Balance publicly visible
* **Governance** — Deployment rules adjustable via vote

## Revenue Projections

### By TVL

| TVL | Annual Revenue | To Buyback/Burn (25%) | To Treasury (50%) | To Insurance (25%) |
|-----|----------------|----------------------|-------------------|-------------------|
| $10M | $200K | $50K | $100K | $50K |
| $50M | $1M | $250K | $500K | $250K |
| $100M | $2M | $500K | $1M | $500K |
| $500M | $10M | $2.5M | $5M | $2.5M |
| $1B | $20M | $5M | $10M | $5M |

*Revenue = 1% yield spread (STRC 11% - 10% pass-through) + 1% annual transaction fees*

## Stakeholder Alignment

### For BUCK Holders

* **50% to Treasury** — More STRC = faster value growth
* **25% to Insurance** — Protection for redemptions
* **Net Effect** — Sustainable, protected growth

### For Future Governance Token Holders

* **25% to Buyback & Burn** — Continuous deflation
* **Governance rights** — Shape protocol direction
* **Net Effect** — Protocol success = increasing scarcity

---

*Next: [Risk Framework →](risks.md)*
