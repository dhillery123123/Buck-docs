---
description: Understanding STRC-related risks and collateralization
---

# STRC & Collateral Risk

## Overview

Buck's yield comes from STRC dividends. Understanding STRC risk is essential to understanding Buck risk.

## Dividend Risk

### What if Strategy stops paying dividends?

**Short answer:** Extremely unlikely, but if it happened, BUCK yield would decrease — your BUCK value would not decrease.

#### Why It's Unlikely

| Factor | Details |
|--------|---------|
| **Contractual obligation** | STRC dividends are preferred equity payments, not discretionary |
| **Cash reserves** | $2.25B in reserves covers 77.4 years of dividends |
| **Payment priority** | Preferred dividends must be paid before common dividends |
| **Regulatory oversight** | NASDAQ-listed, SEC-regulated public company |

#### If Dividends Were Reduced

| Scenario | Impact on BUCK |
|----------|----------------|
| Dividend cut 50% | BUCK yield drops to ~5% APY |
| Dividend suspended | BUCK yield drops to ~0% (no growth) |
| Full default | BUCK backed by remaining STRC + reserves |

**Key point:** Reduced dividends affect *future yield*, not *current BUCK value*. You can still redeem BUCK at the current exchange rate.

### What if Strategy goes bankrupt?

In a liquidation scenario, creditors are paid in order:

```
1. Secured creditors
2. Unsecured creditors
3. Preferred shareholders (STRC) ← Buck is here
4. Common shareholders
```

STRC holders have claims before common stockholders. Strategy would need to liquidate significant Bitcoin holdings before preferred equity is impaired.

#### Strategy's Financial Position

| Metric | Value |
|--------|-------|
| Bitcoin holdings | $60B+ |
| Cash reserves | $2.25B |
| STRC coverage ratio | 5x overcollateralized by BTC |
| Dividend coverage | 77.4 years |

## STRC Price Risk

### What if STRC price crashes?

STRC price movements affect Buck's collateralization ratio but not your ability to redeem.

#### Impact Scenarios

| STRC Move | Collat. Ratio | Protocol Action |
|-----------|---------------|-----------------|
| -10% | ~90% | Monitor closely |
| -20% | ~80% | Pause new mints |
| -30% | ~70% | Redemption queue |
| -50% | ~50% | Treasury recapitalization |

#### Mitigations

| Mitigation | How It Helps |
|------------|--------------|
| **100%+ overcollateralization** | Buffer absorbs price declines |
| **Liquidity Reserve** | USDC reserve for redemptions |
| **Circuit breakers** | Pause operations during extreme volatility |
| **Treasury STRC buys** | Acquire more STRC at lower prices |

### Historical STRC Volatility

STRC typically moves with Bitcoin but with lower volatility due to:

- Fixed 10% dividend provides floor value
- Institutional ownership base
- NASDAQ listing requirements
- Preferred equity structure

{% hint style="info" %}
**Note:** STRC launched in 2024, so historical data is limited. However, its structure as preferred equity with fixed dividends provides inherent stability compared to common stock or pure BTC exposure.
{% endhint %}

## Collateralization Risk

### How is BUCK backed?

| Asset | Purpose | Typical Allocation |
|-------|---------|-------------------|
| **STRC Holdings** | Yield generation | ~85% |
| **USDC Reserve** | Instant redemptions | ~15% |

### Collateralization Ratio

The ratio is calculated as:

```
Collateralization Ratio = (STRC Value + Reserve Value) / (BUCK Supply × BUCK Price)
```

**Target:** 100%+ at all times

### What Happens if Ratio Drops Below 100%?

| Stage | Trigger | Action |
|-------|---------|--------|
| **Watch** | Ratio < 110% | Increased monitoring |
| **Caution** | Ratio < 105% | Pause new mints |
| **Critical** | Ratio < 100% | Redemption queue, treasury action |
| **Recovery** | Ratio > 105% | Resume normal operations |

#### Redemption Queue

If a queue is implemented:

1. Redemption requests processed in order
2. Treasury liquidates STRC as needed
3. All requests fulfilled at current exchange rate
4. No haircut on redemption value

## Bitcoin Correlation Risk

### How BTC Affects BUCK

```
BTC Price Falls
      ↓
STRC Value Falls (correlated)
      ↓
Collateralization Ratio Decreases
      ↓
Protocol takes defensive action if needed
```

### Why STRC Is More Stable Than BTC

| Factor | Effect |
|--------|--------|
| **Fixed dividend** | 10% yield regardless of BTC price |
| **Preferred structure** | Claims before common equity |
| **Cash reserves** | $2.25B buffer independent of BTC |
| **Institutional ownership** | Less volatile trading patterns |

### Bear Market Scenario

Even in a severe BTC downturn:

- STRC dividends continue (contractual obligation)
- BUCK yield continues (dividends still paid)
- Your BUCK remains redeemable
- Protocol may pause mints temporarily

## Risk Mitigation Summary

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Dividend reduction | Very Low | Medium | 77.4 years cash coverage |
| Dividend suspension | Extremely Low | High | Preferred equity priority |
| STRC price crash | Low-Medium | Medium | Overcollateralization, reserves |
| Undercollateralization | Low | High | Circuit breakers, mint pause |
| Strategy bankruptcy | Extremely Low | High | Preferred creditor status |

---

*Next: [Oracle & Market Hours Risk →](risks-oracle.md)*
