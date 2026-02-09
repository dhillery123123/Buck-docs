---
description: The yield-bearing savings coin backed by STRC
---

# BUCK

## Yield-Bearing Savings Coin

BUCK is a **yield-bearing savings coin** that delivers \~10% APY from STRC dividends. Unlike stablecoins that maintain a fixed $1.00 price, BUCK holders earn monthly yield distributions from Strategy's contractual preferred stock dividends.

{% hint style="success" %}
**Hold BUCK, Claim Monthly**

Hold BUCK in your wallet. On the 15th of each month, claim your share of STRC dividend yield in USDC during the eligibility window (9:00 AM - 4:00 PM ET).
{% endhint %}

## Token Specifications

| Property           | Value                                        |
| ------------------ | -------------------------------------------- |
| **Name**           | Buck                                         |
| **Symbol**         | BUCK                                         |
| **Type**           | Yield-Bearing Savings Coin                   |
| **Decimals**       | 18                                           |
| **Standard**       | ERC-20                                       |
| **Chain**          | Ethereum                                     |
| **Contract**       | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` |
| **Starting Price** | $1.00 (at launch)                            |
| **Yield**          | \~10% APY from STRC dividends               |
| **Max Supply**     | Unlimited (mint/burn model)                  |

## How Yield Works

### The Monthly Cycle

```
┌─────────────────────────────────────────────────────────────────┐
│                    BUCK YIELD MODEL                              │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  1. Buck Protocol holds STRC (Strategy's 10% preferred stock)    │
│                         ↓                                        │
│  2. STRC pays quarterly dividends                                │
│                         ↓                                        │
│  3. Buck passes yield to holders monthly                         │
│                         ↓                                        │
│  4. On the 15th, claim your share in USDC (9 AM - 4 PM ET)      │
│                         ↓                                        │
│  5. Your BUCK balance stays the same — yield is paid separately  │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Growth Example

| Time    | BUCK Value (from $1,000) | Annual Yield Earned |
| ------- | ------------------------ | ------------------- |
| Day 0   | $1,000.00                | —                   |
| Day 90  | $1,000.00                | \~$25 claimed       |
| Day 180 | $1,000.00                | \~$50 claimed       |
| Day 365 | $1,000.00                | \~$100 claimed      |

*Your BUCK balance stays constant. Yield is received as USDC monthly.*

## Minting BUCK

### How to Mint

1. **Connect** your wallet to buck.io
2. **Approve** USDC spending
3. **Enter** amount to mint
4. **Receive** BUCK at current exchange rate

```
Example (assuming BUCK price is $1.05):
Deposit 1,050 USDC → Receive 1,000 BUCK
```

### Minting Fees

| Condition | Fee |
| --------- | --- |
| Standard  | 10 bps (0.1%) |

## Redeeming BUCK

### How to Redeem

1. **Connect** your wallet to buck.io
2. **Approve** BUCK spending
3. **Enter** amount to redeem
4. **Receive** USDC at current exchange rate

```
Example (assuming BUCK price is $1.05):
Burn 1,000 BUCK → Receive ~1,047 USDC (after 30 bps fee)
```

### Redemption Fees

| Condition | Fee |
| --------- | --- |
| Standard  | 30 bps (0.3%) |

## Collateralization

### Backing Structure

BUCK is backed by two components:

| Component | Purpose | Composition |
| --------- | ------- | ----------- |
| **STRC Treasury** | Yield generation + collateral | STRC (Strategy preferred stock) |
| **Liquidity Reserve** | Instant redemptions | USDC |

### 180% Over-Collateralized

```
Collateralization Ratio = (STRC Treasury Value + USDC Reserve) / (BUCK Supply x BUCK Price)

Current Target: 180%+
```

The protocol maintains 180%+ overcollateralization at all times, providing significant downside protection.

[Learn more about collateralization →](../protocol/collateralization.md)

## DeFi Use Cases

### As Collateral

BUCK's yield makes it ideal collateral:

```
Day 0:   Deposit 10,000 BUCK as collateral
         Borrow 7,000 USDC (70% LTV)

Day 365: You've earned ~$1,000 in yield
         Same debt, plus $1,000 in yield earned
```

### In Liquidity Pools

Provide BUCK liquidity and earn:

* Trading fees from swaps
* Racks through the [Racks Program](../rewards/points-program.md)
* BUCK rewards via Merkl (during Season 1)

### Integrations

| Protocol   | Type    | Status      | Benefit                |
| ---------- | ------- | ----------- | ---------------------- |
| Curve      | DEX     | ✅ Live      | Deep liquidity         |
| Uniswap V3 | DEX     | ✅ Live      | Concentrated liquidity |
| Morpho     | Lending | 🔄 Pending  | Borrow against BUCK    |
| Pendle     | Yield   | 🎯 Target   | Yield tokenization     |

## Exchange Rate Oracle

### How Price is Determined

The Oracle Adapter contract calculates the BUCK exchange rate using STRC price data from RedStone:

### Price Feed Components

| Component        | Source          | Purpose                    |
| ---------------- | --------------- | -------------------------- |
| STRC Value       | RedStone oracle | Value STRC treasury holdings |
| Reserve Balance  | On-chain        | Value USDC reserves        |
| BUCK Supply      | On-chain        | Calculate exchange rate    |

### Market Hours Handling

STRC trades during U.S. market hours only (Mon-Fri, 9:30 AM - 4:00 PM ET). The oracle:

* Uses live pricing during market hours
* Uses most recent market close price during off-hours
* Applies 30-minute TWAP smoothing
* Circuit breakers for >15% moves

***

_Next:_ [_Racks Program →_](../rewards/points-program.md)
