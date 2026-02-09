---
description: Understanding smart contract security and operational controls
---

# Smart Contract & Operational Risk

## Audits

Three independent security firms have audited Buck's smart contracts:

| Auditor | Status | Report |
|---------|--------|--------|
| **Cyfrin** | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/2025-12-19-cyfrin-strong-v2.0.pdf) |
| **Spearbit** | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/spearbit-buck-1219.pdf) |
| **SSC** | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/Strong%20DAO%20Smart%20Contracts%20_%20SSC.pdf) |

All critical and high-severity findings have been resolved. Audits reduce but don't eliminate risk — unknown attack vectors may exist.

## Upgradeability

Buck uses UUPS proxy contracts. All upgrades require multi-sig approval and a 48-hour timelock. Pending upgrades are visible on-chain before execution.

Your BUCK balance, redemption ability, and core ERC-20 mechanics cannot be changed without notice.

## Access Control

| Role | Permissions | Holder |
|------|-------------|--------|
| **ADMIN_ROLE** | Upgrades, emergency pause | Multi-sig |
| **MINTER_ROLE** | Mint BUCK tokens | Liquidity Window contract only |
| **PAUSER_ROLE** | Pause operations | Multi-sig + select team |
| **ATTESTOR_ROLE** | Submit reserve attestations | The Network Firm |

Admin wallet: `0x376269214bB78b3D4f31d17600499b439c1aCB4b`

No single person can execute privileged operations.

## Emergency Pause

In case of a critical vulnerability or market emergency, minting and redemption can be paused. BUCK transfers and yield accrual continue normally during a pause. Operations resume after manual review.

## Custody

Treasury assets are held via Fireblocks (institutional MPC custody, SOC 2 Type II certified). No single key can sign transactions.

## Bug Bounty

| Severity | Reward |
|----------|--------|
| **Critical** | Up to $500,000 |
| **High** | Up to $50,000 |
| **Medium** | Up to $10,000 |
| **Low** | Up to $1,000 |

**Report to:** security@buck.io

---

*Next: [Reserve Attestations →](reserve-attestations.md)*
