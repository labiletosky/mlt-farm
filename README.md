# 🌾 MLT Farm — Yield Farming on LitVM

> A fully on-chain yield farming protocol built on **LitVM LiteForge testnet** — the first trustless EVM-compatible rollup secured by Litecoin.

---

## 🔗 Live Contracts (LiteForge Testnet)

| Contract | Address |
|---|---|
| MLT Token (ERC-20) | `0x494c41cdf4bd62a7a0e379f7356c4564E399f844` |
| MLTFarm (Yield Farm) | `0x63c63f7F63376c9fB1A481aBC22463AF98700d70` |

🔍 View on explorer: [liteforge.explorer.caldera.xyz](https://liteforge.explorer.caldera.xyz)

---

## 🧠 What is MLT Farm?

MLT Farm is a single-asset yield farming protocol where users stake **MLT tokens** to earn **MLT rewards** in real time — with no lock-up period and no impermanent loss.

It is deployed on **LitVM**, a zero-knowledge rollup built on Litecoin using Arbitrum Orbit, combining EVM compatibility with Litecoin's security as the settlement layer.

---

## ✨ Features

- ✅ **ERC-20 Token** — MLT token with 1,000,000 total supply
- ✅ **Multi-pool architecture** — supports multiple staking pools with different tokens
- ✅ **Real-time rewards** — rewards accrue every second, claimable anytime
- ✅ **Live APY** — on-chain APY calculation per pool
- ✅ **No lock-up** — stake and unstake freely at any time
- ✅ **Frontend DApp** — full web interface with Rabby/MetaMask wallet support
- ✅ **LiteForge native** — deployed and tested on LitVM testnet

---

## 🏗️ Smart Contracts

### `MyLitToken.sol`
Standard ERC-20 token built with OpenZeppelin. Mints 1,000,000 MLT to the deployer on deployment.

### `MLTStaking.sol`
Basic single-pool staking contract. Users deposit MLT and earn MLT rewards per second based on their share of the pool.

### `MLTFarm.sol`
Upgraded multi-pool yield farm. Key functions:

| Function | Description |
|---|---|
| `addPool(token, rate)` | Owner adds a new staking pool |
| `stake(poolId, amount)` | Deposit tokens into a pool |
| `unstake(poolId, amount)` | Withdraw tokens from a pool |
| `claimRewards(poolId)` | Claim accumulated rewards |
| `pendingRewards(poolId, user)` | View real-time pending rewards |
| `getAPY(poolId)` | Returns current APY in basis points |

---

## 🖥️ Frontend

The frontend (`index.html`) is a single-file DApp built with:
- **ethers.js v6** — wallet connection and contract interaction
- **Vanilla HTML/CSS/JS** — no framework dependencies
- **Rabby / MetaMask** — EIP-1193 wallet support

### Features:
- Auto-detects and switches to LiteForge (Chain ID 4441)
- Approve → Stake → Unstake → Claim rewards flow
- Live reward counter refreshing every 5 seconds
- Real-time APY and TVL display
- Links to block explorer for both contracts

---

## 🚀 Getting Started

### Add LiteForge to your wallet

| Field | Value |
|---|---|
| Network Name | LiteForge |
| RPC URL | https://liteforge.rpc.caldera.xyz/http |
| Chain ID | 4441 |
| Currency Symbol | zkLTC |
| Block Explorer | https://liteforge.explorer.caldera.xyz |

### Get testnet zkLTC
Visit the faucet: [liteforge.hub.caldera.xyz](https://liteforge.hub.caldera.xyz)

### Use the DApp
1. Open the live app
2. Click **Connect Wallet**
3. Approve MLT → Stake → Earn rewards

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Smart Contracts | Solidity ^0.8.20 |
| Libraries | OpenZeppelin Contracts |
| Deployment | Remix IDE |
| Network | LitVM LiteForge Testnet |
| Frontend | HTML + CSS + ethers.js v6 |
| Hosting | Vercel |
| Wallet | Rabby / MetaMask |

---

## 🌐 Network Info

| Property | Value |
|---|---|
| Network | LiteForge (LitVM Testnet) |
| Chain ID | 4441 |
| Gas Token | zkLTC |
| Block Time | ~0.4 seconds |
| Settlement | Litecoin |

---

## 📁 Project Structure

```
mlt-farm/
├── index.html          # Frontend DApp (single file)
└── README.md           # This file
```

---

## 🔮 Roadmap

- [ ] Add second staking pool with a different token
- [ ] Deploy to LitVM mainnet
- [ ] Add referral rewards system
- [ ] Analytics dashboard
- [ ] Mobile-optimized UI

---

## 🤝 Built on LitVM

LitVM is the first trustless EVM-compatible rollup secured by Litecoin, combining:
- **Arbitrum Orbit** for EVM compatibility
- **BitcoinOS Grail Bridge** for trustless LTC bridging
- **Litecoin's security** as the settlement foundation

Learn more: [litvm.com](https://www.litvm.com) · [docs.litvm.com](https://docs.litvm.com)

---

## 📬 Contact

- **Telegram:** [t.me/litecoinvm](https://t.me/litecoinvm)
- **Twitter:** [@LitecoinVM](https://twitter.com/LitecoinVM)

---

*Built on LitVM LiteForge Testnet · 2026*