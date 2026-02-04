---
description: Understanding treasury and collateralization risks
---

# Treasury & Collateral Risk

## Overview

Buck's yield comes from a diversified hard asset treasury. Understanding these assets and their risks is essential to understanding Buck risk.

## Dividend Risk

### What if dividend payments stop?

**Short answer:** Extremely unlikely given diversified backing, but if it happened, BUCK yield would decrease — your BUCK value would not decrease.

#### Why It's Unlikely

| Factor | Details |
|--------|---------|
| **Contractual obligation** | Dividends are preferred equity payments, not discretionary |
| **Diversification** | Multiple hard asset classes reduce single-issuer risk |
| **Payment priority** | Preferred dividends must be paid before common dividends |
| **Regulatory oversight** | Yield instruments are NASDAQ-listed, SEC-regulated |

#### If Dividends Were Reduced

| Scenario | Impact on BUCK |
|----------|----------------|
| Dividend cut 50% | BUCK yield drops to ~5% APY |
| Dividend suspended | BUCK yield drops to ~0% (no growth) |
| Full default | BUCK backed by remaining treasury assets + reserves |

**Key point:** Reduced dividends affect *future yield*, not *current BUCK value*. You can still redeem BUCK at the current exchange rate.

### What if a counterparty defaults?

Buck's diversified treasury mitigates single-issuer risk. In a default scenario for any yield instrument, the treasury's remaining assets (BTC, gold, T-bills, other holdings) continue to back BUCK.

For preferred equity instruments specifically, holders have claims before common stockholders in a liquidation:

```
1. Secured creditors
2. Unsecured creditors
3. Preferred shareholders ← Buck's yield instruments
4. Common shareholders
```

#### Treasury Strength

| Factor | Benefit |
|--------|---------|
| **Diversification** | No single asset failure can drain the treasury |
| **Hard asset backing** | BTC, gold, and T-bills provide baseline value |
| **Contractual yield** | Preferred equity dividends are legally obligated |
| **Institutional custody** | All assets held via institutional-grade custody |

## Treasury Asset Price Risk

### What if treasury assets decline in value?

Treasury asset price movements affect Buck's collateralization ratio but not your ability to redeem. Diversification across multiple hard asset classes reduces the impact of any single asset decline.

#### Impact Scenarios

| Treasury Decline | Collat. Ratio | Protocol Action |
|------------------|---------------|-----------------|
| -10% | ~90% | Monitor closely |
| -20% | ~80% | Pause new mints |
| -30% | ~70% | Redemption queue |
| -50% | ~50% | Treasury recapitalization |

#### Mitigations

| Mitigation | How It Helps |
|------------|--------------|
| **Diversification** | BTC, gold, T-bills reduce correlation risk |
| **100%+ overcollateralization** | Buffer absorbs price declines |
| **Liquidity Reserve** | USDC reserve for redemptions |
| **Circuit breakers** | Pause operations during extreme volatility |

### Diversification Benefit

Buck's treasury holds multiple uncorrelated asset classes:

- **Bitcoin** — Digital hard money, high growth potential
- **Gold** — Traditional safe haven, low correlation to crypto
- **U.S. Treasuries** — Risk-free rate, stable value
- **Institutional yield instruments** — Contractual dividends with preferred equity protections

A decline in one asset class is partially offset by stability in others.

## Collateralization Risk

### How is BUCK backed?

| Asset | Purpose |
|-------|---------|
| **Institutional yield instruments** | Primary yield generation |
| **Bitcoin** | Hard money reserve |
| **Gold** | Safe haven diversification |
| **U.S. Treasuries** | Risk-free baseline |
| **USDC Reserve** | Instant redemptions |

### Collateralization Ratio

The ratio is calculated as:

```
Collateralization Ratio = (Treasury Value + Reserve Value) / (BUCK Supply × BUCK Price)
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
2. Treasury liquidates assets as needed
3. All requests fulfilled at current exchange rate
4. No haircut on redemption value

## Market Correlation Risk

### How Market Downturns Affect BUCK

```
Hard Asset Prices Fall
      ↓
Treasury Value Decreases
      ↓
Collateralization Ratio Decreases
      ↓
Protocol takes defensive action if needed
```

### Why Diversification Helps

| Factor | Effect |
|--------|--------|
| **Multiple asset classes** | No single point of failure |
| **Gold as hedge** | Historically uncorrelated to crypto |
| **T-bills as floor** | Risk-free value doesn't decline |
| **Contractual dividends** | Yield continues regardless of price |

### Bear Market Scenario

Even in a severe market downturn:

- Contractual dividends continue (legally obligated)
- BUCK yield continues (dividends still paid)
- Your BUCK remains redeemable
- Gold and T-bills provide downside stability
- Protocol may pause mints temporarily

## Risk Mitigation Summary

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Dividend reduction | Very Low | Medium | Contractual obligations, diversification |
| Dividend suspension | Extremely Low | High | Preferred equity priority |
| Treasury asset decline | Low-Medium | Medium | Overcollateralization, diversification |
| Undercollateralization | Low | High | Circuit breakers, mint pause |
| Counterparty default | Extremely Low | High | Multi-asset treasury, preferred creditor status |

---

*Next: [Oracle & Market Hours Risk →](risks-oracle.md)*
