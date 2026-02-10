---
description: The yield-bearing savings coin backed by STRC
---

# BUCK

## Yield-Bearing Savings Coin

BUCK is a **yield-bearing savings coin** that delivers \~10% APY from STRC dividends. Unlike stablecoins that maintain a fixed $1.00 price, BUCK holders earn monthly yield distributions from Strategy's contractual preferred stock dividends.

Yield is distributed automatically in BUCK each month. See [Monthly Distribution](../yield/distribution.md) for eligibility details.

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
| **Yield**          | \~10% APY from STRC dividends                |
| **Max Supply**     | Unlimited (mint/burn model)                  |

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

| Condition | Fee           |
| --------- | ------------- |
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

| Condition | Fee           |
| --------- | ------------- |
| Standard  | 30 bps (0.3%) |

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
* Buck Points through the [Buck Points Program](../rewards/points-program.md)
* BUCK rewards via Merkl (during Season 1)

For current DeFi integrations, see [Why Buck](../getting-started/why-buck.md#works-everywhere).

## Exchange Rate Oracle

### How Price is Determined

The Oracle Adapter contract calculates the BUCK exchange rate using STRC price data from RedStone:

### Price Feed Components

| Component       | Source          | Purpose                      |
| --------------- | --------------- | ---------------------------- |
| STRC Value      | RedStone oracle | Value STRC treasury holdings |
| Reserve Balance | On-chain        | Value USDC reserves          |
| BUCK Supply     | On-chain        | Calculate exchange rate      |

### Market Hours Handling

STRC trades during U.S. market hours only (Mon-Fri, 9:30 AM - 4:00 PM ET). The oracle:

* Uses live pricing during market hours
* Uses most recent market close price during off-hours
* Circuit breakers for >15% moves

***

_Next:_ [_Points Program →_](../rewards/points-program.md)
