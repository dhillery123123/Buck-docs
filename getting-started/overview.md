---
description: Understanding Buck Protocol
---

# Overview

## What is Buck?

Buck is a **value-accruing savings coin** protocol that delivers ~10% annualized returns through external yield from STRC (Strategy's Bitcoin-collateralized preferred stock).

{% hint style="info" %}
**Not a Stablecoin**

Unlike USDC or USDT that maintain a fixed $1.00 price, BUCK's price steadily increases over time as yield accrues. Think of it as a savings account that automatically compounds.
{% endhint %}

## How BUCK Works

### The Value Accrual Model

```
┌─────────────────────────────────────────────────────────────────┐
│                    BUCK VALUE ACCRUAL                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. You deposit USDC, receive BUCK at current exchange rate    │
│                         ↓                                       │
│  2. Protocol uses USDC to acquire STRC                         │
│                         ↓                                       │
│  3. STRC pays 10% annual dividends                             │
│                         ↓                                       │
│  4. Dividends increase treasury value                          │
│                         ↓                                       │
│  5. BUCK exchange rate rises proportionally                    │
│                         ↓                                       │
│  6. Your BUCK is worth more (no action required)               │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Price Growth Example

| Day | BUCK Price | 1,000 BUCK Value | Cumulative Growth |
|-----|------------|------------------|-------------------|
| 0 | $1.0000 | $1,000.00 | — |
| 30 | $1.0082 | $1,008.20 | +0.82% |
| 90 | $1.0247 | $1,024.70 | +2.47% |
| 180 | $1.0500 | $1,050.00 | +5.00% |
| 365 | $1.1000 | $1,100.00 | +10.00% |

## Why External Yield Matters

Buck's yield comes from a fundamentally different source than other yield-bearing tokens:

| Protocol | Yield Source | Can Go Negative? | Sustainability |
|----------|--------------|------------------|----------------|
| **Buck** | STRC dividends | ❌ No | 77.4 years coverage |
| Ethena (sUSDe) | Funding rates | ✅ Yes | Market dependent |
| Ondo (USDY) | T-Bills | ❌ No | ~4.65% (lower) |
| Traditional stables | None | N/A | 0% |

### What is STRC?

STRC is Strategy's (formerly MicroStrategy) preferred stock:

* **10% annual dividend** — Contractually obligated
* **BTC-backed** — Strategy holds $60B+ in Bitcoin
* **77.4 years coverage** — $2.25B in cash reserves
* **US-regulated** — Traded on NASDAQ

## Protocol Architecture

### Two Asset Pools

| Pool | Purpose | Composition |
|------|---------|-------------|
| **STRC Holdings** | Yield generation | Strategy preferred equity |
| **Liquidity Reserve** | Instant redemptions | USDC |

### Key Guarantees

* **100%+ Collateralized** — Always overcollateralized
* **Instant Redemption** — No waiting periods
* **On-chain Verification** — Real-time reserve transparency

## BUCK Token

| Property | Value |
|----------|-------|
| **Type** | Value-accruing savings coin |
| **Starting Price** | $1.00 |
| **Current Price** | Increases daily (~10% APY) |
| **Chain** | Ethereum (Solana planned) |
| **Contract** | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` |

## Governance Token (Coming Soon)

Buck Protocol will launch a governance token with:

* **Revenue share** — Protocol fees fund buybacks distributed to all holders
* **Governance rights** — Vote on protocol parameters

{% hint style="success" %}
**Season 1 Racks Program — 8 Weeks**

Earn Racks now through our [Racks Program](../rewards/points-program.md) to maximize your governance token allocation at TGE.

**Dual Rewards:** Earn both Racks (future governance tokens) AND $100K BUCK via Merkl
**Hold Multipliers:** 1x → 5x → 10x → 20x based on continuous hold duration
**LP/Morpho:** 3x multiplier for liquidity providers and lenders
{% endhint %}

## DeFi Composability

BUCK is fully composable with DeFi:

### Current Integrations

| Protocol | Type | Status |
|----------|------|--------|
| Curve | DEX | ✅ Live |
| Uniswap V3 | DEX | ✅ Live |

### Planned Integrations

| Protocol | Type | Status |
|----------|------|--------|
| Morpho | Lending | 🔄 In Progress |
| Pendle | Yield | 🎯 Target |
| GMX V2 | Perps | 📋 Research |

## Use Cases

### 1. Savings

Hold BUCK and earn ~10% annually with zero complexity:
* No staking required
* No rewards to claim
* No gas costs for yield

### 2. Collateral

BUCK's appreciating price makes it ideal collateral:
* Effective LTV improves over time
* Earn yield while borrowing
* Reduced liquidation risk

### 3. Treasury Management

For DAOs and protocols:
* Productive treasury asset
* On-chain verifiable backing
* DeFi-native composability

## Getting Started

### To Hold BUCK

1. Visit [buck.io](https://buck.io)
2. Connect your wallet
3. Mint BUCK with USDC
4. Watch your value grow

### To Earn Racks

1. Mint or hold BUCK
2. Optionally provide LP on Curve/Uniswap or lend on Morpho
3. Racks accrue automatically based on daily snapshots
4. Convert to governance tokens at TGE

[Learn more about the Racks Program →](../rewards/points-program.md)

## Quick Links

| Resource | Link |
|----------|------|
| Website | [buck.io](https://buck.io) |
| Whitepaper | [MiCA Whitepaper](https://buck.io/documents/Buck_Token_MiCA_Whitepaper_-_Publication_date_12.16.25_Update_date_1.4.26.pdf) |
| GitHub | [github.com/buck-labs](https://github.com/buck-labs/buck-v1) |
| Twitter | [@BuckToken](https://x.com/BuckToken) |
| Telegram | [buck_discussions](https://t.me/buck_discussions) |

---

*Next: [About Buck →](about.md)*
