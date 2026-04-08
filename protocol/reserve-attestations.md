---
description: Independent verification of Buck's reserves
---

# Independent Reserve Attestations

## Overview

Buck's reserves are independently verified by The Network Firm through monthly attestations. This page explains what's verified and how to verify it yourself.

## What Gets Attested

### Agreed-Upon Procedures Include

| Item | Description |
|------|-------------|
| **STRC Holdings** | Quantity and fair value of STRC equity shares in brokerage account |
| **USD Cash** | Cash balance in brokerage account (dividend proceeds + uninvested funds) |
| **USDC Reserve** | Stablecoin balance in on-chain Liquidity Reserve contract |
| **Custodial Control** | Verification of entity titling and admin role on-chain |
| **Total Buck Assets** | Sum of all in-scope assets in USD |

### Attestation Process

```
1. Obtain listing of in-scope on-chain and off-chain Buck Assets from Management
         ↓
2. Observe Management access brokerage account, document STRC + cash balances
         ↓
3. Verify entity titling (Buck Assets Ltd.) via certificates of name change
         ↓
4. Demonstrate on-chain control via ADMIN_ROLE hasRole verification on Etherscan
         ↓
5. Query blockchain for USDC balance in Liquidity Reserve contract
         ↓
6. Calculate total Buck Assets value and publish signed report
```

### Custodial Arrangements

| Buck Asset | Custodian | Description |
|------------|-----------|-------------|
| **STRC (Equity Shares)** | Alpaca (Brokerage Account) | STRC equity shares held in brokerage account |
| **USD Cash** | Alpaca (Brokerage Account) | Dividend proceeds and uninvested funds |
| **USDC** | On-chain Liquidity Reserve | Smart contract `0x1A426E3A87368a4851f7443Ff656A054Af872f66`, controlled by MPC wallet |

## The Network Firm

### About

The Network Firm specializes in digital asset attestations and has experience with leading DeFi protocols and cryptocurrency projects.

### Why Third-Party Attestation Matters

| Benefit | Description |
|---------|-------------|
| **Independence** | Not controlled by Buck team |
| **Expertise** | Specialized in digital asset verification |
| **Accountability** | Professional reputation at stake |
| **Consistency** | Standardized methodology |

## Latest Attestation

### March 12, 2026 — Agreed-Upon Procedures Report

{% hint style="success" %}
**[Download Full Attestation Report (PDF) →](../attestations/2026-03-12-attestation-report.pdf)**
{% endhint %}

| Field | Details |
|-------|---------|
| **Snapshot Date and Time** | March 12, 2026, 3:00 PM ET |
| **Issued** | March 23, 2026 |
| **Performed by** | The Network Firm LLP, Miami, Florida |
| **Standard** | AICPA Attestation Standards (Agreed-Upon Procedures) |

#### Buck Assets Summary

| Buck Asset | Quantity | Price per Unit | Fair Value (USD) |
|------------|----------|---------------|-----------------|
| **STRC (Equity Shares)** | 15,285.00 | $100.01 | $1,528,652.85 |
| **USD Cash** | 117.46 | $1.00 | $117.46 |
| **USDC** | 489,446.19 | $1.00 | $489,446.19 |
| **Total Buck Assets** | | | **$2,018,216.50** |

#### Key Findings

* **STRC holdings verified** — 15,285 shares at $100.01/share observed in Alpaca brokerage account
* **Entity control confirmed** — Account titled under "Strong Stretch Ltd." with BVI Certificate of Name Change to "Buck Assets Ltd." (December 4, 2025) verified
* **On-chain control confirmed** — ADMIN_ROLE verified via `hasRole` function on Etherscan returning `True`
* **USDC reserve verified** — 489,446.19 USDC queried directly from the Liquidity Reserve contract on Ethereum

#### Important Notes

This is an agreed-upon procedures engagement, not an audit or examination. The Network Firm does not express an opinion or conclusion on the Buck Assets. Per Buck's Terms and Conditions:

* Buck Tokens are not pegged to any asset (Clause 2.7.7, 2.7.9)
* Token holders do not possess legal or economic claims on Buck Assets (Clause 2.7.8)
* Buck Tokens are not redeemable at the instruction of token holders (Clause 2.7.10)

## On-Chain Verification

### CollateralAttestation Contract

Address: `0x1aEEEf99704258947A9ea77eF021d5e0551c0428`

This contract stores attestation data on-chain:

```solidity
// View latest attestation
function getLatestAttestation() external view returns (
    uint256 timestamp,
    uint256 strcValue,
    uint256 reserveValue,
    uint256 buckSupply,
    uint256 backingRatio
);
```

### Verify Yourself

1. Go to [Etherscan](https://etherscan.io/address/0x1aEEEf99704258947A9ea77eF021d5e0551c0428#readContract)
2. Click "Read Contract"
3. Call `getLatestAttestation()`
4. Compare with published attestation report

### Attestor Wallet

| Wallet | Address |
|--------|---------|
| **CAS_ATTESTOR_WALLET** | `0x6f31810c8e6bFaf3BA486B4b7ce651b023423Fa3` |

Only this address (controlled by The Network Firm) can submit attestations.

## Real-Time Monitoring

### Key Metrics Dashboard

Monitor Buck's backing in real-time:

| Metric | How to Check |
|--------|--------------|
| **BUCK Supply** | [Etherscan Token](https://etherscan.io/token/0xdb13997f4D83EF343845d0bAEb27d1173dF8c224) |
| **Reserve Balance** | [Liquidity Reserve Contract](https://etherscan.io/address/0x1A426E3A87368a4851f7443Ff656A054Af872f66) |
| **Exchange Rate** | buck.io |

For all contract and wallet addresses, see [Smart Contracts](../technical/contracts.md).

## Attestation vs. Audit

| | Attestation | Audit |
|---|-------------|-------|
| **What** | Reserve verification | Code security |
| **Frequency** | Monthly | One-time + updates |
| **Provider** | The Network Firm | Cyfrin, Spearbit, SSC |
| **Output** | Reserve report | Security report |
| **Focus** | "Do the assets exist?" | "Is the code safe?" |

Both are important:
- **Audits** verify the code works correctly
- **Attestations** verify the reserves exist

## Historical Attestations

| Date | Total Buck Assets | STRC Holdings | USDC Reserve | Report |
|------|-------------------|---------------|-------------|--------|
| March 12, 2026 | $2,018,216.50 | 15,285 shares ($1,528,652.85) | $489,446.19 | [PDF](../attestations/2026-03-12-attestation-report.pdf) |

## FAQ

### How often are attestations published?

Monthly, typically within 10 business days of month end.

### What if backing drops significantly?

The attestation would reflect this. Protocol would:
1. Pause new mints
2. Implement redemption queue if needed
3. Treasury takes action to restore ratio

### Can I verify reserves without waiting for attestation?

Yes. Use the on-chain contract or Etherscan links above for real-time data. Attestations provide third-party verification of what you can already see on-chain.

### Why not real-time attestations?

Attestations require manual verification by The Network Firm. On-chain data is always available for real-time monitoring; attestations provide periodic third-party confirmation.

### What if The Network Firm makes an error?

Attestations are based on on-chain data that anyone can verify. Any discrepancy between the attestation and on-chain reality would be immediately visible.

---

*Next: [Smart Contracts →](../technical/contracts.md)*
