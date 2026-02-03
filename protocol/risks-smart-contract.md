---
description: Understanding smart contract security and operational controls
---

# Smart Contract & Operational Risk

## Overview

Buck's security model combines multiple audits, upgradeability safeguards, and operational controls to protect user funds.

## Audit Status

### Completed Audits

Three independent security firms have audited Buck's smart contracts:

| Auditor | Scope | Status | Report |
|---------|-------|--------|--------|
| **Cyfrin** | Full protocol | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/2025-12-19-cyfrin-strong-v2.0.pdf) |
| **Spearbit** | Full protocol | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/spearbit-buck-1219.pdf) |
| **SSC** | Full protocol | ✅ Complete | [View](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/Strong%20DAO%20Smart%20Contracts%20_%20SSC.pdf) |

All critical and high-severity findings have been resolved.

### Audit Coverage

| Contract | Audited |
|----------|---------|
| BUCK Token | ✅ |
| Liquidity Window (mint/redeem) | ✅ |
| Liquidity Reserve | ✅ |
| Policy Manager | ✅ |
| Oracle Adapter | ✅ |
| Rewards Engine | ✅ |
| Collateral Attestation | ✅ |

## Upgradeability

### Proxy Pattern

Buck uses UUPS (Universal Upgradeable Proxy Standard):

| Benefit | Description |
|---------|-------------|
| **Bug fixes** | Critical issues can be patched |
| **Improvements** | New features can be added |
| **Stable addresses** | Your BUCK token address never changes |

### Upgrade Safeguards

| Control | Description |
|---------|-------------|
| **48-hour timelock** | All upgrades delayed 48 hours minimum |
| **Multi-sig required** | Multiple signatures needed |
| **Public announcement** | Upgrades announced in advance |
| **Community review** | Code published before execution |

### What CAN'T Be Changed Without Notice

- Your BUCK balance
- Your ability to redeem
- Core token mechanics (ERC-20 standard)
- Historical transactions

{% hint style="info" %}
**Timelock transparency:** Anyone can monitor pending upgrades on-chain before they execute.
{% endhint %}

## Access Control

### Role-Based Permissions

| Role | Permissions | Holder |
|------|-------------|--------|
| **ADMIN_ROLE** | Upgrades, emergency pause | Multi-sig |
| **MINTER_ROLE** | Mint BUCK tokens | Liquidity Window contract only |
| **PAUSER_ROLE** | Pause operations | Multi-sig + select team |
| **ORACLE_ROLE** | Update price feeds | Oracle Adapter contract |
| **ATTESTOR_ROLE** | Submit reserve attestations | The Network Firm |

### Multi-Sig Configuration

| Property | Value |
|----------|-------|
| **Admin Wallet** | `0x376269214bB78b3D4f31d17600499b439c1aCB4b` |
| **Threshold** | Multi-sig required |
| **Signers** | Core team members |

No single person can execute privileged operations.

## Emergency Controls

### Pause Functionality

In case of critical vulnerability or market emergency:

| Function | Who Can Call | Effect |
|----------|--------------|--------|
| `pause()` | PAUSER_ROLE | Halt minting/redemption |
| `unpause()` | ADMIN_ROLE | Resume operations |

### When Pause Would Be Used

- Critical smart contract vulnerability discovered
- Oracle malfunction detected
- Extreme market conditions
- Regulatory requirement

### User Impact During Pause

| Function | During Pause |
|----------|--------------|
| Mint BUCK | ⏸️ Paused |
| Redeem BUCK | ⏸️ Paused |
| Transfer BUCK | ✅ Normal |
| Hold BUCK | ✅ Value continues accruing |

Your BUCK holdings remain safe and continue earning yield even during a pause.

## Custody & Key Management

### Treasury Custody

| Property | Details |
|----------|---------|
| **Provider** | Fireblocks |
| **Type** | Institutional MPC custody |
| **Certification** | SOC 2 Type II |
| **Insurance** | Covered by Fireblocks policy |

### Key Security

| Layer | Protection |
|-------|------------|
| **MPC** | No single key can sign |
| **Hardware** | Keys stored in secure hardware |
| **Geographic** | Distributed across locations |
| **Access** | Strict authentication required |

## Smart Contract Risks

### Potential Vulnerabilities

| Risk | Mitigation |
|------|------------|
| **Reentrancy** | Checks-effects-interactions pattern, audited |
| **Overflow/Underflow** | Solidity 0.8+ built-in checks |
| **Access control bypass** | OpenZeppelin AccessControl, audited |
| **Oracle manipulation** | NASDAQ-based pricing, TWAP |
| **Flash loan attacks** | No flash-loan vulnerable functions |

### What Audits Don't Guarantee

Audits reduce but don't eliminate risk:

- Unknown attack vectors may exist
- Economic exploits may not be covered
- Composability risks with other protocols
- Future vulnerabilities in dependencies

## Bug Bounty Program

We maintain an active bug bounty to incentivize responsible disclosure:

| Severity | Reward |
|----------|--------|
| **Critical** | Up to $500,000 |
| **High** | Up to $50,000 |
| **Medium** | Up to $10,000 |
| **Low** | Up to $1,000 |

### Scope

| In Scope | Out of Scope |
|----------|--------------|
| All deployed contracts | Third-party services |
| Oracle infrastructure | Social engineering |
| Frontend security | Already known issues |

**Report to:** security@buck.io

{% hint style="success" %}
**Responsible disclosure:** We work with researchers to fix issues before public disclosure and credit all valid reports.
{% endhint %}

## Operational Security

### Deployment Process

| Stage | Controls |
|-------|----------|
| **Development** | Code review required |
| **Testing** | Full test suite + fuzzing |
| **Staging** | Testnet deployment |
| **Audit** | External review |
| **Deployment** | Multi-sig execution |
| **Monitoring** | 24/7 alerting |

### Incident Response

| Severity | Response Time | Action |
|----------|---------------|--------|
| **Critical** | < 1 hour | Pause + investigate |
| **High** | < 4 hours | Team mobilized |
| **Medium** | < 24 hours | Scheduled fix |
| **Low** | < 1 week | Queued for update |

## Risk Summary

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Smart contract exploit | Low | Critical | 3 audits, bug bounty |
| Malicious upgrade | Very Low | Critical | Timelock, multi-sig |
| Key compromise | Very Low | Critical | MPC custody, multi-sig |
| Operational error | Low | Medium | Access controls, testing |
| Dependency vulnerability | Low | Medium | Regular updates, monitoring |

---

*Next: [Reserve Attestations →](reserve-attestations.md)*
