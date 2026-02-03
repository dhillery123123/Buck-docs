---
description: Understanding oracle infrastructure and market hours risks
---

# Oracle & Market Hours Risk

## Overview

STRC trades on NASDAQ during US market hours only. This creates unique challenges for 24/7 DeFi protocols that Buck's oracle infrastructure addresses.

## Market Hours Gap

### The Challenge

| Period | STRC Trading | Hours/Week |
|--------|--------------|------------|
| Market hours | ✅ Active | ~32.5 hours |
| Nights & weekends | ❌ Closed | ~135.5 hours |

DeFi operates 24/7, but STRC only trades ~20% of the time.

### Why This Matters

- **Lending protocols** need accurate prices for liquidations
- **Stale prices** could trigger inappropriate liquidations
- **Price gaps** at market open create uncertainty
- **Manipulation risk** during off-hours

## Oracle Architecture

### RedStone Integration

Buck uses RedStone oracles with custom STRC handling:

| Period | Price Source | Update Frequency |
|--------|--------------|------------------|
| **Market hours** | Live NASDAQ feed | Every block |
| **Off-hours** | Last market close | Static until open |

### Price Feed Flow

```
NASDAQ STRC Price
        ↓
   RedStone Node
        ↓
   30-min TWAP Smoothing
        ↓
   Circuit Breaker Check
        ↓
   Oracle Adapter Contract
        ↓
   Buck Protocol
```

### TWAP Smoothing

Time-Weighted Average Price (TWAP) smoothing prevents manipulation:

| Window | Purpose |
|--------|---------|
| **30 minutes** | Smooths short-term volatility |
| **Prevents** | Flash crashes triggering liquidations |
| **Allows** | Gradual price discovery |

## Circuit Breakers

### Automatic Triggers

| Condition | Action |
|-----------|--------|
| STRC moves >15% in 24h | Enhanced monitoring |
| STRC moves >25% in 24h | Operations paused |
| Oracle feed stale >2h | Fallback to backup |
| Price divergence between sources | Manual review required |

### What Happens During Pause

| Function | Status |
|----------|--------|
| Minting | ⏸️ Paused |
| Redemptions | ⏸️ May be delayed |
| Existing positions | ✅ Unaffected |
| BUCK transfers | ✅ Normal |

Operations resume after manual review confirms price accuracy.

## Liquidation Protection

### The Problem

If STRC gaps down overnight (market closed), lending positions could be underwater when market opens.

### Buck's Solution for Morpho Integration

| Protection | How It Works |
|------------|--------------|
| **Conservative LTV** | Parameters set with overnight gaps in mind |
| **TWAP smoothing** | Prevents instant liquidations on gap |
| **Treasury backstop** | Protocol LP provides liquidation liquidity |
| **Graceful degradation** | 21-day cooldown on LP withdrawals |

### Gap Scenario Example

```
Friday Close:  STRC = $100
Monday Open:   STRC = $85 (15% gap down)

Without protection:
  → Instant liquidations at market open
  → Cascade selling pressure
  → Poor execution for users

With Buck's protections:
  → TWAP smooths the price over 30 min
  → Liquidations happen gradually if needed
  → Treasury LP provides liquidity
  → Users have time to add collateral
```

## Oracle Manipulation Risk

### Attack Vectors & Mitigations

| Attack Vector | Risk Level | Mitigation |
|---------------|------------|------------|
| DEX price manipulation | N/A | Oracle uses NASDAQ, not DEX |
| Flash loan attacks | Low | TWAP smoothing |
| Stale price exploitation | Low | Staleness checks |
| Single source failure | Low | Multiple data sources |

### Why NASDAQ-Based Pricing Helps

| Factor | Benefit |
|--------|---------|
| **Regulated exchange** | SEC surveillance for manipulation |
| **Deep liquidity** | Harder to move price |
| **Institutional participation** | Professional market makers |
| **Legal consequences** | Manipulation is securities fraud |

DEX oracles can be manipulated with sufficient capital. NASDAQ manipulation requires securities fraud — a much higher bar.

## Off-Hours Behavior

### During Market Close

| Component | Behavior |
|-----------|----------|
| **Oracle price** | Frozen at last close |
| **BUCK minting** | Uses last close price |
| **BUCK redemption** | Uses last close price |
| **Exchange rate** | Continues to accrue yield |

### Market Open Transition

1. Market opens at 9:30 AM ET
2. Live price feed resumes
3. TWAP begins incorporating new prices
4. Full price update within 30 minutes
5. Any queued operations process

## Extended Closure Scenarios

### Holidays & Market Closures

| Event | Duration | Protocol Action |
|-------|----------|-----------------|
| Weekend | 2.5 days | Normal (expected) |
| US holiday | 1 day | Normal (expected) |
| Extended closure | 3+ days | Enhanced monitoring |
| Market emergency | Unknown | Manual intervention |

### Emergency Procedures

If markets close unexpectedly for extended periods:

1. Protocol continues with last known price
2. Team monitors for material news
3. Manual price updates if justified
4. Communication via official channels

## Monitoring & Transparency

### Real-Time Dashboard

Monitor oracle health at [link to dashboard]:

- Current STRC price
- Last update timestamp
- TWAP vs spot deviation
- Circuit breaker status

### Oracle Contract

| Contract | Address |
|----------|---------|
| Oracle Adapter | `0xa6c5f4D041192C2019E77f679eA02e9684235Fd9` |

```solidity
// Check current price
function getPrice() external view returns (uint256);

// Check if market is open
function isMarketOpen() external view returns (bool);

// Get TWAP
function getTWAP(uint256 period) external view returns (uint256);
```

## Risk Summary

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Price gap at market open | Medium | Low-Medium | TWAP, conservative LTV |
| Oracle manipulation | Low | Medium | NASDAQ source, circuit breakers |
| Stale price exploitation | Low | Medium | Staleness checks |
| Extended market closure | Very Low | Medium | Manual intervention capability |
| Oracle failure | Very Low | High | Multiple data sources, fallback |

---

*Next: [Smart Contract & Operational Risk →](risks-smart-contract.md)*
