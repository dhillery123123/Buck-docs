---
description: Understanding STRC and collateralization risks
---

# Treasury & Collateral Risk

## Overview

Buck's yield comes from STRC — Strategy's 10% perpetual preferred stock. Understanding STRC and its risks is essential to understanding Buck.

## STRC Dividend Risk

### What if dividend payments stop?

**Short answer:** Extremely unlikely given Strategy's financial position, but if it happened, BUCK yield would decrease — your BUCK value would not decrease.

#### Why It's Unlikely

| Factor | Details |
|--------|---------|
| **Contractual obligation** | Dividends are preferred equity payments, not discretionary |
| **Cash coverage** | $2.25B in reserves = 77.4 years of dividend payments |
| **Payment priority** | Preferred dividends must be paid before common dividends |
| **Regulatory oversight** | STRC is NASDAQ-listed, SEC-regulated |
| **Bitcoin backing** | Strategy holds $60B+ in BTC (5x overcollateral) |

#### If Dividends Were Reduced

| Scenario | Impact on BUCK |
|----------|----------------|
| Dividend cut 50% | BUCK yield drops to \~5% APY |
| Dividend suspended | BUCK yield drops to \~0% (no growth) |
| Strategy default | BUCK backed by remaining treasury STRC value + USDC reserves |

**Key point:** Reduced dividends affect *future yield*, not *current BUCK value*. You can still redeem BUCK at the current exchange rate.

### Strategy Solvency Risk

STRC is issued by Strategy (NASDAQ: MSTR). In a solvency scenario:

```
1. Secured creditors
2. Unsecured creditors
3. Preferred shareholders ← STRC holders (including Buck)
4. Common shareholders
```

Preferred equity holders have priority over common stockholders in liquidation, providing additional downside protection.

#### Strategy's Financial Position

| Factor | Details |
|--------|---------|
| **Bitcoin Treasury** | $60B+ (largest corporate BTC holder) |
| **Cash Reserves** | $2.25B |
| **Dividend Coverage** | 77.4 years at current rates |
| **Public Company** | NASDAQ-listed with SEC oversight |

## STRC Price Risk

### What if STRC declines in value?

STRC price movements affect Buck's collateralization ratio. However, Buck maintains 180%+ overcollateralization as a buffer.

#### Impact Scenarios

| STRC Decline | Collat. Ratio | Protocol Action |
|--------------|---------------|-----------------|
| -10% | \~162% | Monitor closely |
| -20% | \~144% | Increased monitoring |
| -30% | \~126% | Pause new mints |
| -50% | \~90% | Redemption queue, treasury action |

#### Mitigations

| Mitigation | How It Helps |
|------------|--------------|
| **180%+ overcollateralization** | Large buffer absorbs price declines |
| **USDC Liquidity Reserve** | Separate reserve for redemptions |
| **Circuit breakers** | Pause operations during extreme volatility |
| **Daily monitoring** | Automated alerts on ratio changes |

### Why 180% Overcollateralization?

At 180%+, STRC would need to decline by more than 44% before the protocol approaches 100% collateralization. This provides substantial protection against market downturns while maintaining the \~10% yield pass-through.

## Collateralization Risk

### How is BUCK backed?

| Component | Purpose |
|-----------|---------|
| **STRC** | Yield generation + primary collateral |
| **USDC Reserve** | Instant redemptions |

### Collateralization Ratio

```
Collateralization Ratio = (STRC Value + USDC Reserve) / (BUCK Supply x BUCK Price)

Target: 180%+
```

### What Happens if Ratio Drops Below 100%?

| Stage | Trigger | Action |
|-------|---------|--------|
| **Watch** | Ratio < 150% | Increased monitoring |
| **Caution** | Ratio < 120% | Pause new mints |
| **Critical** | Ratio < 100% | Redemption queue, treasury action |
| **Recovery** | Ratio > 120% | Resume normal operations |

#### Redemption Queue

If a queue is implemented:

1. Redemption requests processed in order
2. Treasury liquidates assets as needed
3. All requests fulfilled at current exchange rate
4. No haircut on redemption value

## Concentration Risk

### Single-Asset Treasury

Unlike diversified portfolios, Buck's treasury is concentrated in STRC. This means:

**Advantages:**
* Simpler to verify and audit
* Single, transparent yield source
* No complex rebalancing or asset selection risk

**Risks:**
* No diversification across asset classes
* Dependent on Strategy's financial health
* STRC price correlated to Bitcoin market

### Why This Trade-Off Works

Strategy is the world's largest corporate Bitcoin holder with $60B+ in BTC and $2.25B in cash. STRC has the strongest preferred dividend coverage of any institutional yield instrument, with 77.4 years of reserves. The concentration risk is mitigated by the extraordinary financial strength of the underlying issuer.

## Risk Mitigation Summary

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Dividend reduction | Very Low | Medium | $2.25B cash reserves, 77+ years coverage |
| Dividend suspension | Extremely Low | High | Preferred equity priority, SEC oversight |
| STRC price decline | Low-Medium | Medium | 180%+ overcollateralization |
| Strategy insolvency | Extremely Low | High | $60B+ BTC treasury, preferred creditor status |
| Under-collateralization | Low | High | Circuit breakers, mint pause, 180% buffer |

---

*Next: [Oracle & Market Hours Risk →](risks-oracle.md)*
