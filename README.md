# 🌾 MLT Farm — Yield Farming on LitVM

> A fully on-chain yield farming protocol built on **LitVM LiteForge testnet** — the first trustless EVM-compatible rollup secured by Litecoin.

---

## 🔗 Live Contracts (LiteForge Testnet)

| Contract | Address |
|---|---|
| MLTToken (ERC-20 + Faucet) | `0x705c4D8Deb24F25d92c9e96621df6036134810bD` |
| MLTFarm (Yield Farm) | `0xd11793cF5a4B78Dd4607c01d1f064BA746Bc5E4F` |

🔍 View on explorer: [liteforge.explorer.caldera.xyz](https://liteforge.explorer.caldera.xyz)

---

## 🧠 What is MLT Farm?

MLT Farm is a single-asset yield farming protocol where users stake **MLT tokens** to earn **MLT rewards** in real time — with no lock-up period and no impermanent loss.

It is deployed on **LitVM**, a zero-knowledge rollup built on Litecoin using Arbitrum Orbit, combining EVM compatibility with Litecoin's security as the settlement layer.

---

## ✨ Features

- ✅ **ERC-20 Token** — MLT token with 1,000,000 total supply
- ✅ **Built-in Faucet** — anyone can claim 1,000 MLT free every 24 hours
- ✅ **Multi-pool architecture** — supports multiple staking pools with different tokens
- ✅ **Real-time rewards** — rewards accrue every second, claimable anytime
- ✅ **Live APY** — on-chain APY calculation per pool
- ✅ **No lock-up** — stake and unstake freely at any time
- ✅ **Frontend DApp** — full web interface with Rabby/MetaMask/Zerion support
- ✅ **Mobile ready** — responsive UI with bottom tab bar navigation
- ✅ **Auto network** — app auto-adds LiteForge (Chain 4441) to any wallet
- ✅ **LiteForge native** — deployed and tested on LitVM testnet

---

## 🚀 How to Test

1. Visit the live app
2. Connect your wallet (Rabby, MetaMask, or Zerion)
3. App auto-switches to LiteForge Testnet (Chain 4441)
4. Get free zkLTC gas from the faucet: [liteforge.hub.caldera.xyz](https://liteforge.hub.caldera.xyz)
5. Click **"Claim Test MLT"** → receive 1,000 MLT free
6. Click **Approve MLT** → confirm in wallet
7. Enter amount → click **Stake MLT** → confirm
8. Watch rewards accumulate every second ⏱️
9. Click **Claim Rewards** anytime

---

## 🏗️ Smart Contracts

### `MLTToken.sol`
ERC-20 token built with OpenZeppelin. Includes a built-in faucet so anyone can claim 1,000 MLT every 24 hours for testing.

| Function | Description |
|---|---|
| `faucet()` | Claim 1,000 MLT free (24hr cooldown) |
| `timeUntilNextClaim(address)` | Check cooldown remaining |
| `fundFaucet(amount)` | Owner funds the faucet pool |

### `MLTFarm.sol`
Multi-pool yield farm. Key functions:

| Function | Description |
|---|---|
| `addPool(token, rate)` | Owner adds a new staking pool |
| `stake(poolId, amount)` | Deposit tokens into a pool |
| `unstake(poolId, amount)` | Withdraw tokens from a pool |
| `claimRewards(poolId)` | Claim accumulated rewards |
| `pendingRewards(poolId, user)` | View real-time pending rewards |
| `getAPY(poolId)` | Returns current APY in basis points |
| `poolLength()` | Returns number of active pools |

---

## 🖥️ Frontend

The frontend (`app.html`) is a single-file DApp built with:
- **ethers.js v6** — wallet connection and contract interaction
- **Vanilla HTML/CSS/JS** — no framework dependencies
- **EIP-6963** — supports Rabby, MetaMask, Zerion, Rainbow

### Pages:
- **Earn** — stake/unstake/claim + faucet + live rewards
- **Pools** — all active pools with APY and TVL
- **Analytics** — protocol stats and charts

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
| Wallet Support | Rabby, MetaMask, Zerion |

---

## 🌐 Network Info

| Property | Value |
|---|---|
| Network | LiteForge (LitVM Testnet) |
| Chain ID | 4441 |
| RPC URL | https://liteforge.rpc.caldera.xyz/http |
| Gas Token | zkLTC |
| Block Time | ~0.4 seconds |
| Explorer | https://liteforge.explorer.caldera.xyz |
| Settlement | Litecoin |

---

## 📁 Project Structure

```
mlt-farm/
├── index.html          # Landing page
├── app.html            # DApp frontend
├── favicon.png         # App icon
└── README.md           # This file
```

---

## 🔮 Roadmap

- [ ] Add more staking pools
- [ ] Deploy to LitVM mainnet
- [ ] Referral rewards system
- [ ] Analytics dashboard
- [ ] Token swap integration

---

## 🤝 Built on LitVM

LitVM is the first trustless EVM-compatible rollup secured by Litecoin, combining:
- **Arbitrum Orbit** for EVM compatibility
- **BitcoinOS Grail Bridge** for trustless LTC bridging
- **Litecoin's security** as the settlement foundation

Learn more: [litvm.com](https://www.litvm.com) · [docs.litvm.com](https://docs.litvm.com)

---

## 📬 Community

- **Telegram:** [t.me/litecoinvm](https://t.me/litecoinvm)
- **Twitter:** [@LitecoinVM](https://twitter.com/LitecoinVM)

---

*Built on LitVM LiteForge Testnet · 2026*