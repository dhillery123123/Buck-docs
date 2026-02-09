---
description: Understanding and managing protocol risks
---

# Risk Framework

{% hint style="warning" %}
**Important**

All DeFi protocols carry inherent risks. You could lose some or all of your funds. Only deposit what you can afford to lose. This section helps you understand the specific risks of holding BUCK.
{% endhint %}

## Risk Overview

Buck's risk profile differs from traditional stablecoins and other yield-bearing tokens. Understanding these differences helps you make informed decisions.

### Risk Categories

| Category | Page | Key Concerns |
|----------|------|--------------|
| **Treasury & Collateral** | [Read →](risks-collateral.md) | Dividend risk, asset price volatility, collateralization |
| **Oracle & Market Hours** | [Read →](risks-oracle.md) | Price gaps, oracle manipulation, liquidation protection |
| **Smart Contract & Operational** | [Read →](risks-smart-contract.md) | Code security, upgradeability, custody, access control |

## Quick Risk Summary

### What Could Cause Losses?

| Risk | Likelihood | Potential Impact | Primary Mitigation |
|------|------------|------------------|-------------------|
| STRC price decline | Low-Medium | Medium | 180%+ overcollateralization |
| Dividend suspension | Very Low | Medium | $2.25B cash reserves, 77+ years coverage |
| Smart contract exploit | Low | Critical | 3 independent audits |
| Oracle manipulation | Low | Medium | NASDAQ-based pricing + TWAP |
| Strategy insolvency | Extremely Low | High | $60B+ BTC treasury, preferred creditor status |

### What BUCK Is Not

- **Not a stablecoin:** BUCK price changes (upward) as yield accrues
- **Not risk-free:** Smart contract, counterparty, and market risks exist
- **Not guaranteed:** Yield depends on STRC dividends continuing
- **Not insured by FDIC:** This is DeFi, not a bank account

## Audits

Three independent security firms have audited Buck's smart contracts:

| Auditor | Scope | Status | Report |
|---------|-------|--------|--------|
| **Cyfrin** | Full protocol | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/2025-12-19-cyfrin-strong-v2.0.pdf) |
| **Spearbit** | Full protocol | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/spearbit-buck-1219.pdf) |
| **SSC** | Full protocol | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/Strong%20DAO%20Smart%20Contracts%20_%20SSC.pdf) |

All critical and high-severity findings have been resolved.

## Bug Bounty

We maintain an active bug bounty program:

| Severity | Reward |
|----------|--------|
| Critical | Up to $500,000 |
| High | Up to $50,000 |
| Medium | Up to $10,000 |
| Low | Up to $1,000 |

**Report to:** security@buck.io

## Detailed Risk Documentation

For comprehensive risk analysis, see:

- [Treasury & Collateral Risk →](risks-collateral.md)
- [Oracle & Market Hours Risk →](risks-oracle.md)
- [Smart Contract & Operational Risk →](risks-smart-contract.md)

---

*Next: [Treasury & Collateral Risk →](risks-collateral.md)*
