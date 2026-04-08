# Season 1

Season 1 of the Buck Points Program rewards early adopters across holding and liquidity provision.

## Overview

| Detail         | Value                                |
| -------------- | ------------------------------------ |
| Season Start   | February 12, 2026                    |
| Infrastructure | Merkl                                |
| Points Token   | `0x4f6834B384F58fb07867871553d1d1483212A80D` |
| Activities     | Hold BUCK, Curve BUCK/USDC LP        |
| Referrals      | 10% bonus (Hold campaigns only)      |

## Active Campaigns

Season 1 runs in batches via Merkl. Each batch includes **Buck Points** (participation tracking) and **BUCK token rewards** (direct distribution).

### Batch 1 (Ended)

| Campaign | Period | Reward | Total |
| -------- | ------ | ------ | ----- |
| Hold BUCK — BUCK Rewards | Feb 12 – Feb 27, 2026 | BUCK | 24,250 BUCK |
| Hold BUCK — Buck Points | Feb 16 – Mar 2, 2026 | Buck Points | 97,000,000 |
| Curve LP — BUCK Rewards | Feb 12 – Feb 27, 2026 | BUCK | 14,550 BUCK |
| Curve LP — Buck Points | Feb 16 – Mar 2, 2026 | Buck Points | 9,700,000 |

**Batch 1 Totals:** 38,800 BUCK + 106,700,000 Buck Points

### Batch 2 (Live)

| Campaign | Period | Reward | Total |
| -------- | ------ | ------ | ----- |
| Hold BUCK — BUCK Rewards | Mar 16 – Apr 6, 2026 | BUCK | 14,550 BUCK |
| Hold BUCK — Buck Points | Mar 16 – Apr 6, 2026 | Buck Points | 4,850,000 |
| Curve LP — BUCK Rewards | Mar 16 – Apr 6, 2026 | BUCK | 14,113.50 BUCK |
| Curve LP — Buck Points | Mar 16 – Apr 6, 2026 | Buck Points | 9,409,000 |

**Batch 2 Totals:** 28,663.50 BUCK + 14,259,000 Buck Points

### Current Rates (Batch 2)

| Opportunity | TVL | APR | Daily BUCK Rewards | Daily Buck Points |
| ----------- | --- | --- | ------------------ | ----------------- |
| Hold BUCK | $1,179,551 | 21.43% | 692.86 BUCK | 353,865 |
| Curve BUCK/USDC LP | $1,165,143 | 21.04% | 672.07 BUCK | 349,543 |

## How to Earn Buck Points

### Active Activities

| Activity     | Description                       |
| ------------ | --------------------------------- |
| Hold BUCK    | Hold BUCK in your wallet          |
| Curve LP     | Provide BUCK/USDC liquidity on Curve |

Uniswap V3 and Morpho campaigns are not yet live. Additional campaigns may be added in future batches.

### Distribution Method

Both Buck Points and BUCK rewards use **time-weighted** distribution via Merkl:

* Points: Fixed reward amount per dollar of liquidity (FIX_APR)
* BUCK: Maximum APR capped at 35%, distributed proportionally by holdings

## Referral Program

Referrals are live on **Hold BUCK campaigns only** (not Curve LP).

| Parameter | Value |
| --------- | ----- |
| ReferralRegistry | [`0x36Fed2CE0fBad6F913B90CEAa294B1a0F1534A27`](https://etherscan.io/address/0x36Fed2CE0fBad6F913B90CEAa294B1a0F1534A27) |
| Program Key | `"buck"` |
| Referrer Bonus | 10% of referee's points |
| Referee Bonus | 10% boost on points earned |
| Cumulative | Yes (bonuses stack across referrals) |
| Max Boost | No cap |

### How to Refer

1. Call `becomeReferrer("buck", "YOURCODE")` on the ReferralRegistry — or use the referral page at [buck.io](https://buck.io)
2. Share your link: `https://app.buck.io/referral?ref=YOURCODE`
3. When your referee connects and holds BUCK, the referral relationship is recorded on-chain
4. Merkl automatically applies the 10% bonuses during reward distribution

## Blacklisted Addresses

The following addresses are excluded from earning rewards:

| Address | Description |
| ------- | ----------- |
| `0x5d105791469064cA0764cfaCfc577c286351CFAD` | Treasury Wallet |
| `0x42CB0274c6492e3991BDE2Ce75aBf8cDf7F11d66` | Curve BUCK/USDC Pool (excluded from Hold campaigns) |

## Claiming Rewards

* **Buck Points** accrue automatically via Merkl — no claiming needed for points tracking
* **BUCK rewards** are claimable at [merkl.xyz](https://app.merkl.xyz) via the Merkl Distributor contract (`0x3Ef3D8bA38EBe18DB133cEc108f4D14CE00Dd9Ae`)

## Season 1 Totals To Date

| Metric | Value |
| ------ | ----- |
| Total BUCK rewards budgeted | 67,463.50 BUCK |
| Total Buck Points budgeted | 120,959,000 |
| Batches completed | 1 |
| Batches live | 1 |
| Campaign creator | `0x536a75E33592eAb87bd499CC9912C80878B2a818` |

## Disclaimer

Points are non-monetary participation indicators used within the Buck ecosystem. They are designed to recognize and reflect a user's level of activity, engagement, and contribution (for example, forum participation, holding Buck Tokens, or involvement in community initiatives). Points are non-transferable, have no monetary value, and do not confer any legal, ownership, governance, or financial rights in or over any Buck-related entity.

Any references to potential future features are illustrative only and do not constitute a roadmap, promise, or commitment. Users should not acquire Buck Tokens or seek to accumulate points in anticipation of, or reliance upon, any future distributions, upgrades, or additional rights.

## Related

* [Quickstart](../getting-started/quickstart.md)
