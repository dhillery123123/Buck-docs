---
description: Understanding and managing protocol risks
---

# Risk Framework

{% hint style="warning" %}
**Important**

All DeFi protocols carry inherent risks. You could lose some or all of your funds. Only deposit what you can afford to lose.
{% endhint %}

## Risk Categories

| Category | Key Risks |
|----------|-----------|
| **Market** | STRC price volatility, BTC exposure |
| **Counterparty** | Strategy solvency, custody |
| **Liquidity** | Redemption capacity, DEX depth |
| **Regulatory** | Securities classification |

## Market Risks

### STRC Price Volatility

**Risk:** STRC price may decline, reducing treasury value and BUCK's backing.

**Mitigations:**

* 100% minimum overcollateralization
* Liquidity Reserve holds stablecoins
* Circuit breakers pause on extreme moves
* Insurance fund provides buffer

### Bitcoin Correlation

**Risk:** STRC correlates with Bitcoin. Severe BTC crash could impact STRC value.

**Mitigations:**

* STRC is preferred equity (senior to common)
* Dividends paid regardless of BTC price
* Overcollateralization absorbs declines
* Strategy's diversified BTC acquisition

## Counterparty Risks

### Strategy (STRC Issuer)

**Risk:** Strategy could reduce or suspend dividends.

**Mitigations:**

* 77.4 years dividend coverage ($2.25B reserves)
* Publicly traded with regulatory oversight
* Preferred equity has legal dividend claim
* Core business tied to Bitcoin success

### Custody

**Risk:** Custodians could be compromised or insolvent.

**Mitigations:**

* Fireblocks institutional custody
* MPC key management
* SOC 2 Type II certified
* Insurance on custodied assets

## Liquidity Risks

### Redemption Capacity

**Risk:** Large redemptions could exceed available liquidity.

**Mitigations:**

* Liquidity Reserve maintains stablecoin buffer
* STRC can be liquidated for large redemptions
* Insurance fund provides backstop
* Redemption queuing for extreme scenarios

### Market Hours Gap

**Risk:** STRC doesn't trade 24/7, creating price uncertainty.

**Mitigations:**

* Oracle uses "most recent price" during closed periods
* Conservative valuations overnight
* Fundamental pricing methodology

## Security Resources

### Audits

| Auditor | Report |
|---------|--------|
| Cyfrin | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/2025-12-19-cyfrin-strong-v2.0.pdf) |
| Spearbit | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/spearbit-buck-1219.pdf) |
| SSC | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/Strong%20DAO%20Smart%20Contracts%20_%20SSC.pdf) |

### Bug Bounty

| Severity | Reward |
|----------|--------|
| Critical | Up to $500,000 |
| High | Up to $50,000 |
| Medium | Up to $10,000 |
| Low | Up to $1,000 |

Report to: security@buck.io

---

*Next: [Smart Contracts →](../technical/contracts.md)*
