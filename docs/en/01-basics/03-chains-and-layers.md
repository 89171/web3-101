# 03. Public Chains, Layer 1, and Layer 2

## One-Sentence Version

A public chain is a blockchain network anyone can use. Layer 1 is the base chain. Layer 2 is a faster, cheaper layer built on top.

## Why Are There So Many Chains?

If there were only one blockchain, life would be simple. In reality there are many: Bitcoin, Ethereum, Solana, BNB Chain, Polygon, Arbitrum, Base, and more.

Why? Because blockchains face a famous tradeoff called the **blockchain trilemma**:

> **Decentralization, security, and performance: it is hard to maximize all three at the same time.**

- If a chain is highly secure and decentralized, performance is usually limited.
- If it is fast and decentralized, security can be harder to guarantee.
- If it is fast and secure, it may become more centralized because participation is harder.

Different chains make different tradeoffs. There is no universal best chain, only tradeoffs.

## Public Chains vs Consortium Chains vs Private Chains

| Type | Who Can Use It | Who Can Produce Blocks | Typical Use |
|---|---|---|---|
| **Public chain** | Anyone | Anyone, subject to protocol rules | Bitcoin, Ethereum |
| **Consortium chain** | Approved members | Members of the consortium | A bank settlement network |
| **Private chain** | One organization | That organization | Internal audit or record system |

Most of what this handbook calls Web3 happens on **public chains**. Consortium and private chains may use blockchain techniques, but they are closer to shared databases among already-trusted parties.

Below, "chain" usually means a public chain.

## Layer 1: The Base Layer

**Layer 1 (L1) = an independent blockchain with its own consensus mechanism.**

It processes transactions, produces blocks, and settles its own state.

Common L1s:

| Chain | Simple Description |
|---|---|
| **Bitcoin** | The earliest major chain, focused on value storage and transfers. |
| **Ethereum** | The first chain to run general-purpose smart contracts at large scale. DeFi and NFTs largely started here, but Ethereum L1 is slow and expensive. |
| **Solana** | Focuses on high speed and low fees on a single high-performance chain. Validator requirements are higher than Ethereum's. |
| **BNB Chain** | Strongly influenced by the Binance ecosystem. Cheap and fast, but more centralized in validators and governance. |
| **Tron** | Widely used for stablecoin transfers, especially USDT. |

Key point: **L1s are independent ledgers**. BTC on Bitcoin does not automatically exist on Ethereum, and ETH on Ethereum does not automatically exist on Solana.

## Layer 2: Faster Roads on Top of the Base Layer

Ethereum is secure and decentralized, but Ethereum L1 is slow and expensive when crowded. This is hard to use for daily small transactions.

**Layer 2 (L2) = a scaling layer built on top of L1. It processes transactions off the base layer and settles results back to L1.**

Analogy:

> L1 is like a court: slow and expensive, but final.  
> L2 is like local mediation: faster and cheaper for everyday activity, with final results reported back to the court.

If you make 100 transactions on an L2, the L2 processes them internally and submits a compressed result or proof to L1. L1 does far less work.

Benefits of L2:

- **Faster**: often seconds rather than minutes.
- **Cheaper**: often a tiny fraction of L1 cost.
- **Security inheritance**: mature rollups submit data or proofs to L1, so their security depends heavily on L1.

But "uses L1 security" does not mean every L2 is as safe as L1. L2s can have their own risks: sequencer downtime, censorship, bridge contracts, upgrade admin keys, and immature proof systems. Newer L2s should be treated as infrastructure still maturing.

Representative Ethereum L2s:

| L2 | Notes |
|---|---|
| **Arbitrum** | One of the most-used Ethereum L2s. |
| **Optimism** | Another major optimistic rollup. |
| **Base** | Coinbase-backed L2, relatively beginner-friendly. |
| **zkSync / Scroll / Linea** | ZK-based L2s using zero-knowledge proofs. |

You do not need to understand every technical difference at first. Remember: **L2s make L1 cheaper and faster, but their security model depends on exactly how they publish data, proofs, and exits back to L1.**

## Moving Money Across Chains

Chains are separate ledgers. To move assets between them, people use **bridges**.

A bridge roughly works like this:

> Lock 100 USDT on Chain A -> receive 100 equivalent receipts on Chain B -> use them on Chain B -> reverse the process to return.

Bridges are convenient, but they are among the most frequently attacked parts of Web3. They hold large amounts of value and have broad attack surfaces.

Practical safety tips:

- **Avoid bridging when you can.** Use native assets on the chain you need.
- **Use official bridges** when bridging is necessary.
- **Split large transfers** into smaller batches.

## Quick Memory Table

| Concept | One-Sentence Version |
|---|---|
| Public chain | A blockchain anyone can use and participate in. |
| L1 | An independent base blockchain with its own consensus and settlement. |
| L2 | A faster, cheaper layer built on L1, with a security model that depends on how it relies on L1. |
| Bridge | Infrastructure for moving assets between chains; useful but risky. |

## What to Read Next

- To understand transaction fees: [04. What Is Gas?](04-what-is-gas.md)
- To understand wallet addresses: [05. Wallets, Addresses, Private Keys, and Seed Phrases](../02-wallets/01-wallet-basics.md)

---

> If you remember one sentence:
> **L1 is the base layer, L2 is a faster road on top, and assets do not automatically move between chains. Bridges move them, but bridges add risk.**
