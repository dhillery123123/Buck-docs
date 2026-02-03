---
description: Frequently asked questions
---

# FAQ

## General

### What is BUCK?

BUCK is a **value-accruing savings coin**. Unlike stablecoins that stay at $1.00, BUCK's price steadily increases (\~10% annually) as yield from STRC dividends accrues to the token.

### How does BUCK increase in value?

Buck Protocol holds STRC (Strategy's preferred stock), which pays 10% annual dividends. These dividends flow into the treasury, increasing BUCK's exchange rate automatically.

### Do I need to stake or claim rewards?

**No.** Just hold BUCK in your wallet. The value accrues automatically—no staking, no claiming, no gas costs.

### What tokens does Buck Protocol have?

Currently Buck Protocol has one token:

| Token | Type | Purpose |
|-------|------|---------|
| **BUCK** | Savings coin | Hold to earn ~10% annually |

A governance token is launching after Season 1. Earn Racks through the [Racks Program](../rewards/points-program.md) to maximize your allocation.

## Value & Yield

### What's the current BUCK price?

BUCK started at $1.00 and increases daily. Check [buck.io](https://buck.io) for the current exchange rate.

### Is the 10% yield guaranteed?

The yield comes from STRC dividends, which are contractually obligated but not guaranteed. Strategy has 77.4 years of dividend coverage ($2.25B reserves), making it highly reliable.

### Can BUCK's yield go negative?

**No.** Unlike funding-rate-based yields (Ethena), STRC dividends are always positive. The yield rate may vary slightly based on STRC prices, but value always accrues.

### How is this different from rebasing tokens?

| Rebasing | Value Accrual (BUCK) |
|----------|----------------------|
| Token quantity changes | Token quantity stays same |
| Creates tax events | Tax only when you sell |
| Can be confusing | Simple to understand |

## Minting & Redemption

### How do I get BUCK?

1. Go to [buck.io](https://buck.io)
2. Connect your wallet
3. Deposit USDC
4. Receive BUCK at current exchange rate

### Can I always redeem BUCK?

Yes. BUCK is redeemable for USDC at the current exchange rate through the Liquidity Window. No waiting period.

### Are there fees?

* **Normal times:** 10% mint / 30% redeem fees

## Safety & Risk

### Is BUCK audited?

Yes. Multiple audits completed by Cyfrin, Spearbit, and SSC. [View audits →](../security/audits.md)

### What backs BUCK?

* **STRC Holdings** — Strategy preferred equity
* **Liquidity Reserve** — USDC for redemptions
* **100%+ Collateralization** — Always overcollateralized

### What if Strategy stops paying dividends?

Strategy has $2.25B in cash reserves covering 77.4 years of dividends. If dividends were reduced, BUCK's growth rate would decrease proportionally, but your BUCK would still be backed by STRC and reserve assets.

### What happens if STRC price crashes?

The protocol maintains 100%+ overcollateralization. A significant STRC decline would reduce the collateralization ratio, but BUCK would remain fully redeemable. Circuit breakers pause operations during extreme volatility.

## Racks Program & Governance Token

### How does the Racks Program work?

Season 1 runs for **8 weeks**. Earn Racks based on your activity:

| Activity | Weight | Multiplier |
|----------|--------|------------|
| Hold BUCK | 50% | 1x-20x (based on hold duration) |
| Curve/Uniswap LP | 30% | 3x |
| Morpho Lending | 10% | 3x |
| Referrals | 10% | 10% of referee's Racks |

**Hold Duration Multipliers:**
- 0-29 days: 1x
- 30-89 days: 5x
- 90-179 days: 10x
- 180+ days: 20x

Base rate: 1 Rack per $10 BUCK per day. Minimum $100 to participate.

### What percentage of tokens go to Season 1?

The exact allocation will be announced closer to TGE. We're following Ethena's playbook of strategic ambiguity on token details while providing clear earning mechanics.

### How do Racks convert to tokens?

Pro-rata distribution:

```
Your Tokens = (Your Racks ÷ Total Racks) × Season 1 Pool
```

### When does the governance token launch?

TGE (Token Generation Event) follows Season 1 completion. Token name, supply, and conversion ratio will be announced 2-4 weeks before TGE. Follow [@BuckToken](https://x.com/BuckToken) for announcements.

### What will the governance token do?

| Benefit | Details |
|---------|---------|
| **Revenue share** | Protocol fees fund buybacks distributed to holders |
| **Governance rights** | Vote on protocol parameters |

### Do I need to stake the governance token?

**No.** Unlike other protocols, Buck does not require staking. Just hold the governance token in your wallet to:
- Receive your share of buyback distributions
- Vote on proposals

### Do large wallets have vesting?

Yes. Top 2,000 wallets by Racks receive:
- 50% at TGE
- 50% vested over 6 months (requires continued participation)

Wallets outside top 2,000 receive full allocation at TGE.

### Do early participants get benefits in future seasons?

Yes. Season 1 participants receive a **10% Racks boost** in Season 2.

## Technical

### What chain is BUCK on?

Currently Ethereum. Solana expansion planned.

### What's the contract address?

| Contract | Address |
|----------|---------|
| BUCK Token | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` |
| Liquidity Window | `0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E` |

[Full contract list →](../security/addresses.md)

### Is BUCK composable with DeFi?

Yes. BUCK works with:

* **DEXs** — Curve, Uniswap
* **Lending** — Morpho (coming soon)
* **Yield** — Pendle (planned)

### How does the oracle work?

The Oracle Adapter uses RedStone for STRC price feeds with:

* 30-minute TWAP smoothing
* Market hours detection
* Circuit breakers for extreme moves

## Comparisons

### How is BUCK different from USDC?

| Feature | USDC | BUCK |
|---------|------|------|
| Yield | 0% | \~10% annually |
| Price | Fixed $1.00 | Grows over time |
| Backing | Cash/treasuries | STRC (BTC-backed) |

### How is BUCK different from sUSDe (Ethena)?

| Feature | sUSDe | BUCK |
|---------|-------|------|
| Yield | \~5% (variable) | \~10% |
| Can go negative | Yes | No |
| Yield source | Funding rates | Dividends |

### How is BUCK different from USDY (Ondo)?

| Feature | USDY | BUCK |
|---------|------|------|
| Yield | \~4.65% | \~10% |
| KYC | Required | Not required |
| DeFi | Limited | Full composability |

## Support

### Where can I get help?

* **Telegram:** [t.me/buck\_discussions](https://t.me/buck_discussions)
* **Twitter:** [@BuckToken](https://x.com/BuckToken)
* **Email:** admin@buck.io

### How do I report a bug or security issue?

* **General bugs:** [GitHub Issues](https://github.com/buck-labs/buck-v1/issues)
* **Security issues:** security@buck.io (up to $500K bounty)

### Where can I learn more?

* [Whitepaper (PDF)](https://buck.io/documents/Buck_Token_MiCA_Whitepaper_-_Publication_date_12.16.25_Update_date_1.4.26.pdf)
* [GitHub](https://github.com/buck-labs/buck-v1)
* [Blog](https://buck.io/blog)

---

*Have more questions? Join our [Telegram](https://t.me/buck_discussions)*
