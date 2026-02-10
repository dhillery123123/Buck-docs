---
description: Independent verification of Buck's reserves
---

# Independent Reserve Attestations

## Overview

Buck's reserves are independently verified by The Network Firm through monthly attestations. This page explains what's verified and how to verify it yourself.

## What Gets Attested

### Monthly Verification Includes

| Item | Description |
|------|-------------|
| **STRC Holdings** | Quantity and value of STRC treasury holdings |
| **USDC Reserve** | Stablecoin balance in Liquidity Reserve |
| **Total BUCK Supply** | Outstanding BUCK tokens |
| **Collateralization Ratio** | (Treasury + Reserve) / (BUCK Supply × Price) |
| **Exchange Rate Accuracy** | Calculated vs. reported rate |

### Attestation Process

```
1. The Network Firm receives read access to treasury wallets
         ↓
2. Independent verification of STRC holdings via custody provider
         ↓
3. On-chain verification of BUCK supply and reserve balances
         ↓
4. Calculation of collateralization ratio
         ↓
5. Signed attestation published
```

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

{% hint style="info" %}
**Coming Soon**

Monthly attestations will be published here starting with the first full month after launch. Check back for updates.
{% endhint %}

### Attestation Format

Each attestation includes:

| Field | Description |
|-------|-------------|
| **Date** | Attestation date |
| **Period** | Period covered |
| **STRC Holdings** | Quantity and USD value |
| **USDC Reserve** | Balance |
| **BUCK Supply** | Total outstanding |
| **Collateralization Ratio** | Percentage |
| **Attestor Signature** | Cryptographic signature |

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
    uint256 collateralizationRatio
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

| Date | Collat. Ratio | Treasury Holdings | BUCK Supply | Report |
|------|---------------|---------------|-------------|--------|
| *Coming Soon* | — | — | — | — |

{% hint style="info" %}
Historical attestations will be added here as they are published.
{% endhint %}

## FAQ

### How often are attestations published?

Monthly, typically within 10 business days of month end.

### What if collateralization drops below 100%?

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
