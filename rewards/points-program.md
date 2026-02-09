---
description: Earn Points toward Buck's protocol allocation
---

# Points Program

## Season 1 Overview

Buck Points rewards early participants with protocol allocation. Season 1 runs for **8 weeks** with rewards distributed based on participation across holding, liquidity provision, lending, and referrals.

{% hint style="success" %}
**Dual Rewards: Points + BUCK**

During Season 1, earn both Points (future protocol allocation) AND direct BUCK rewards through our Merkl campaign. This is the highest-reward period in Buck's history.
{% endhint %}

## How Points Work

Points convert to protocol allocation at TGE. The longer you hold and the more you contribute to the protocol, the more Points you earn.

**No staking required for Points.** Points multipliers are earned simply by holding longer — no lock contracts, no commitments. Just hold BUCK to accrue Points automatically. (Note: STRC yield is distributed automatically on the 15th of each month.)

## Earning Structure

### Base Rate

**1 Point per $10 BUCK per day**

A $10,000 BUCK position earns 1,000 Points per day at the base rate.

### Activity Weights

Points are distributed across four activities:

| Activity                | Weight | Description                               |
| ----------------------- | ------ | ----------------------------------------- |
| **Hold BUCK**           | 50%    | Simply hold BUCK in your wallet           |
| **Liquidity Provision** | 30%    | Provide LP to Curve BUCK pools            |
| **Morpho Lending**      | 10%    | Supply BUCK to Morpho lending markets     |
| **Referrals**           | 10%    | Refer new users who mint BUCK             |

### Multipliers

#### Hold Duration Multipliers

The longer you hold continuously, the higher your multiplier:

| Hold Duration | Multiplier | Daily Points ($10K) |
| ------------- | ---------- | ------------------- |
| 0-29 days     | 1x         | 1,000               |
| 30+ days      | 5x         | 5,000               |

**How it works:** Your multiplier increases automatically based on how long you've held continuously. If you sell or transfer, your timer resets to zero.

#### Activity Multipliers

| Activity       | Base Multiplier |
| -------------- | --------------- |
| Hold BUCK      | 1x              |
| Curve LP       | 3x              |
| Morpho Lending | 3x              |

{% hint style="warning" %}
**Multipliers Do NOT Stack**

You earn either the hold duration multiplier OR the activity multiplier—whichever applies to that position. A Curve LP position earns 3x, not 3x × hold duration.
{% endhint %}

## Earning Examples

Based on 1 Point per $10/day base rate:

| Scenario             | Multiplier | Daily Points | 8-Week Total |
| -------------------- | ---------- | ------------ | ------------ |
| $10K BUCK, 0-29 days | 1x         | 1,000        | 56,000       |
| $10K BUCK, 30+ days  | 5x         | 5,000        | 280,000      |
| $10K in Curve LP     | 3x         | 3,000        | 168,000      |
| $10K in Morpho       | 3x         | 3,000        | 168,000      |

## Referral Program

Earn **10% of your referees' Points** on an ongoing basis.

| Component             | Details                              |
| --------------------- | ------------------------------------ |
| **Platform**          | Merkl                                |
| **Bonus**             | 10% of referee's Points              |
| **Qualifying Action** | Referee mints $100+ BUCK via buck.io |
| **Duration**          | Ongoing (as long as referee earns)   |

Referrals only count for direct mints through buck.io—DEX purchases don't qualify.

## Merkl BUCK Rewards (Running Concurrently)

Alongside Points, Season 1 includes direct BUCK distributions via Merkl:

| Pool             | Weekly BUCK | 8-Week Total | Est. APY\* |
| ---------------- | ----------- | ------------ | ---------- |
| **BUCK Holders** | $6,250      | $50,000      | \~75%      |
| **Curve LP**     | $4,167      | $33,333      | \~50%      |
| **Total**        | $10,417     | $83,333      | —          |

\*APY estimates at $500K TVL. Actual rates depend on total participation.

{% hint style="info" %}
**Two Reward Streams**

During Season 1, you earn BOTH:

1. **Points** → Convert to protocol allocation at TGE
2. **BUCK** → Immediate value via Merkl, claimable weekly
{% endhint %}

## Season 1 Parameters

| Parameter                 | Value                     |
| ------------------------- | ------------------------- |
| **Duration**              | 8 weeks                   |
| **Minimum Participation** | $100 BUCK                 |
| **Base Rate**             | 1 Point per $10/day       |
| **Referral Bonus**        | 10% of referee's Points   |
| **Tracking**              | Daily snapshots via Merkl |

## Converting Points to Protocol Allocation

### Pro-Rata Distribution

Your protocol allocation is calculated as:

```
Your Allocation = (Your Points ÷ Total Points Earned) × Season 1 Pool
```

### Why Pro-Rata?

Pro-rata distribution ensures:

* Predictable total dilution
* Rewards relative contribution fairly
* No gaming through last-minute deposits

## Anti-Gaming Measures

### Daily Snapshots

Points are calculated using daily balance snapshots. This prevents:

* Last-minute deposits before snapshots
* Flash loan manipulation
* Cross-protocol arbitrage

### Minimum Balance

$100 minimum BUCK balance required to earn Points. Filters dust wallets and reduces sybil attacks.

### Continuous Holding

Hold duration multipliers require **continuous** holding. Any break (selling, transferring out) resets your timer to zero.

## How to Participate

### Step 1: Get BUCK

```
1. Go to buck.io
2. Connect wallet
3. Mint BUCK with USDC
   —or—
   Buy on Curve
```

### Step 2: Choose Your Strategy

| Strategy           | Risk   | Reward                 | Best For           |
| ------------------ | ------ | ---------------------- | ------------------ |
| **Hold BUCK**      | Low    | Up to 5x (at 30+ days)  | Patient holders    |
| **Curve LP**       | Medium | 3x + trading fees       | Active DeFi users  |
| **Morpho Lending** | Medium | 3x + lending yield      | Yield optimizers   |
| **Refer Friends**  | None   | 10% of referee's Points | Community builders |

### Step 3: Track Progress

Points dashboard at buck.io/points. Your position is tracked on-chain via daily snapshots.

## Infrastructure

| Component          | Platform                   | Purpose                                 |
| ------------------ | -------------------------- | --------------------------------------- |
| **Points Tracking** | [Merkl](https://merkl.xyz) | On-chain activity tracking, leaderboard |
| **Referrals**       | [Merkl](https://merkl.xyz) | Referral links, 10% bonus tracking      |
| **BUCK Rewards**   | [Merkl](https://merkl.xyz) | Direct BUCK distributions               |

## Season Timeline

```
SEASON 1: 8 WEEKS
├── Points: Earn based on holding, LP, Morpho, referrals
├── Merkl:  $10,417/week BUCK rewards
└── Goal:   Bootstrap TVL + liquidity for Morpho approval

TGE: Following Season 1
├── Points convert to protocol allocation
├── Conversion ratio announced pre-TGE
└── Season 2 begins
```

## Competitive Context

Buck Points draws from proven models:

| Protocol   | Program | Duration  | Model                        |
| ---------- | ------- | --------- | ---------------------------- |
| **Ethena** | Shards  | \~6 weeks | Shards → ENA                 |
| **Falcon** | Miles   | Ongoing   | Miles → FF                   |
| **Buck**   | Points  | 8 weeks   | Points → Protocol Allocation |

We designed Points with strategic ambiguity on token details (following Ethena's playbook) while providing clear earning mechanics.

## Contract Addresses

| Contract                    | Address                                      |
| --------------------------- | -------------------------------------------- |
| **BUCK Token**              | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` |
| **Liquidity Window (Mint)** | `0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E` |

***

*Next: [Yield Overview →](../yield/overview.md)*
