---
description: Understanding smart contract security and operational controls
---

# Smart Contract Risk

## Audits

Three independent security firms have audited Buck's smart contracts:

| Auditor      | Status     | Report                                                                                                              |
| ------------ | ---------- | ------------------------------------------------------------------------------------------------------------------- |
| **Cyfrin**   | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/2025-12-19-cyfrin-strong-v2.0.pdf)              |
| **Spearbit** | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/spearbit-buck-1219.pdf)                         |
| **SSC**      | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/Strong%20DAO%20Smart%20Contracts%20_%20SSC.pdf) |

All critical and high-severity findings have been resolved. Audits reduce but don't eliminate risk — unknown attack vectors may exist.

## Upgradeability

Buck uses UUPS proxy contracts. All upgrades require multi-sig approval and a 48-hour timelock. Pending upgrades are visible on-chain before execution.

Your BUCK balance, redemption ability, and core ERC-20 mechanics cannot be changed without notice.

## Emergency Pause

In case of a critical vulnerability or market emergency, minting and redemption can be paused. BUCK transfers and yield accrual continue normally during a pause. Operations resume after manual review.

## Custody

Treasury assets are held via Fireblocks (institutional MPC custody, SOC 2 Type II certified). No single key can sign transactions.

**Report to:** security@buck.io

***

_Next:_ [_Independent Reserve Attestations →_](reserve-attestations.md)
