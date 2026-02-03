---
description: Earn Racks toward Buck's governance token
---

# Racks Program

## Season 1 Overview

Buck Racks rewards early participants with governance token allocation. Season 1 runs for **8 weeks** with rewards distributed based on participation across holding, liquidity provision, lending, and referrals.

{% hint style="success" %}
**Dual Rewards: Racks + BUCK**

During Season 1, earn both Racks (future governance tokens) AND direct BUCK rewards through our Merkl campaign. This is the highest-reward period in Buck's history.
{% endhint %}

## How Racks Work

Racks are points that convert to governance tokens at TGE. The longer you hold and the more you contribute to the protocol, the more Racks you earn.

**No staking required.** Buck streams yield automatically via STRC dividends. Racks multipliers are earned simply by holding longer—no lock contracts, no commitments, just hold.

## Earning Structure

### Base Rate

**1 Rack per $10 BUCK per day**

A $10,000 BUCK position earns 1,000 Racks per day at the base rate.

### Activity Weights

Racks are distributed across four activities:

| Activity | Weight | Description |
|----------|--------|-------------|
| **Hold BUCK** | 50% | Simply hold BUCK in your wallet |
| **Liquidity Provision** | 30% | Provide LP to Curve or Uniswap BUCK pools |
| **Morpho Lending** | 10% | Supply BUCK to Morpho lending markets |
| **Referrals** | 10% | Refer new users who mint BUCK |

### Multipliers

#### Hold Duration Multipliers

The longer you hold continuously, the higher your multiplier:

| Hold Duration | Multiplier | Daily Racks ($10K) |
|---------------|------------|-------------------|
| 0-29 days | 1x | 1,000 |
| 30-89 days | 5x | 5,000 |
| 90-179 days | 10x | 10,000 |
| 180+ days | 20x | 20,000 |

**How it works:** Your multiplier increases automatically based on how long you've held continuously. If you sell or transfer, your timer resets to zero.

#### Activity Multipliers

| Activity | Base Multiplier |
|----------|-----------------|
| Hold BUCK | 1x |
| Curve LP | 3x |
| Uniswap V3 LP | 3x |
| Morpho Lending | 3x |

{% hint style="warning" %}
**Multipliers Do NOT Stack**

You earn either the hold duration multiplier OR the activity multiplier—whichever applies to that position. A Curve LP position earns 3x, not 3x × hold duration.
{% endhint %}

## Earning Examples

Based on 1 Rack per $10/day base rate:

| Scenario | Multiplier | Daily Racks | 8-Week Total |
|----------|------------|-------------|--------------|
| $10K BUCK, just started | 1x | 1,000 | 56,000 |
| $10K BUCK, held 30+ days | 5x | 5,000 | 280,000 |
| $10K BUCK, held 90+ days | 10x | 10,000 | 560,000 |
| $10K BUCK, held 180+ days | 20x | 20,000 | 1,120,000 |
| $10K in Curve LP | 3x | 3,000 | 168,000 |
| $10K in Morpho | 3x | 3,000 | 168,000 |

## Referral Program

Earn **10% of your referees' Racks** on an ongoing basis.

| Component | Details |
|-----------|---------|
| **Platform** | Sharemint |
| **Bonus** | 10% of referee's Racks |
| **Qualifying Action** | Referee mints $100+ BUCK via buck.io |
| **Duration** | Ongoing (as long as referee earns) |

Referrals only count for direct mints through buck.io—DEX purchases don't qualify.

## Merkl BUCK Rewards (Running Concurrently)

Alongside Racks, Season 1 includes direct BUCK distributions via Merkl:

| Pool | Weekly BUCK | 8-Week Total | Est. APY* |
|------|-------------|--------------|-----------|
| **BUCK Holders** | $6,250 | $50,000 | ~75% |
| **Curve LP** | $4,167 | $33,333 | ~50% |
| **Uniswap LP** | $2,083 | $16,667 | ~50% |
| **Total** | $12,500 | $100,000 | — |

*APY estimates at $500K TVL. Actual rates depend on total participation.

{% hint style="info" %}
**Two Reward Streams**

During Season 1, you earn BOTH:
1. **Racks** → Convert to governance tokens at TGE
2. **BUCK** → Immediate value via Merkl, claimable weekly
{% endhint %}

## Season 1 Parameters

| Parameter | Value |
|-----------|-------|
| **Duration** | 8 weeks |
| **Minimum Participation** | $100 BUCK |
| **Base Rate** | 1 Rack per $10/day |
| **Referral Bonus** | 10% of referee's Racks |
| **Tracking** | Daily snapshots via Absinthe |

## Converting Racks to Governance Tokens

### Pro-Rata Distribution

Your governance token allocation is calculated as:

```
Your Allocation = (Your Racks ÷ Total Racks Earned) × Season 1 Pool
```

The exact Season 1 pool size (% of total token supply) will be announced closer to TGE.

### Why Pro-Rata?

Pro-rata distribution ensures:
- Predictable total dilution
- Rewards relative contribution fairly
- No gaming through last-minute deposits

## Anti-Gaming Measures

### Daily Snapshots

Racks are calculated using daily balance snapshots. This prevents:
- Last-minute deposits before snapshots
- Flash loan manipulation
- Cross-protocol arbitrage

### Minimum Balance

$100 minimum BUCK balance required to earn Racks. Filters dust wallets and reduces sybil attacks.

### Continuous Holding

Hold duration multipliers require **continuous** holding. Any break (selling, transferring out) resets your timer to zero.

## How to Participate

### Step 1: Get BUCK

```
1. Go to buck.io
2. Connect wallet
3. Mint BUCK with USDC
   —or—
   Buy on Curve/Uniswap
```

### Step 2: Choose Your Strategy

| Strategy | Risk | Reward | Best For |
|----------|------|--------|----------|
| **Hold BUCK** | Low | Up to 20x (at 180 days) | Patient holders |
| **Curve LP** | Medium | 3x + trading fees | Active DeFi users |
| **Morpho Lending** | Medium | 3x + lending yield | Yield optimizers |
| **Refer Friends** | None | 10% of referee's Racks | Community builders |

### Step 3: Track Progress

Racks dashboard at buck.io/racks. Your position is tracked on-chain via daily snapshots.

## Infrastructure

| Component | Platform | Purpose |
|-----------|----------|---------|
| **Racks Tracking** | [Absinthe Network](https://absinthe.network) | On-chain activity tracking, leaderboard |
| **Referrals** | [Sharemint](https://sharemint.com) | Referral links, 10% bonus tracking |
| **BUCK Rewards** | [Merkl](https://merkl.xyz) | Direct BUCK distributions |

## Season Timeline

```
SEASON 1: 8 WEEKS
├── Racks:  Earn based on holding, LP, Morpho, referrals
├── Merkl:  $12,500/week BUCK rewards
└── Goal:   Bootstrap TVL + liquidity for Morpho approval

TGE: Following Season 1
├── Racks convert to governance tokens
├── Conversion ratio announced pre-TGE
└── Season 2 begins
```

## Competitive Context

Buck Racks draws from proven models:

| Protocol | Program | Duration | Model |
|----------|---------|----------|-------|
| **Ethena** | Shards | ~6 weeks | Shards → ENA |
| **Falcon** | Miles | Ongoing | Miles → FF |
| **Buck** | Racks | 8 weeks | Racks → Governance |

We designed Racks with strategic ambiguity on token details (following Ethena's playbook) while providing clear earning mechanics.

## Contract Addresses

| Contract | Address |
|----------|---------|
| **BUCK Token** | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` |
| **Liquidity Window (Mint)** | `0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E` |

---

*Next: [Governance →](governance.md)*
