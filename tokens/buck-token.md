---
description: The value-accruing savings coin
---

# BUCK

## The Bitcoin Dollar

BUCK is a **value-accruing savings coin** that delivers \~10% annualized growth. Unlike stablecoins that maintain a fixed $1.00 price, BUCK's price steadily increases as STRC dividend yield accrues directly to the token.

{% hint style="success" %}
**Simple as Holding**

Just hold BUCK in your wallet. No staking, no claiming, no complexity. Your BUCK automatically appreciates in value every day.
{% endhint %}

## Token Specifications

| Property           | Value                                        |
| ------------------ | -------------------------------------------- |
| **Name**           | Buck                                         |
| **Symbol**         | BUCK                                         |
| **Type**           | Value-Accruing Savings Coin                  |
| **Decimals**       | 18                                           |
| **Standard**       | ERC-20                                       |
| **Chain**          | Ethereum (Solana planned)                    |
| **Contract**       | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` |
| **Starting Price** | $1.00 (at launch)                            |
| **Current Price**  | Increases daily (\~10% annually)             |
| **Max Supply**     | Unlimited (mint/burn model)                  |

## How Value Accrual Works

### The Mechanism

```
┌─────────────────────────────────────────────────────────────────┐
│                    BUCK VALUE ACCRUAL                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. Strategy pays STRC dividends quarterly                      │
│                         ↓                                       │
│  2. Buck Treasury receives dividend payments                    │
│                         ↓                                       │
│  3. Treasury value increases                                    │
│                         ↓                                       │
│  4. BUCK exchange rate increases proportionally                 │
│                         ↓                                       │
│  5. Your BUCK is worth more (without any action)                │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Price Growth Example

| Time    | BUCK Price | 1,000 BUCK Value | Growth  |
| ------- | ---------- | ---------------- | ------- |
| Day 0   | $1.0000    | $1,000.00        | —       |
| Day 30  | $1.0082    | $1,008.20        | +0.82%  |
| Day 90  | $1.0247    | $1,024.70        | +2.47%  |
| Day 180 | $1.0500    | $1,050.00        | +5.00%  |
| Day 270 | $1.0759    | $1,075.90        | +7.59%  |
| Day 365 | $1.1000    | $1,100.00        | +10.00% |

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

### Exchange Rate

The BUCK exchange rate is calculated as:

```
Exchange Rate = (STRC Price / 100) + Accrued Yield
```

This rate increases continuously as dividends accrue.

### Minting Fees

| Condition | Fee |
| --------- | --- |
| Standard  | 10% |

## Redeeming BUCK

### How to Redeem

1. **Connect** your wallet to buck.io
2. **Approve** BUCK spending
3. **Enter** amount to redeem
4. **Receive** USDC at current exchange rate

```
Example (assuming BUCK price is $1.10):
Burn 1,000 BUCK → Receive 1,100 USDC
```

## Collateralization

### Backing Structure

BUCK is backed by two asset pools:

| Pool                  | Purpose             | Composition               |
| --------------------- | ------------------- | ------------------------- |
| **STRC Holdings**     | Yield generation    | Strategy preferred equity |
| **Liquidity Reserve** | Instant redemptions | USDC                      |

### Collateralization: 100%

```
Collateralization Ratio = (STRC Value + Reserve Value) / (BUCK Supply × BUCK Price)
```

The protocol maintains 100% collateralization at all times.

## DeFi Use Cases

### As Collateral

BUCK's appreciating price makes it ideal collateral:

```
Day 0:   Deposit 10,000 BUCK ($10,000) as collateral
         Borrow 7,000 USDC (70% LTV)
         
Day 365: Your collateral is now worth $11,000
         Same debt, lower effective LTV
         Can borrow additional $700 or reduce liquidation risk
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
| Uniswap V2 | DEX     | ✅ Live      | Concentrated liquidity |
| Morpho     | Lending | 🔄 Pending  | Borrow against BUCK    |
| Pendle     | Yield   | 🎯 Target   | Yield tokenization     |
| GMX V2     | Perps   | 📋 Research | Margin collateral      |

## Exchange Rate Oracle

### How Price is Determined

The Oracle Adapter contract calculates the BUCK exchange rate:

```solidity
function getExchangeRate() public view returns (uint256) {
    uint256 treasuryValue = getTotalTreasuryValue();
    uint256 buckSupply = buck.totalSupply();
    return (treasuryValue * 1e18) / buckSupply;
}
```

### Price Feed Components

| Component       | Source          | Purpose                   |
| --------------- | --------------- | ------------------------- |
| STRC Price      | RedStone Oracle | Value STRC holdings       |
| Reserve Balance | On-chain        | Value stablecoin reserves |
| BUCK Supply     | On-chain        | Calculate exchange rate   |

### Market Hours Handling

STRC trades during US market hours only. The oracle:

* Uses live pricing during market hours
* Uses most recent market close price during off hours
* Applies circuit breakers for extreme moves

***

_Next:_ [_Racks Program →_](../rewards/points-program.md)
