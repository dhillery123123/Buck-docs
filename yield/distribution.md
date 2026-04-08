---
description: Continuous yield streaming into BUCK price
---

# Yield Streaming

## How It Works

BUCK yield is delivered through **continuous yield streaming**. Instead of monthly snapshots and payouts, yield accrues directly into the BUCK price every second — automatically, with no action required.

{% hint style="success" %}
**Continuous Yield**

Yield streams into your BUCK price 24/7. There are no snapshots, no eligibility windows, and no claiming. Every second you hold BUCK, its price appreciates.
{% endhint %}

## How It's Different

| Feature | Traditional (Monthly) | BUCK (Continuous) |
| ------- | --------------------- | ----------------- |
| **Yield delivery** | New tokens distributed monthly | Price appreciates every second |
| **Eligibility** | Must hold during snapshot window | Hold BUCK at any time |
| **Action required** | None (auto-distribution) | None (auto-accrual) |
| **Timing risk** | Miss the snapshot, miss the yield | No timing risk |
| **Gas cost** | None | None |

## The Yield Multiplier

BUCK uses a synthetic yield multiplier that increases the token's NAV over time:

1. The protocol sets a yield rate (~10% APY) and a vesting period
2. The yield multiplier increases linearly over the vesting period
3. At the end of each period, accrued yield compounds into the base
4. A new stream begins — the process repeats continuously

### Example

```
Period 1: Base = 1.000 → streams 10% APY → ends at ~1.008 (1 month)
Period 2: Base = 1.008 → streams 10% APY → continues compounding
...
After 12 months: ~1.100 (10% growth)
```

## No Snapshots, No Windows

There is no advantage to timing your entry or exit. Unlike protocols with monthly snapshots:

* **No eligibility window** — You don't need to hold during a specific date/time
* **No missed distributions** — Every second of holding earns yield
* **No gaming** — Can't buy before snapshot and sell after
* **Fair to all holders** — Pro-rata yield based on actual hold time

## Where Does the Yield Come From?

The ~10% APY is funded entirely by **STRC dividends** — contractual preferred equity payments from Strategy. This is external, real-world yield:

* Not token emissions
* Not funding rate arbitrage
* Not inflationary rewards

See [Yield Overview](overview.md) for a deep dive on STRC as a yield source.

## Rate Updates

The protocol operator sets the yield stream rate based on realized STRC dividend income. Rate changes are:

* Applied prospectively (not retroactively)
* Bounded by on-chain safety parameters
* Visible on-chain for full transparency

The target rate is ~10% APY, matching STRC's stated coupon rate.

## FAQ

### Do I need to do anything to earn yield?

No. Just hold BUCK. Yield accrues into the price automatically.

### What if I buy BUCK mid-period?

You start earning yield immediately from the moment you hold BUCK. There is no waiting period or alignment to any schedule.

### Is there a gas fee to earn yield?

No. Yield is built into the token price — no transactions required.

***

_Next:_ [_BUCK Token →_](../tokens/buck-token.md)
