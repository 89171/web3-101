# 14. Centralized Exchanges vs Decentralized Exchanges

## One-Sentence Version

A CEX is a **company-run exchange**. A DEX is an **on-chain trading contract or protocol**. They are not enemies; they solve different problems.

## The Core Difference

Remember this:

> **On a CEX, your assets are entries in the exchange's internal ledger.**  
> **On a DEX, your assets remain in your own wallet until a contract moves them.**

This difference affects custody, support, freezing risk, fiat access, trading speed, and responsibility.

## Detailed Comparison

| Dimension | CEX | DEX |
|---|---|---|
| **Custody** | Exchange custody | Your wallet |
| **Fiat on/off ramp** | Usually supported | Usually not supported |
| **KYC** | Usually required | Protocol layer usually not; some frontends restrict regions or addresses |
| **Liquidity** | Strong for major assets | Strong for major on-chain assets and long-tail tokens vary |
| **New listings** | Exchange approval | Anyone can create a pool |
| **Fees** | Often around 0.1% | Swap fee plus gas |
| **Speed** | Instant internal matching | Wait for chain confirmation |
| **Support** | Customer support may exist | No support desk |
| **Freezing risk** | Exchange or regulator can freeze account | Wallet address cannot be reset by a platform, but frontends, RPCs, and certain token contracts can restrict or freeze |
| **Advanced orders** | Limit, stop-loss, grid, etc. | Often limited, though some DEXs support more |
| **Leverage** | Common | Some DEXs support it |
| **Main risk** | Exchange failure, hacks, regulation | Contract bugs, phishing, user mistakes |

## CEX Examples

Common global exchanges include:

- **Binance**
- **Coinbase**
- **OKX**
- **Bybit**
- **Kraken**
- **Bitget**
- **Gate.io**

Availability depends on your country. For beginners, key questions are: can you legally use it, can you deposit/withdraw fiat, and can you get support in your language?

## DEX Examples

- **Ethereum and multichain**: Uniswap, SushiSwap, Curve
- **BNB Chain**: PancakeSwap
- **Solana**: Jupiter, Raydium, Orca
- **Aggregators**: 1inch, Matcha, Jupiter

## When to Use CEX vs DEX

### CEX Is Usually Better For

1. **First purchase**: most people buy crypto through fiat on a CEX.
2. **Fiat withdrawal**: turning crypto back into local currency.
3. **Large trades in major assets**: CEXs often have deeper liquidity.
4. **Advanced order types**: limit, stop-loss, grid, derivatives.
5. **Users who do not want self-custody**: this can be rational if self-custody risk feels higher than exchange risk.

### DEX Is Usually Better For

1. **Long-tail tokens** that are not listed on CEXs.
2. **Less KYC at protocol level**, though frontends may still restrict access.
3. **On-chain activity** such as DeFi, NFTs, airdrops.
4. **Self-custody**: assets stay in your wallet.
5. **Global protocol access**, subject to frontend and legal constraints.

### A Practical Combination

| Use | Suggested Path |
|---|---|
| Fiat -> buy major assets | CEX |
| Long-term large holdings | Withdraw from CEX to your own hardware wallet |
| Daily small trades | Small wallet balance + DEX |
| DeFi / NFT / airdrop | Wallet + on-chain apps |
| Cash out | Send to CEX -> withdraw fiat |

The important step is moving long-term assets out of the CEX if you choose self-custody. FTX and Mt.Gox showed why exchange custody has real risk.

> **Not your keys, not your coins.**

## Real CEX Risks

### 1. Exchange Failure or Fraud

Examples:

- **Mt.Gox (2014)**: once the largest Bitcoin exchange, collapsed after massive losses.
- **FTX (2022)**: once a top exchange, collapsed after misuse of customer funds.
- Smaller exchanges have also run away, halted withdrawals, or failed.

### 2. Regulatory Risk

- A country changes rules and the exchange stops serving your region.
- A sanctioned address causes accounts or withdrawals to be reviewed.
- Local legal status may be unclear.

### 3. Account Risk Controls

Exchanges can freeze accounts due to:

- Suspicious login or withdrawal.
- Links to risky addresses.
- Compliance requests.

Resolution depends on the exchange and regulators.

### 4. Withdrawal Delays

"Network congestion," "maintenance," and compliance reviews can delay withdrawals.

Conclusion: **CEXs are useful for trading and fiat access, but not ideal for long-term custody.**

## Real DEX Risks

DEXs are not automatically safe. Their risks are different:

1. **Smart contract bugs**: see [DeFi chapter](../04-applications/01-defi.md).
2. **Phishing sites**: fake Uniswap or PancakeSwap clones.
3. **Slippage / MEV / sandwich attacks**: see [DEX chapter](../04-applications/02-dex.md).
4. **Fake tokens and fake pools**: verify contract addresses.
5. **Wrong signatures**: see [Signing chapter](../02-wallets/03-signing.md).

Also remember: some tokens themselves are centralized contracts. Stablecoin issuers may freeze addresses. Frontends may block regions or addresses.

Simple summary:

> **CEX risk is concentrated in the exchange. DEX risk is spread across every signature, contract, token, and frontend.**

## Decision Tree

```text
What do you want to do?
+-- First purchase or fiat deposit
|   +-- Use a CEX
+-- Long-term large holdings
|   +-- Withdraw to your own hardware wallet
+-- DeFi / NFT / airdrop
|   +-- Use wallet + on-chain apps
+-- Token not listed on a CEX
|   +-- Use a DEX, but check fake tokens and slippage
+-- Limit orders or derivatives
|   +-- Usually use a CEX or specialized platform
+-- Convert crypto to cash
    +-- Send to CEX and withdraw fiat
```

## Quick Memory Table

| Key Point | One-Sentence Version |
|---|---|
| CEX | Company-run exchange, custody held by exchange. |
| DEX | On-chain trading, custody starts in your wallet. |
| Fiat access | Usually CEX. |
| Long-term custody | Use your own wallet if you choose self-custody. |
| On-chain activity | Requires wallet and on-chain apps. |
| Relationship | Not either-or; use each for what it is good at. |

## What to Read Next

Final chapter: the most important scam patterns.

-> [15. Common Scams and How to Avoid Them](02-common-scams.md)

---

> If you remember one sentence:
> **Use CEXs for trading and fiat rails, DEXs for on-chain activity, and hold long-term assets with keys you control if you choose self-custody.**
