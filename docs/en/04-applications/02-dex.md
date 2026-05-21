# 12. DEXs and AMMs

## One-Sentence Version

A DEX is an **on-chain exchange**. An AMM is the most common pricing mechanism: instead of an order book, it uses a mathematical formula.

## DEX vs Traditional Exchange

Traditional exchanges use an **order book**:

> Buyers place bids. Sellers place asks. The exchange matches compatible orders.

This works well off-chain, but on-chain order books are expensive because placing and canceling orders can cost gas.

So many DEXs use **AMMs**: automated market makers.

## AMM Intuition

Imagine a vending machine with two assets:

> 100 apples + 100 oranges.  
> The machine follows one rule: **apples x oranges = 10000** (ignoring fees).

If you put in 10 oranges, the machine now has 110 oranges. To keep the product near 10000, apples must fall to about 90.9. You receive about 9.1 apples.

If you put in 50 oranges, you get more apples, but the price gets worse as the pool becomes imbalanced. That price movement is **slippage**.

The classic AMM formula is:

> **x * y = k**

`x` is the amount of asset A, `y` is the amount of asset B, and `k` is a constant. Real protocols charge fees, so `k` can grow over time, but the pricing intuition remains.

Uniswap V2, PancakeSwap, and SushiSwap are based on this idea. Uniswap V3 introduced concentrated liquidity, and V4 adds more customization, but x*y=k is still the best beginner intuition.

## Liquidity Pools

Where do the assets in the machine come from?

They come from **liquidity providers (LPs)**.

LPs deposit assets into pools so traders can swap. In return, LPs earn a share of trading fees.

| Role | What They Do | Revenue / Cost |
|---|---|---|
| Trader | Swaps tokens | Pays a fee and slippage |
| LP | Provides assets to the pool | Earns fees but takes risk |

Classic AMMs often require two assets to be deposited in equal value. Concentrated liquidity lets LPs provide liquidity only in a chosen price range, which is more efficient but more complex.

## Impermanent Loss

Impermanent loss is a hidden cost for LPs.

Simple version:

> If the relative price of the two pool assets changes, an LP may end up with less value than if they had simply held the two assets.

Example:

> You deposit 1 ETH worth $2000 and 2000 USDC, total $4000.  
> ETH rises to $4000.  
> If you had simply held, you would have $6000.  
> In the pool, arbitrage changes the asset mix: you end with less ETH and more USDC. Your value might be around $5660.  
> The difference is impermanent loss.

Important points:

1. The bigger the price move, the bigger the loss.
2. The more the two assets diverge, the bigger the loss.
3. Stablecoin pairs usually have lower impermanent loss, but still have depeg, contract, and liquidity risk.
4. Fees may or may not offset the loss.

For beginners, if you want to try LPing, use tiny amounts in mature stablecoin pools first.

## Types of DEXs

### 1. AMM-Based DEXs

Use formulas to price trades.

Examples: **Uniswap**, **PancakeSwap**, **Raydium**, **Curve**.

### 2. Concentrated Liquidity AMMs

LPs choose a price range where their liquidity is active. More efficient, but harder to manage.

Example: **Uniswap V3**.

### 3. Order Book DEXs

Use order books, usually on high-performance chains or specialized infrastructure.

Examples: **dYdX**, **Hyperliquid**.

### 4. DEX Aggregators

They route trades through multiple DEXs to find better prices.

Examples: **1inch**, **Matcha**, **Jupiter**.

In practice, many users use aggregators more than single DEXs.

## DEX Practical Risks

### 1. Slippage

The displayed price and final execution price may differ because:

- Your own trade moves the AMM price.
- Prices move while the transaction waits.
- MEV bots may attack high-slippage trades.

Beginners:

- Major pairs: 0.1%-0.5% slippage is often enough.
- Small illiquid tokens may need more, but higher slippage is dangerous.

### 2. MEV and Sandwich Attacks

If you place a large DEX trade, bots may buy before you and sell after you, forcing you into a worse price. This is called a **sandwich attack**.

Defenses:

- Do not set slippage too high.
- Use wallets or aggregators with MEV protection.
- Split large trades.

### 3. Fake Tokens and Fake Pools

Anyone can create a token and a pool. Many fake tokens use the same name as real ones.

Defenses:

- Use official swap links.
- Verify contract addresses from official sites, CoinGecko, or CoinMarketCap.
- Do not trust token names alone.

### 4. Low Liquidity

Illiquid tokens can have brutal slippage.

You may buy 1000 dollars' worth and receive only 700 dollars of value due to slippage. When selling, you may lose again.

Low liquidity means expensive entry and exit.

## DEX vs CEX

| | DEX | CEX |
|---|---|---|
| Asset custody | Your wallet | Exchange custody |
| KYC | Protocol layer usually no; some frontends restrict | Usually required |
| Listing barrier | Anyone can create pools | Exchange approval |
| Support | None | Customer support may exist |
| Liquidity | Good for major on-chain assets, poor for many small tokens | Often better for major assets |
| Best for | On-chain users and long-tail tokens | Beginners, fiat on/off ramps, large trades |

Chapter 14 compares them in more detail.

## Quick Memory Table

| Key Point | One-Sentence Version |
|---|---|
| DEX | On-chain exchange using smart contracts. |
| AMM | Formula-based pricing. |
| Liquidity pool | LPs deposit assets for traders to swap. |
| Impermanent loss | LPs may underperform simple holding after price divergence. |
| Slippage | Difference between expected and final trade price. |
| Fake tokens | Verify contract addresses, not names. |

## What to Read Next

- A Web3-native organization model: [13. DAOs](03-dao.md)
- CEX or DEX for trading: [14. CEX vs DEX](../05-trading-and-safety/01-cex-vs-dex.md)

---

> If you remember one sentence:
> **A DEX uses contracts to trade on-chain; AMMs price with formulas; LPs earn fees but face impermanent loss, slippage, MEV, and fake token risk.**
