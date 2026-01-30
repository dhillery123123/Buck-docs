---
description: Contract addresses and architecture
---

# Smart Contracts

## Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                      USER INTERACTIONS                          │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                     LIQUIDITY WINDOW                            │
│              (Mint, Redeem, Exchange Rate)                      │
└─────────────────────────────────────────────────────────────────┘
         │                   │                   │
         ▼                   ▼                   ▼
┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐
│   BUCK TOKEN    │  │    LIQUIDITY    │  │     POLICY      │
│   ERC-20        │  │    RESERVE      │  │    MANAGER      │
└─────────────────┘  └─────────────────┘  └─────────────────┘
                              │
                              ▼
                     ┌─────────────────┐
                     │     ORACLE      │
                     │    ADAPTER      │
                     └─────────────────┘
```

## Core Contracts

| Contract | Address | Purpose |
|----------|---------|---------|
| **BUCK Token** | `0xdb13997f4D83EF343845d0bAEb27d1173dF8c224` | ERC-20 savings coin |
| **Liquidity Window** | `0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E` | Mint/redeem gateway |
| **Liquidity Reserve** | `0x1A426E3a87368a4851f7443Ff656A054Af872f66` | Asset custody |
| **Policy Manager** | `0x79f86b9E0ac84C7580575089E453431D77905E36` | Fee logic |
| **Oracle Adapter** | `0xa6c5f4D041192C2019E77f679eA02e9684235Fd9` | Price feeds |
| **Rewards Engine** | `0x159c1C0F796a02111334cC280eE001b091a9580C` | Distribution |
| **Collateral Attestation** | `0x1aEEEf99704258947A9ea77eF021d5e0551c0428` | Reserve verification |
| **Access Registry** | `0xbCc6de2423B496cb36C3278dC487EfD9c5C550B6` | Permissions |

## Implementation Addresses

| Contract | Proxy | Implementation |
|----------|-------|----------------|
| BUCK Token | `0xdb13997f...c224` | `0x1d66007CA026AeA5e0476D5c0807c2Eb46A18fF4` |
| Liquidity Window | `0x6E87adb2...548E` | `0x1281C23dbB2afEED23428AD52DA26a04A5dD655c` |
| Liquidity Reserve | `0x1A426E3a...f66` | `0x1B38a250C3DaB104E4299F5BE2957dFE0AeE5e83` |
| Policy Manager | `0x79f86b9E...E36` | `0xd7B66A4937c561ac0eC76a912caD36e4662dA696` |
| Rewards Engine | `0x159c1C0F...80C` | `0xfE07470aE5711f1d3F10C4627854C3C8Bf1e8F5e` |
| Collateral Attestation | `0x1aEEEf99...428` | `0x224d327C36CA9569D86D250EB77bC88Fc8D4bD41` |

## Administrative Addresses

| Role | Address |
|------|---------|
| Admin Wallet | `0x376269214bB78b3D4f31d17600499b439c1aCB4b` |
| Treasury Wallet | `0x5d105791469064cA0764cfaCfc577c286351CFAD` |
| Distributor Wallet | `0xC2a2dbBD627872E78894F3C1c403Fbe1cd4C36df` |
| CAS Attestor | `0x6f31810c8e6bFaf3BA486B4b7ce651b023423Fa3` |

## External Dependencies

| Contract | Address |
|----------|---------|
| USDC | `0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48` |

## Key Functions

### BUCK Token

```solidity
// Get current exchange rate (BUCK price in USDC)
function getExchangeRate() external view returns (uint256);

// Standard ERC-20
function transfer(address to, uint256 amount) external returns (bool);
function approve(address spender, uint256 amount) external returns (bool);
function balanceOf(address account) external view returns (uint256);
```

### Liquidity Window

```solidity
// Mint BUCK by depositing collateral
function mint(address collateral, uint256 amount) external;

// Redeem BUCK for collateral
function redeem(uint256 buckAmount, address collateral) external;

// Get current fee rate
function getFee(bool isMint) external view returns (uint256);
```

### Oracle Adapter

```solidity
// Get current STRC price
function getPrice() external view returns (uint256);

// Get time-weighted average price
function getTWAP(uint256 period) external view returns (uint256);

// Check if market is open
function isMarketOpen() external view returns (bool);
```

## Access Control

| Role | Permissions |
|------|-------------|
| ADMIN\_ROLE | Upgrades, emergency pause |
| MINTER\_ROLE | Mint BUCK tokens |
| PAUSER\_ROLE | Pause operations |
| ORACLE\_ROLE | Update price feeds |
| ATTESTOR\_ROLE | Submit attestations |

## Security

### Upgradeability

* UUPS proxy pattern
* 48-hour timelock on upgrades
* Multi-sig required

### Emergency Controls

| Function | Access | Effect |
|----------|--------|--------|
| `pause()` | PAUSER\_ROLE | Halt operations |
| `unpause()` | ADMIN\_ROLE | Resume operations |
| `emergencyWithdraw()` | ADMIN\_ROLE + timelock | Extract funds |

## Source Code

| Resource | Link |
|----------|------|
| GitHub Repository | [github.com/buck-labs/buck-v1](https://github.com/buck-labs/buck-v1) |
| Block Explorer | [Etherscan](https://etherscan.io/address/0xdb13997f4D83EF343845d0bAEb27d1173dF8c224) |
| Audit Reports | [View All](https://github.com/buck-labs/buck-v1/blob/master/docs/audits/) |

---

*Next: [Integration Guide →](integration.md)*
