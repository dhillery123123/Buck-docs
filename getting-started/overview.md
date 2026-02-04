---
description: Understanding Buck Protocol
---

# Overview

## What is Buck?

Buck is a **value-accruing savings coin** protocol that delivers \~10% annualized returns through external yield from a diversified treasury of hard assets — Bitcoin, gold, U.S. treasuries, and institutional yield instruments.

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
│  1. You deposit USDC, receive BUCK at current exchange rate     │
│                         ↓                                       │
│  2. Protocol deploys USDC into hard asset treasury              │
│     (BTC, gold, T-bills, institutional yield instruments)       │
│                         ↓                                       │
│  3. Hard assets generate ~10% annual yield via dividends        │
│                         ↓                                       │
│  4. Yield increases treasury value                              │
│                         ↓                                       │
│  5. BUCK exchange rate rises proportionally                     │
│                         ↓                                       │
│  6. Your BUCK is worth more (no action required)                │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Price Growth Example

| Day | BUCK Price | 1,000 BUCK Value | Cumulative Growth |
| --- | ---------- | ---------------- | ----------------- |
| 0   | $1.0000    | $1,000.00        | —                 |
| 30  | $1.0082    | $1,008.20        | +0.82%            |
| 90  | $1.0247    | $1,024.70        | +2.47%            |
| 180 | $1.0500    | $1,050.00        | +5.00%            |
| 365 | $1.1000    | $1,100.00        | +10.00%           |

## Why External Yield Matters

Buck's yield comes from a fundamentally different source than other yield-bearing tokens:

| Protocol            | Yield Source        | Can Go Negative? | Sustainability      |
| ------------------- | ------------------- | ---------------- | ------------------- |
| **Buck**            | Hard asset dividends | ❌ No             | Contractual backing |
| Ethena (sUSDe)      | Funding rates       | ✅ Yes            | Market dependent    |
| Ondo (USDY)         | T-Bills             | ❌ No             | \~4.65% (lower)     |
| Traditional stables | None                | N/A              | 0%                  |

### What Backs Buck?

Buck's treasury is diversified across the hardest assets in the world:

* **Institutional yield instruments** — Contractual dividends generating \~10% annually
* **Bitcoin** — The hardest digital money, held as reserve backing
* **Gold** — Traditional store of value and safe haven asset
* **U.S. Treasuries** — Risk-free government-backed securities

## Protocol Architecture

### Two Asset Pools

| Pool                    | Purpose             | Composition                                    |
| ----------------------- | ------------------- | ---------------------------------------------- |
| **Hard Asset Treasury** | Yield generation    | BTC, gold, T-bills, institutional yield instruments |
| **Liquidity Reserve**   | Instant redemptions | USDC                                           |

### Key Guarantees

* **100%+ Collateralized** — Always overcollateralized
* **Instant Redemption** — No waiting periods
* **On-chain Verification** — Real-time reserve transparency

## BUCK Token

| Property           | Value                                        |
| ------------------ | -------------------------------------------- |
| **Type**           | Value-accruing savings coin                  |
| **Starting Price** | $1.00                                        |
| **Current Price**  | Increases daily (\~10% APY)                  |
| **Chain**          | Ethereum (Solana planned)                    |
| **Contract**       | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` |

## DeFi Composability

BUCK is fully composable with DeFi:

### Current Integrations

| Protocol   | Type | Status |
| ---------- | ---- | ------ |
| Curve      | DEX  | ✅ Live |
| Uniswap V3 | DEX  | ✅ Live |

### Planned Integrations

| Protocol | Type    | Status         |
| -------- | ------- | -------------- |
| Morpho   | Lending | 🔄 In Progress |
| Pendle   | Yield   | 🎯 Target      |
| GMX V2   | Perps   | 📋 Research    |

## Use Cases

### 1. Savings

Hold BUCK and earn \~10% annually with zero complexity:

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

| Resource   | Link                                                                                                                       |
| ---------- | -------------------------------------------------------------------------------------------------------------------------- |
| Website    | [buck.io](https://buck.io)                                                                                                 |
| Whitepaper | [MiCA Whitepaper](https://buck.io/documents/Buck_Token_MiCA_Whitepaper_-_Publication_date_12.16.25_Update_date_1.4.26.pdf) |
| GitHub     | [github.com/buck-labs](https://github.com/buck-labs/buck-v1)                                                               |
| Twitter    | [@BuckToken](https://x.com/BuckToken)                                                                                      |
| Telegram   | [buck\_discussions](https://t.me/buck_discussions)                                                                         |

***

_Next:_ [_About Buck →_](about.md)
