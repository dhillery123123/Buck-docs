---
description: Understanding Buck's value-accrual savings coin model
---

# Overview

## The Bitcoin Dollar

Buck is a **value-accruing savings coin** that delivers 10% annualized growth through STRC dividends. Unlike traditional stablecoins that stay pegged to $1.00, BUCK's price steadily increases as yield accrues directly to the token.

## Value Accrual Model

### How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                    VALUE ACCRUAL FLOW                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  STRC Dividends    →    Buck Treasury    →    BUCK Price       │
│  (10% Annual)           Receives Cash         Increases        │
│                                                                 │
│  ┌─────────────┐        ┌─────────────┐      ┌─────────────┐   │
│  │  Strategy   │   $    │    Buck     │  ↑   │    BUCK     │   │
│  │  Pays Out   │ ────▶  │  Protocol   │ ───▶ │   Token     │   │
│  │  Quarterly  │        │  Treasury   │      │   Price     │   │
│  └─────────────┘        └─────────────┘      └─────────────┘   │
│                                                                 │
│  Result: BUCK price grows ~0.026% daily (~10% annually)        │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Why Value Accrual?

| Model | How Yield Works | User Experience |
|-------|-----------------|-----------------|
| **Rebasing** (like stETH) | Token quantity increases | Confusing, tax events |
| **Reward Claiming** (like farms) | Manual claim required | Gas costs, complexity |
| **Value Accrual** (like wstETH, **BUCK**) | Token price increases | Simple, automatic |

BUCK uses the **value accrual model** because:

1. **Simplicity** — Just hold BUCK, value grows automatically
2. **Tax Efficiency** — No taxable events until you sell
3. **DeFi Compatibility** — Works seamlessly as collateral
4. **No Gas Costs** — No transactions needed to receive yield

## Token System

Buck Protocol currently operates with one token, with a governance token coming soon:

### BUCK — The Savings Coin

| Property | Value |
|----------|-------|
| **Type** | Value-accruing savings coin |
| **Yield** | ~10% annualized price appreciation |
| **Mechanism** | Price increases as STRC dividends accrue |

### Governance Token — Coming Soon

| Property | Value |
|----------|-------|
| **Type** | Governance & value capture |
| **Revenue Share** | 25% of protocol fees will fund buybacks & burns |
| **Use Cases** | Voting, staking for boosted rewards |

{% hint style="info" %}
Earn points now through our [Points Program](../rewards/points-program.md) to maximize your governance token allocation at TGE.
{% endhint %}

## Core Value Proposition

### vs. Traditional Stablecoins (USDC, USDT)

| Feature | USDC/USDT | BUCK |
|---------|-----------|------|
| Yield | 0% | ~10% annually |
| Price | Fixed at $1.00 | Grows over time |
| Backing | Cash/treasuries | STRC (Bitcoin-backed) |

### vs. Yield-Bearing Stablecoins (sDAI, sUSDe)

| Feature | sDAI | sUSDe | BUCK |
|---------|------|-------|------|
| Yield | ~5% | ~5% (variable) | ~10% |
| Yield Source | RWAs + lending | Funding rates | STRC dividends |
| Can Go Negative | No | Yes | No |
| Bitcoin Exposure | No | No | Yes |

## Yield Source: STRC

### What is STRC?

STRC (Strategy Preferred Stock) is a preferred equity instrument issued by Strategy (formerly MicroStrategy), the largest corporate holder of Bitcoin.

| Property | Details |
|----------|---------|
| **Issuer** | Strategy (NASDAQ: MSTR) |
| **Type** | Series A Perpetual Preferred Stock |
| **Dividend Rate** | 10% annual (paid quarterly) |
| **Backing** | Strategy's Bitcoin treasury (~$60B+) |
| **Dividend Coverage** | 77.4 years at current rates |

### Why STRC?

1. **External Yield** — Dividends paid regardless of crypto market conditions
2. **Publicly Traded** — Full transparency and regulatory oversight
3. **Long-Term Stability** — 77+ years of dividend coverage

## How to Use BUCK

### Mint BUCK

```
Deposit USDC → Receive BUCK at current exchange rate
```

### Hold BUCK

```
BUCK price increases daily (~0.026% per day)
No staking, no claiming, no action required
```

### Redeem BUCK

```
Burn BUCK → Receive USDC at current exchange rate
```

### Use as Collateral

```
Deposit BUCK in Morpho/Aave → Borrow against appreciating collateral
```

---

*Next: [About Buck →](about.md)*
