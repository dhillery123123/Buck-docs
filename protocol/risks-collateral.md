---
description: Understanding STRC and collateralization risks
---

# Treasury & Collateral Risk

## STRC Dividend Risk

BUCK's yield depends on STRC dividends. If dividends were reduced or suspended, BUCK yield would decrease — but your BUCK value would not decrease. You can always redeem at the current exchange rate.

**Why dividend suspension is unlikely:**

- Dividends are contractual preferred equity payments, not discretionary
- $2.25B in cash reserves covers 77.4 years of dividend payments
- Preferred dividends must be paid before common dividends
- STRC is NASDAQ-listed with SEC oversight

In a Strategy solvency scenario, preferred shareholders (including Buck) have priority over common stockholders.

## STRC Price Risk

STRC price movements affect Buck's collateralization ratio. The protocol maintains 100%+ overcollateralization as a buffer.

| STRC Decline | Approx. Collat. Ratio | Protocol Action |
|--------------|----------------------|-----------------|
| -10% | ~90% | Monitor closely |
| -20% | ~80% | Increased monitoring |
| -30% | ~70% | Pause new mints |
| -50% | ~50% | Redemption queue, treasury action |

## Concentration Risk

Buck's treasury is concentrated in STRC. This means simpler verification and a single transparent yield source, but no diversification across asset classes. This trade-off is mitigated by Strategy's position as the world's largest corporate Bitcoin holder ($60B+ BTC, $2.25B cash reserves).

---

*Next: [Oracle & Market Hours Risk →](risks-oracle.md)*
