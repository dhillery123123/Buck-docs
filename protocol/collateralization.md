---
description: How BUCK is backed by STRC with 180% over-collateralization
---

# How Buck is Backed

## STRC: The Sole Collateral

BUCK is backed by **STRC** — Strategy's 10% perpetual preferred stock (NASDAQ: STRC). The protocol holds STRC in its treasury and maintains a USDC liquidity reserve for instant redemptions.

{% hint style="success" %}
**180% Over-Collateralized**

For every $1 of BUCK in circulation, the protocol holds $1.80+ in STRC and USDC reserves. This buffer protects holders even in adverse market conditions.
{% endhint %}

## Backing Structure

| Component | Purpose | Composition |
|-----------|---------|-------------|
| **STRC Treasury** | Yield generation + collateral | STRC (Strategy preferred stock) |
| **Liquidity Reserve** | Instant redemptions | USDC |

### Collateralization Ratio

```
Collateralization Ratio = (STRC Treasury Value + USDC Reserve) / (BUCK Supply x BUCK Price)

Current Target: 180%+
```

## Why STRC?

| Property | Details |
|----------|---------|
| **Issuer** | Strategy (NASDAQ: MSTR) |
| **Type** | Series A Perpetual Preferred Stock |
| **Dividend** | 10% annual, paid quarterly |
| **Cash Reserves** | $2.25B (77.4 years of dividend coverage) |
| **BTC Treasury** | $60B+ in Bitcoin holdings |
| **Overcollateralization** | STRC itself is 5x overcollateralized by Strategy's Bitcoin |
| **Regulation** | SEC-regulated, NASDAQ-listed |

### Layered Protection

```
Layer 1: STRC dividends are contractually obligated (preferred equity)
         ↓
Layer 2: Strategy has $2.25B cash to cover 77+ years of dividends
         ↓
Layer 3: Strategy holds $60B+ in Bitcoin (5x overcollateral for STRC)
         ↓
Layer 4: Buck Protocol maintains 180%+ collateral ratio on top of all this
```

## Independent Verification

### The Network Firm (Monthly Attestations)

Buck's reserves are independently verified monthly by The Network Firm:

| Verified Item | Description |
|---------------|-------------|
| **STRC Holdings** | Quantity and USD value |
| **USDC Reserve** | Liquidity reserve balance |
| **BUCK Supply** | Total outstanding tokens |
| **Collateral Ratio** | Calculated and confirmed |

### On-Chain Verification

You can verify Buck's collateral anytime via the CollateralAttestation contract:

**Contract:** `0x1aEEEf99704258947A9ea77eF021d5e0551c0428`

1. Go to [Etherscan](https://etherscan.io/address/0x1aEEEf99704258947A9ea77eF021d5e0551c0428#readContract)
2. Click "Read Contract"
3. Call `getLatestAttestation()`

### Key Addresses

| Wallet | Purpose | Address |
|--------|---------|---------|
| **Treasury** | STRC holdings | `0x5d105791469064cA0764cfaCfc577c286351CFAD` |
| **Liquidity Reserve** | USDC buffer | `0x1A426E3A87368a4851f7443Ff656A054Af872f66` |
| **BUCK Token** | Supply tracking | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` |

## Security

| Measure | Details |
|---------|---------|
| **Custody** | Fireblocks institutional custody |
| **Multi-sig** | Treasury controlled by multi-signature wallet |
| **Audits** | Cyfrin, Halborn, Spearbit |
| **Attestations** | Monthly by The Network Firm |
| **Smart contracts** | UUPS proxy with 48-hour timelock |

---

*Next: [Risk Framework →](risks.md)*
