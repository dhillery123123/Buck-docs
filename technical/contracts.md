---
description: Contract addresses
---

# Smart Contracts

## Core Contracts

| Contract | Address |
|----------|---------|
| **BUCK Token** | [`0xdb13997f4D83EF343845d0bAEb27d1173dF8c224`](https://etherscan.io/address/0xdb13997f4D83EF343845d0bAEb27d1173dF8c224) |
| **Liquidity Window** | [`0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E`](https://etherscan.io/address/0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E) |
| **Liquidity Reserve** | [`0x1A426E3a87368a4851f7443Ff656A054Af872f66`](https://etherscan.io/address/0x1A426E3a87368a4851f7443Ff656A054Af872f66) |
| **Policy Manager** | [`0x79f86b9E0ac84C7580575089E453431D77905E36`](https://etherscan.io/address/0x79f86b9E0ac84C7580575089E453431D77905E36) |
| **Oracle Adapter** | [`0xa6c5f4D041192C2019E77f679eA02e9684235Fd9`](https://etherscan.io/address/0xa6c5f4D041192C2019E77f679eA02e9684235Fd9) |
| **Rewards Engine** | [`0x159c1C0F796a02111334cC280eE001b091a9580C`](https://etherscan.io/address/0x159c1C0F796a02111334cC280eE001b091a9580C) |
| **Collateral Attestation** | [`0x1aEEEf99704258947A9ea77eF021d5e0551c0428`](https://etherscan.io/address/0x1aEEEf99704258947A9ea77eF021d5e0551c0428) |
| **Access Registry** | [`0xbCc6de2423B496cb36C3278dC487EfD9c5C550B6`](https://etherscan.io/address/0xbCc6de2423B496cb36C3278dC487EfD9c5C550B6) |

## Administrative Addresses

| Role | Address |
|------|---------|
| **Admin Wallet** | `0x376269214bB78b3D4f31d17600499b439c1aCB4b` |
| **Treasury Wallet** | `0x5d105791469064cA0764cfaCfc577c286351CFAD` |
| **Distributor Wallet** | `0xC2a2dbBD627872E78894F3C1c403Fbe1cd4C36df` |
| **CAS Attestor** | `0x6f31810c8e6bFaf3BA486B4b7ce651b023423Fa3` |

## Security

All contracts use the UUPS upgradeable proxy pattern and have been audited by Cyfrin, Spearbit, and SSC.

Admin wallet operations — including contract upgrades and configuration adjustments — are secured by a **Fireblocks 4/4 MPC approval system** with a TAP (Transaction Authorization Policy) and function-level whitelist. Every admin action requires approval from all 4 MPC key holders before it can execute, and only pre-approved contract functions can be called.

Treasury and Liquidity Reserve withdrawals/operations are also under a separate **4/4 MPC multisig** in Fireblocks. No single individual can unilaterally upgrade contracts, change protocol parameters, or move funds.

## Collateral Attestation

An off-chain attestor periodically publishes two values to the CollateralAttestation contract ([`0x1aEEEf99704258947A9ea77eF021d5e0551c0428`](https://etherscan.io/address/0x1aEEEf99704258947A9ea77eF021d5e0551c0428)):

- **Portfolio value (V)** — The current value of protocol-held STRC and other collateral
- **Haircut coefficient (HC)** — A conservative discount applied to the portfolio value

The contract computes the collateral ratio as:

```
CR = (USDC in Liquidity Reserve + haircutted portfolio value) / BUCK total supply
```

The protocol currently maintains a CR of **~1.6x**, meaning there's $1.60+ backing every $1 of BUCK. If the attestation becomes stale (exceeds a configurable freshness window), mints and refunds are paused automatically until a fresh attestation is published.

For monthly attestation reports, see [Independent Reserve Attestations](../protocol/reserve-attestations.md).

## Fees

| Action | Fee | Applied When |
|--------|-----|-------------|
| **Mint** | 10 bps (0.10%) | Minting BUCK from USDC via the Liquidity Window |
| **Refund** | 10 bps (0.10%) | Redeeming BUCK back to USDC via the Liquidity Window |
| **DEX Buy** | 15 bps (0.15%) | Buying BUCK on Curve or Uniswap |
| **DEX Sell** | 15 bps (0.15%) | Selling BUCK on Curve or Uniswap |

All fees are sent to the protocol Treasury (`0x5d105791469064cA0764cfaCfc577c286351CFAD`). Fee rates are configurable by the admin via the PolicyManager contract ([`0x79f86b9E0ac84C7580575089E453431D77905E36`](https://etherscan.io/address/0x79f86b9E0ac84C7580575089E453431D77905E36)) and may change based on protocol health band.

## Resources

| Resource | Link |
|----------|------|
| GitHub | [github.com/buck-labs/buck-v1](https://github.com/buck-labs/buck-v1) |
| Audit Reports | [View All](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/) |

---

*[Back to FAQ →](../resources/faq.md)*
