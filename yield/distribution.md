---
description: Monthly yield distribution and the eligibility window
---

# Monthly Distribution

## How It Works

BUCK yield follows a two-step process each month: a **snapshot** to measure who is eligible, and a **payout** when new BUCK tokens are distributed.

{% hint style="success" %}
**Eligibility Snapshot**

**When:** 15th of each month, 9:00 AM – 4:00 PM Eastern Time

**What happens:** The protocol snapshots holder balances to determine who is eligible for that month's distribution. This is when your balance is measured — not when you get paid.

**Payout:** New BUCK tokens are distributed on the **4th business day of the following month**.
{% endhint %}

## Snapshot vs. Payout

| Step | When | What Happens |
| ---- | ---- | ------------ |
| **Eligibility snapshot** | 15th of each month, 9:00 AM – 4:00 PM ET | Protocol measures your BUCK balance |
| **Payout** | 4th business day of the following month | New BUCK minted and sent to eligible holders |

### Why 9 AM – 4 PM ET?

STRC trades on NASDAQ during U.S. market hours. The snapshot window aligns with these hours so that STRC pricing is live and accurate. This ensures fair, real-time valuation of the protocol's collateral.

## Eligibility Requirements

To receive your monthly yield distribution:

1. **Hold BUCK** — You must hold BUCK in your wallet during the eligibility window

Just hold BUCK during the window. Yield is distributed automatically — no transaction needed on your end.

## Distribution Schedule

The snapshot is taken on the 15th. Yield is distributed on the **4th business day of the following month**.

| Month         | Snapshot Date    | Payout Date          |
| ------------- | ---------------- | -------------------- |
| February 2026 | Feb 15 (Sun)\*   | Mar 5 (Thu)          |
| March 2026    | Mar 15 (Sun)\*   | Apr 6 (Mon)          |
| April 2026    | Apr 15 (Wed)     | May 6 (Wed)          |
| May 2026      | May 15 (Fri)     | Jun 4 (Thu)          |

\*When the 15th falls on a weekend, the snapshot is taken on the last trading day before the 15th.

## What If I Don't Hold During the Window?

{% hint style="warning" %}
**Hold During the Snapshot Window**

If you don't hold BUCK during the snapshot window on the 15th, you won't be included in that month's distribution. The payout happens later (4th business day of the following month), but eligibility is locked in during the snapshot. Set a reminder for the 15th of each month.
{% endhint %}

## How It Works On-Chain

Yield distribution runs in monthly epochs managed by the RewardsEngine contract ([`0x159c1C0F796a02111334cC280eE001b091a9580C`](https://etherscan.io/address/0x159c1C0F796a02111334cC280eE001b091a9580C)).

Each epoch has a start date, end date, and a checkpoint window. During the checkpoint window (the 15th), the protocol snapshots all holder balances to calculate eligible **balance-time** units — how much BUCK you held and for how long during the epoch.

After the checkpoint closes, the admin triggers distribution, which mints new BUCK tokens proportional to each holder's share of total eligible balance-time. Holders don't need to claim — the new BUCK appears in their wallet automatically.

The following are excluded from eligibility:
- DEX LP positions (yield is for holders, not AMM pools)
- Excluded addresses (treasury, reserve, protocol contracts)
- Wallets that held below minimum thresholds

For contract details, see [Smart Contracts](../technical/contracts.md).

## FAQ

### What currency is yield paid in?

Yield is distributed in additional Buck tokens.

### Do I need to do anything on the 15th?

No. Just make sure you're holding BUCK in your wallet during the snapshot window (9 AM – 4 PM ET). Your balance is measured then, and yield is paid out automatically on the 4th business day of the following month.

### Does yield go to any wallet holding BUCK?

Yes, as long as your wallet holds BUCK during the snapshot window on the 15th.

### Is there a gas fee?

No. Yield is distributed automatically — no transaction required on your end.

***

_Next:_ [_BUCK Token →_](../tokens/buck-token.md)
