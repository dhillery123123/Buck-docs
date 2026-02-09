---
description: Understanding Buck Protocol
---

# Overview

## What is Buck?

Buck is a **yield-bearing savings coin** that delivers \~10% APY through STRC — Strategy's Bitcoin-collateralized preferred stock. STRC pays contractual quarterly dividends, and Buck passes this yield to holders via monthly distributions.

{% hint style="info" %}
**Not a Stablecoin**

Unlike USDC or USDT that maintain a fixed $1.00 price, BUCK's value grows over time as STRC dividend yield accrues. Think of it as a savings account with monthly interest payments.
{% endhint %}

## How BUCK Works

### The Monthly Yield Model

```
┌─────────────────────────────────────────────────────────────────┐
│                    HOW BUCK YIELD WORKS                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  1. You deposit USDC, receive BUCK at the current exchange rate  │
│                         ↓                                        │
│  2. Protocol holds STRC (Strategy's 10% preferred stock)         │
│                         ↓                                        │
│  3. STRC generates ~10% annual yield via quarterly dividends     │
│                         ↓                                        │
│  4. Yield passed through to holders monthly                      │
│                         ↓                                        │
│  5. On the 15th, yield distributed automatically (9 AM - 4 PM ET)│
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Growth Example

| Day | BUCK Price | 1,000 BUCK Value | Cumulative Growth |
| --- | ---------- | ---------------- | ----------------- |
| 0   | $1.0000    | $1,000.00        | —                 |
| 30  | $1.0082    | $1,008.20        | +0.82%            |
| 90  | $1.0247    | $1,024.70        | +2.47%            |
| 180 | $1.0500    | $1,050.00        | +5.00%            |
| 365 | $1.1000    | $1,100.00        | +10.00%           |

## Why External Yield Matters

Buck's yield comes from a fundamentally different source than other yield-bearing tokens:

| Protocol            | Yield Source         | Can Go Negative? | Sustainability      |
| ------------------- | -------------------- | ---------------- | ------------------- |
| **Buck**            | STRC dividends       | ❌ No             | Contractual backing |
| Ethena (sUSDe)      | Funding rates        | ✅ Yes            | Market dependent    |
| Ondo (USDY)         | T-Bills              | ❌ No             | \~4.65% (lower)     |
| Traditional stables | None                 | N/A              | 0%                  |

### What Backs Buck?

Buck is backed by **STRC** — Strategy's 10% perpetual preferred stock:

* **$60B+ Bitcoin treasury** — Strategy holds more Bitcoin than any other public company
* **$2.25B cash reserves** — 77.4 years of dividend coverage at current rates
* **180% over-collateralized** — $1.80+ of backing per $1 of BUCK
* **SEC-regulated, NASDAQ-listed** — Institutional-grade oversight

## Protocol Architecture

### Two Components

| Component | Purpose | Composition |
| --------- | ------- | ----------- |
| **STRC Treasury** | Yield generation + collateral | STRC (Strategy preferred stock) |
| **Liquidity Reserve** | Instant redemptions | USDC |

### Key Guarantees

* **180%+ Over-Collateralized** — Significant buffer above backing requirements
* **Instant Redemption** — Redeem BUCK for USDC anytime via the Liquidity Reserve
* **On-chain Verification** — Collateral attestations verifiable on Etherscan

## BUCK Token

| Property           | Value                                        |
| ------------------ | -------------------------------------------- |
| **Type**           | Yield-bearing savings coin                   |
| **Starting Price** | $1.00                                        |
| **Yield**          | \~10% APY from STRC dividends               |
| **Chain**          | Ethereum                                     |
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

Hold BUCK and earn \~10% APY:

* Yield distributed automatically on the 15th
* No lock-ups or commitments
* Redeem for USDC anytime

### 2. Collateral

BUCK's appreciating value makes it ideal collateral:

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
4. Receive yield automatically on the 15th of each month

### To Earn Points

1. Mint or hold $100+ BUCK
2. Optionally provide LP on Curve or lend on Morpho
3. Points accrue automatically based on daily snapshots
4. Convert to protocol allocation at TGE

[Learn more about the Points Program →](../rewards/points-program.md)

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
