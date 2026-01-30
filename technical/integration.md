---
description: How to integrate with Buck Protocol
---

# Integration Guide

## Overview

This guide covers how to integrate Buck Protocol into your application, including minting, redeeming, and reading on-chain data.

## Quick Start

### Contract Addresses

```javascript
const CONTRACTS = {
  BUCK_TOKEN: "0xdb13997f4D83EF343845d0bAEb27d1173dF8c224",
  LIQUIDITY_WINDOW: "0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E",
  USDC: "0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48"
};
```

### ABIs

Download full ABIs from our [GitHub repository](https://github.com/buck-labs/buck-v1/tree/master/abis).

## Minting BUCK

### JavaScript (ethers.js)

```javascript
const { ethers } = require('ethers');

// Contract addresses
const USDC = '0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48';
const LIQUIDITY_WINDOW = '0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E';

// ABIs (simplified)
const ERC20_ABI = [
  'function approve(address spender, uint256 amount) returns (bool)',
  'function balanceOf(address account) view returns (uint256)'
];

const WINDOW_ABI = [
  'function mint(address collateral, uint256 amount)',
  'function getFee(bool isMint) view returns (uint256)'
];

async function mintBuck(signer, usdcAmount) {
  // 1. Check current fee
  const window = new ethers.Contract(LIQUIDITY_WINDOW, WINDOW_ABI, signer);
  const fee = await window.getFee(true);
  console.log(`Current mint fee: ${fee} bps`);

  // 2. Approve USDC spending
  const usdc = new ethers.Contract(USDC, ERC20_ABI, signer);
  const approveTx = await usdc.approve(LIQUIDITY_WINDOW, usdcAmount);
  await approveTx.wait();
  console.log('USDC approved');

  // 3. Mint BUCK
  const mintTx = await window.mint(USDC, usdcAmount);
  await mintTx.wait();
  console.log('BUCK minted successfully');
}
```

### Python (web3.py)

```python
from web3 import Web3

# Connect to Ethereum
w3 = Web3(Web3.HTTPProvider('https://eth-mainnet.g.alchemy.com/v2/YOUR_KEY'))

# Contract addresses
USDC = '0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48'
LIQUIDITY_WINDOW = '0x6E87adb23ac0e150Ca9F76C33Df2AdCae508548E'

# Load contracts
usdc = w3.eth.contract(address=USDC, abi=ERC20_ABI)
window = w3.eth.contract(address=LIQUIDITY_WINDOW, abi=WINDOW_ABI)

def mint_buck(account, usdc_amount):
    # Approve USDC
    approve_tx = usdc.functions.approve(
        LIQUIDITY_WINDOW, 
        usdc_amount
    ).build_transaction({
        'from': account.address,
        'nonce': w3.eth.get_transaction_count(account.address)
    })
    signed = account.sign_transaction(approve_tx)
    w3.eth.send_raw_transaction(signed.rawTransaction)
    
    # Mint BUCK
    mint_tx = window.functions.mint(
        USDC, 
        usdc_amount
    ).build_transaction({
        'from': account.address,
        'nonce': w3.eth.get_transaction_count(account.address)
    })
    signed = account.sign_transaction(mint_tx)
    return w3.eth.send_raw_transaction(signed.rawTransaction)
```

## Redeeming BUCK

### JavaScript (ethers.js)

```javascript
const BUCK = '0xdb13997f4D83EF343845d0bAEb27d1173dF8c224';

const BUCK_ABI = [
  'function approve(address spender, uint256 amount) returns (bool)',
  'function balanceOf(address account) view returns (uint256)',
  'function getExchangeRate() view returns (uint256)'
];

const WINDOW_ABI = [
  'function redeem(uint256 buckAmount, address collateral)',
  'function getFee(bool isMint) view returns (uint256)'
];

async function redeemBuck(signer, buckAmount) {
  // 1. Check exchange rate
  const buck = new ethers.Contract(BUCK, BUCK_ABI, signer);
  const rate = await buck.getExchangeRate();
  console.log(`Current BUCK price: $${ethers.formatUnits(rate, 6)}`);

  // 2. Approve BUCK spending
  const approveTx = await buck.approve(LIQUIDITY_WINDOW, buckAmount);
  await approveTx.wait();

  // 3. Redeem for USDC
  const window = new ethers.Contract(LIQUIDITY_WINDOW, WINDOW_ABI, signer);
  const redeemTx = await window.redeem(buckAmount, USDC);
  await redeemTx.wait();
  console.log('Redeemed BUCK for USDC');
}
```

## Reading Exchange Rate

### Get Current BUCK Price

```javascript
const BUCK_ABI = [
  'function getExchangeRate() view returns (uint256)',
  'function totalSupply() view returns (uint256)'
];

async function getBuckPrice(provider) {
  const buck = new ethers.Contract(BUCK, BUCK_ABI, provider);
  
  const rate = await buck.getExchangeRate();
  const price = ethers.formatUnits(rate, 6);
  
  console.log(`1 BUCK = $${price}`);
  return price;
}
```

### Calculate USD Value

```javascript
async function getBuckUsdValue(provider, buckAmount) {
  const buck = new ethers.Contract(BUCK, BUCK_ABI, provider);
  
  const rate = await buck.getExchangeRate();
  const usdValue = (buckAmount * rate) / 1e18;
  
  return ethers.formatUnits(usdValue, 6);
}
```

## Checking Fees

### Get Current Fee Rate

```javascript
async function getCurrentFee(provider) {
  const window = new ethers.Contract(LIQUIDITY_WINDOW, WINDOW_ABI, provider);
  
  const mintFee = await window.getFee(true);
  const redeemFee = await window.getFee(false);
  
  console.log(`Mint fee: ${mintFee} bps`);
  console.log(`Redeem fee: ${redeemFee} bps`);
  
  return { mintFee, redeemFee };
}
```

## Events

### Listen for Mints

```javascript
const WINDOW_EVENTS = [
  'event Minted(address indexed user, address collateral, uint256 amount, uint256 buckReceived, uint256 fee)'
];

async function listenForMints(provider) {
  const window = new ethers.Contract(LIQUIDITY_WINDOW, WINDOW_EVENTS, provider);
  
  window.on('Minted', (user, collateral, amount, buckReceived, fee) => {
    console.log(`User ${user} minted ${ethers.formatUnits(buckReceived, 18)} BUCK`);
  });
}
```

### Listen for Redemptions

```javascript
const WINDOW_EVENTS = [
  'event Redeemed(address indexed user, uint256 buckBurned, address collateral, uint256 amountReceived, uint256 fee)'
];

async function listenForRedemptions(provider) {
  const window = new ethers.Contract(LIQUIDITY_WINDOW, WINDOW_EVENTS, provider);
  
  window.on('Redeemed', (user, buckBurned, collateral, amountReceived, fee) => {
    console.log(`User ${user} redeemed ${ethers.formatUnits(buckBurned, 18)} BUCK`);
  });
}
```

## Best Practices

### Gas Estimation

Always estimate gas before sending transactions:

```javascript
async function mintWithGasEstimate(signer, amount) {
  const window = new ethers.Contract(LIQUIDITY_WINDOW, WINDOW_ABI, signer);
  
  // Estimate gas
  const gasEstimate = await window.mint.estimateGas(USDC, amount);
  const gasLimit = gasEstimate * 120n / 100n; // 20% buffer
  
  // Send with estimate
  const tx = await window.mint(USDC, amount, { gasLimit });
  return tx.wait();
}
```

### Error Handling

```javascript
async function safeMint(signer, amount) {
  try {
    const window = new ethers.Contract(LIQUIDITY_WINDOW, WINDOW_ABI, signer);
    const tx = await window.mint(USDC, amount);
    const receipt = await tx.wait();
    
    if (receipt.status === 0) {
      throw new Error('Transaction reverted');
    }
    
    return receipt;
  } catch (error) {
    if (error.code === 'INSUFFICIENT_FUNDS') {
      console.error('Not enough ETH for gas');
    } else if (error.code === 'UNPREDICTABLE_GAS_LIMIT') {
      console.error('Transaction would fail - check allowance or balance');
    } else {
      console.error('Unknown error:', error.message);
    }
    throw error;
  }
}
```

### Checking Allowances

```javascript
async function ensureAllowance(signer, tokenAddress, spender, amount) {
  const token = new ethers.Contract(tokenAddress, ERC20_ABI, signer);
  
  const allowance = await token.allowance(signer.address, spender);
  
  if (allowance < amount) {
    const approveTx = await token.approve(spender, amount);
    await approveTx.wait();
    console.log('Approval confirmed');
  }
}
```

## SDK (Coming Soon)

We're working on an official Buck SDK for easier integration:

```javascript
// Coming soon
import { Buck } from '@buck-protocol/sdk';

const buck = new Buck({ provider });

// Simple mint
await buck.mint('1000', 'USDC');

// Simple redeem  
await buck.redeem('1000');

// Get price
const price = await buck.getPrice();
```

## Support

Need help integrating?

* **Discord:** [Join our server](https://discord.gg/buck)
* **GitHub:** [Open an issue](https://github.com/buck-labs/buck-v1/issues)
* **Email:** dev@buck.io

---

*Next: [Competitive Landscape →](../resources/comparison.md)*
