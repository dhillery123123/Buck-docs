---
description: Protocol governance and value capture
---

# Governance Token

## Overview

Buck Protocol's governance token enables community ownership and aligns long-term holders with protocol success through governance rights and value accrual mechanisms.

{% hint style="info" %}
**Strategic Ambiguity**

Following the Ethena and Falcon playbooks, specific token details (name, supply, allocation percentages) will be announced closer to TGE. This page covers the planned governance structure and value accrual mechanisms.
{% endhint %}

## Earning Governance Tokens

The primary path to governance tokens is through the **Racks Program**. Racks earned during Season 1 convert to governance tokens at TGE.

See [Racks Program](points-program.md) for full earning details.

### Conversion Process

```
Your Allocation = (Your Racks ÷ Total Racks Earned) × Season 1 Pool
```

- **Pro-rata distribution** ensures fair allocation based on contribution
- **Conversion ratio** announced 2-4 weeks before TGE
- **Season 1 pool size** announced 4-6 weeks before TGE

## Value Accrual

### Revenue Allocation (Planned)

```
┌─────────────────────────────────────────────────────────────────┐
│                    PROTOCOL REVENUE                             │
│           (mint fees, redeem fees, time-weighted fees)          │
└─────────────────────────────────────────────────────────────────┘
                              │
            ┌─────────────────┼─────────────────┐
            │                 │                 │
            ▼                 ▼                 ▼
     ┌─────────────┐   ┌─────────────┐   ┌─────────────┐
     │   Token     │   │  Treasury   │   │  Insurance  │
     │  Buybacks   │   │ (Hard Asset │   │    Fund     │
     │             │   │ Acquisition)│   │             │
     └─────────────┘   └─────────────┘   └─────────────┘
            │                                   
            ▼                                   
     ┌─────────────┐                           
     │ Distributed │                           
     │ to token    │                           
     │  holders    │                           
     └─────────────┘                           
```

### How Buybacks Work

1. **Collection** — Fees accumulate in protocol treasury
2. **Execution** — Periodic automatic buybacks via DEX
3. **Distribution** — Purchased tokens distributed pro-rata to holders
4. **Transparency** — All transactions on-chain and verifiable

{% hint style="info" %}
**No Staking Required**

Unlike protocols that require staking to earn rewards, Buck distributes buybacks to ALL token holders automatically. Just hold tokens in your wallet.
{% endhint %}

## Token Holder Benefits

### What You Get

| Benefit | Details |
|---------|---------|
| **Buyback Distribution** | Pro-rata share of buybacks |
| **Governance Rights** | Vote on protocol parameters |
| **Future Season Boosts** | Multipliers in future Racks seasons |

### How It Works

```
Hold Governance Token
        │
        ├── Automatically receive buyback distributions
        ├── Vote on proposals (1 token = 1 vote)
        └── Boosted Racks in future seasons
```

No staking, no lockups, no cooldown periods. Just hold.

## Governance

### Voting Power

All token holders can vote. 1 token = 1 vote.

### Governance Scope

Token holders can vote on:

* **Protocol Parameters** — Collateralization ratios, fee structures
* **Revenue Allocation** — Adjustments to buyback/treasury/insurance split
* **Collateral Policy** — Approved collateral types and limits
* **Integration Approvals** — New DeFi protocol partnerships
* **Treasury Deployment** — Hard asset acquisition strategy
* **Upgrade Proposals** — Smart contract upgrades
* **Future Season Parameters** — Racks program adjustments

### Governance Process

```
1. Forum Discussion (3 days minimum)
         │
         ▼
2. Temperature Check (Snapshot, 2 days)
         │
         ▼
3. Formal Vote (On-chain, 5 days)
         │
         ▼
4. Execution (Timelock: 48 hours)
```

## Top Wallet Vesting

To prevent large holders from dumping at TGE, the top 2,000 wallets by Racks will have vesting requirements:

| Component | Details |
|-----------|---------|
| **Scope** | Top 2,000 wallets by Racks |
| **Split** | 50% at TGE / 50% vested |
| **Vesting Period** | 6 months linear |
| **Participation Requirement** | Must maintain protocol activity during vesting |

### Why Vesting?

- Prevents concentrated sell pressure at TGE
- Ensures large holders remain aligned post-launch
- Filters long-term believers from mercenary capital

Wallets outside the top 2,000 receive full allocation at TGE.

## Season Loyalty Program

Early participants receive ongoing benefits in future seasons:

| Participation | Future Season Boost |
|---------------|---------------------|
| Season 1 only | +10% Racks |
| Season 1 + 2 | +15% Racks |
| All seasons | Compounding |

This rewards long-term alignment over mercenary farming.

## How to Acquire Governance Tokens

1. **Racks Program** — Participate in [Season 1](points-program.md) to earn allocation
2. **DEX** — Purchase on Curve or Uniswap (post-TGE)
3. **Buyback Distributions** — Hold tokens to receive your share

## Timeline

```
NOW:        Season 1 Racks Program (8 weeks)
            └── Earn Racks through holding, LP, Morpho, referrals

PRE-TGE:    Token Details Announced
            └── Token name, supply, allocation % revealed
            └── Conversion ratio announced

TGE:        Token Generation Event
            └── Racks convert to governance tokens
            └── Top 2000 wallets: 50% immediate, 50% vesting

POST-TGE:   Governance & Value Accrual Live
            └── Hold tokens to receive buyback distributions
            └── Vote on protocol decisions
            └── Season 2 begins
```

## Competitive Context

| Protocol | Token | Revenue to Holders | Staking Required? |
|----------|-------|-------------------|-------------------|
| **Buck** | Governance | Buybacks | ❌ No |
| Maple | SYRUP | Buybacks | ❌ No |
| Ethena | ENA | TBD | ✅ Yes |
| Ondo | ONDO | None | N/A |

Buck follows the Maple model: hold tokens, receive value. No extra steps.

---

*Next: [Yield Mechanics →](../protocol/yield-mechanics.md)*
