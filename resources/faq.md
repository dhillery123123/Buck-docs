---
description: Frequently asked questions
---

# FAQ

## General

### What is BUCK?

BUCK is a **yield-bearing savings coin** backed by STRC (Strategy's Bitcoin-collateralized preferred stock). BUCK holders earn \~10% APY from STRC's contractual quarterly dividends, distributed monthly.

### How does BUCK generate yield?

Buck Protocol holds STRC — Strategy's 10% perpetual preferred stock on NASDAQ. STRC pays contractual quarterly dividends. Buck passes this yield to holders via monthly distributions on the 15th of each month.

### Do I need to claim my yield?

**No.** Yield is distributed automatically. On the 15th of each month, eligible holders receive their USDC yield during the eligibility window (9:00 AM - 4:00 PM ET). Just hold BUCK — no action needed. Your BUCK balance stays the same; yield is paid as a separate USDC payment.

### What tokens does Buck Protocol have?

| Token | Type | Purpose |
|-------|------|---------|
| **BUCK** | Savings coin | Hold to earn \~10% APY from STRC dividends |

A governance token is launching after Season 1. Earn Points through the [Points Program](../rewards/points-program.md) to maximize your allocation.

## Yield & Distribution

### When do I receive yield?

On the **15th of each month** during the eligibility window: **9:00 AM - 4:00 PM ET**. If the 15th falls on a weekend or market holiday, distribution moves to the next trading day.

### Why is the eligibility window 9 AM - 4 PM ET?

STRC trades on NASDAQ during U.S. market hours. The eligibility window aligns with these hours so that STRC pricing is live and accurate during distribution.

### What if I don't hold during the eligibility window?

Your portion rolls into the next month's distribution pool.

### Is the 10% yield guaranteed?

The yield comes from STRC's contractual preferred equity dividends. While these are contractually obligated (not discretionary), they are not guaranteed in the strictest sense. Strategy has $2.25B in cash reserves covering 77.4 years of dividend payments, making them highly reliable.

### Can BUCK's yield go negative?

**No.** STRC dividends are contractual preferred equity payments — they are always positive or zero, never negative. Unlike funding-rate-based yields (Ethena), you will never owe yield back.

### What currency is yield paid in?

USDC. Your BUCK balance stays the same; yield is a separate USDC payment.

### How is my share calculated?

```
Your Monthly Yield = (Your BUCK Balance / Total BUCK Supply) x Monthly Distribution Pool
```

## Minting & Redemption

### How do I get BUCK?

1. Go to [buck.io](https://buck.io)
2. Connect your wallet
3. Deposit USDC
4. Receive BUCK at current exchange rate

### Can I always redeem BUCK?

Yes. BUCK is redeemable for USDC at the current exchange rate through the Liquidity Window. No waiting period.

### Are there fees?

| Action | Fee |
|--------|-----|
| Mint | 10 bps (0.1%) |
| Redeem | 30 bps (0.3%) |

## Safety & Risk

### Is BUCK audited?

Yes. Multiple audits completed by Cyfrin, Halborn, and Spearbit.

### What backs BUCK?

* **STRC** — Strategy's 10% preferred stock ($60B+ BTC backing, $2.25B cash reserves)
* **USDC Liquidity Reserve** — For instant redemptions
* **180%+ Overcollateralization** — $1.80+ of backing per $1 of BUCK

### What if STRC dividends stop?

STRC dividends are contractually obligated preferred equity payments. If they were reduced or suspended:
- Your BUCK remains backed by the STRC treasury value and USDC reserves
- Yield rate would decrease proportionally
- You can still redeem at the current exchange rate
- Strategy's $2.25B cash reserves cover 77.4 years of dividends

### What happens if STRC price declines?

Buck maintains 180%+ overcollateralization. STRC would need to decline by more than 44% before the protocol approaches 100% collateralization. Circuit breakers and mint pauses activate at defined thresholds.

## Points Program & Governance Token

### How does the Points Program work?

Season 1 runs for **8 weeks**. Earn Points based on your activity:

| Activity | Weight | Multiplier |
|----------|--------|------------|
| Hold BUCK | 50% | 1x (5x at 30+ days) |
| Curve LP | 30% | 3x |
| Morpho Lending | 10% | 3x |
| Referrals | 10% | 10% of referee's Points |

Base rate: 1 Point per $10 BUCK per day. Minimum $100 to participate.

### What percentage of tokens go to Season 1?

The exact allocation will be announced closer to TGE. We're following Ethena's playbook of strategic ambiguity on token details while providing clear earning mechanics.

### How do Points convert to tokens?

Pro-rata distribution:

```
Your Tokens = (Your Points / Total Points) x Season 1 Pool
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

Yes. Top 2,000 wallets by Points receive:
- 50% at TGE
- 50% vested over 6 months (requires continued participation)

Wallets outside top 2,000 receive full allocation at TGE.

### Do early participants get benefits in future seasons?

Yes. Season 1 participants receive a **10% Points boost** in Season 2.

## Technical

### What chain is BUCK on?

Ethereum mainnet.

### What's the contract address?

| Contract | Address |
|----------|---------|
| BUCK Token | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` |
| Liquidity Window | `0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E` |

### Is BUCK composable with DeFi?

Yes. BUCK works with:

* **DEXs** — Curve, Uniswap
* **Lending** — Morpho (coming soon)
* **Yield** — Pendle (planned)

### How does the oracle work?

The Oracle Adapter uses RedStone for STRC price feeds with:

* 30-minute TWAP smoothing
* Market hours detection (STRC trades Mon-Fri 9:30 AM - 4 PM ET)
* Circuit breakers for >15% moves

## Comparisons

### How is BUCK different from USDC?

| Feature | USDC | BUCK |
|---------|------|------|
| Yield | 0% | \~10% APY |
| Price | Fixed $1.00 | Exchange rate + monthly yield |
| Backing | Cash/treasuries | STRC (Strategy preferred stock) |

### How is BUCK different from sUSDe (Ethena)?

| Feature | sUSDe | BUCK |
|---------|-------|------|
| Yield | \~5% (variable) | \~10% |
| Can go negative | Yes | No |
| Yield source | Funding rates | STRC dividends |

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

---

*Have more questions? Join our [Telegram](https://t.me/buck_discussions)*
