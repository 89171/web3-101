# 04. What Is Gas?

## One-Sentence Version

Gas is the **network fee** you pay for an on-chain action. Part of it compensates validators or miners, and on some chains part of it is burned by the protocol.

## Why Pay This Fee?

Imagine the "10 friends keeping a ledger" example again. If writing to the ledger were free, someone could spam it:

> "A sends 0 dollars to A" repeated one million times.

The network would be flooded.

So blockchains need an anti-spam mechanism: **if you want to use network resources, you must pay**. That payment is gas, also called a network fee, transaction fee, or miner fee depending on the chain and era.

Gas has two main purposes:

1. **Prevent spam**: every transaction has a cost.
2. **Incentivize validators or miners**: they are paid to process real transactions.

## How Is It Calculated?

Different chains use different formulas, but the intuition is:

> **Gas fee = work required by the transaction x current unit price**

Like a taxi fare:

> Taxi fare = distance x price per distance  
> Gas fee = computation/storage work x current network price

- **Work required** depends on what you do. A simple transfer is cheap. A complex DeFi transaction costs more.
- **Unit price** depends on network congestion. When many people compete for block space, fees rise.

This is why the same Ethereum transfer might cost 1 dollar one day and 50 dollars another day. The network may be more congested, and the ETH price may also have changed. Wallets usually show the fee converted into dollars, so both factors matter.

## Common Questions

**"Do I pay gas even if I transfer zero value?"**  
Yes. Gas is not based on how much value you transfer. It is based on network resources consumed by the operation.

**"Who receives the gas fee?"**  
Not always one party. On Ethereum-style EIP-1559 chains, fees roughly have two parts:

- **Base fee**: calculated by the protocol and burned.
- **Priority fee**: paid to the validator to prioritize your transaction.

Other chains have different designs, but the basic idea is the same: **gas is resource pricing, not a random platform fee**.

**"What token do I use to pay gas?"**  
You pay gas with the chain's native coin:

- Ethereum and many Ethereum L2s -> ETH
- Bitcoin -> BTC
- Solana -> SOL
- BNB Chain -> BNB

Important: if you want to use a chain, keep a little native coin in your wallet. A common beginner problem is: "I have USDT, why can't I send it?" Because you may not have ETH, SOL, TRX, or BNB to pay gas.

## Fee Ranges

These numbers change over time. They are only rough scale references:

| Chain | Typical Network Fee Scale for a Simple Transfer |
|---|---|
| Bitcoin | $0.5-$5 |
| Ethereum L1 | $0.5-$20, sometimes $50+ when congested |
| Ethereum L2s (Arbitrum, Base, etc.) | $0.01-$0.1 |
| Solana | $0.0001-$0.01 |
| Tron | TRX transfers are usually cheap; TRC-20 USDT consumes energy and can burn several dollars' worth of TRX if you have no energy |

Tron's fee model is special. Normal transfers consume bandwidth. Smart contract calls, such as TRC-20 USDT transfers, consume energy. You can burn TRX directly, or stake/rent resources to reduce costs. This is why many people use Tron for USDT transfers, but it does not mean Tron is always free.

## How to Avoid Gas Problems

1. **Check which chain you are on.** USDT on Ethereum L1, L2s, Tron, and Solana all have different fee models.
2. **Wait if you are not in a hurry.** Fees are lower when the network is less congested.
3. **Always keep a little native coin.** ETH, SOL, BNB, TRX, or the relevant native coin is needed for activity.
4. **Use L2 for small Ethereum activity.** Ethereum L1 is better for high-value or maximum-security operations.
5. **Read the wallet prompt before signing.** If the estimated gas is strangely high, stop.

## Quick Memory Table

| Question | Answer |
|---|---|
| What is gas? | The network fee for an on-chain operation. |
| Who sets the price? | Mostly market demand for block space and protocol rules. |
| What token pays it? | The chain's native coin. |
| How to save gas? | Choose the right chain, avoid congestion, use L2s, keep native coins ready. |

## What to Read Next

Part 1 ends here. Next we move to wallets and identity.

-> [05. Wallets, Addresses, Private Keys, and Seed Phrases](../02-wallets/01-wallet-basics.md)

---

> If you remember one sentence:
> **Gas is the network fee paid in the chain's native coin. Without native coins for gas, you may be unable to move your other assets.**
