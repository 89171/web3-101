# 09. Stablecoins

## One-Sentence Version

Stablecoins are tokens that **try to stay near 1 dollar**. They are a bridge between crypto markets and the real world.

## Why Stablecoins Exist

Cryptocurrencies are volatile. BTC or ETH can move 10% in a day. That is hard for daily payments or accounting.

Stablecoins provide a relatively stable unit inside crypto. Most track the US dollar, though some track other currencies or assets.

They are used as:

- **Trading medium**: many DEX pairs are token/stablecoin pairs.
- **Risk-off asset**: traders move into stablecoins during volatility.
- **Cross-border payment rail**: stablecoin transfers can be faster and cheaper than traditional rails in some contexts.
- **DeFi fuel**: lending, market making, and yield strategies often use stablecoins.

## How Do They Stay Stable?

There are several models.

### 1. Fiat-Backed Stablecoins

The issuer holds reserves, such as dollars, Treasury bills, or cash-like assets, and issues tokens on-chain.

Examples:

- **USDT** by Tether: largest and oldest, also controversial.
- **USDC** by Circle: more compliance-oriented and transparent.
- **PYUSD** by PayPal.

Their stability depends on trust in the issuer:

- Are the reserves real?
- Are they liquid?
- Can the issuer redeem them?
- Will the issuer stay solvent and compliant?

USDT has often been criticized for reserve transparency, but it has not experienced a UST-style collapse. USDC publishes regular reserve attestations and is generally considered more transparent. Both are widely used and stable most of the time.

### 2. Crypto-Collateralized Stablecoins

These are backed by overcollateralized crypto assets.

Example: to mint 100 DAI, you may need to deposit 150 dollars' worth of ETH or other collateral. If collateral value falls too low, the system liquidates it to repay debt.

Examples:

- **DAI** in the MakerDAO / Sky ecosystem
- **LUSD**
- **crvUSD**

Their stability relies on collateral value and liquidation mechanisms. They reduce reliance on a single issuer, but capital efficiency is lower because users must overcollateralize.

Important: many "decentralized" stablecoins today are not backed only by ETH. They may include USDC, tokenized Treasuries, or other real-world asset exposure. They can be more on-chain than USDT/USDC, but not necessarily free from centralization risk.

### 3. Algorithmic Stablecoins

These attempt to hold a peg through market incentives and mint/burn algorithms without sufficient collateral.

Famous failure:

- **UST** by Terra collapsed in May 2022, falling from 1 dollar toward near zero and wiping out tens of billions of dollars in value.

Lesson: **pure algorithmic stablecoins are extremely risky**. If a stablecoin claims to be uncollateralized and stable by algorithm alone, be very careful.

## Depeg Risk

Stablecoins can depeg, meaning they trade away from their target price.

Major examples:

- **UST in May 2022**: collapsed and never recovered.
- **USDC in March 2023**: fell to around 0.87 dollars after part of its reserves were exposed to Silicon Valley Bank; it recovered after regulators intervened.
- **USDT** has had several smaller temporary depegs and recovered.

Lessons:

1. **Stablecoins are not risk-free.**
2. Risk comes from issuer, collateral, mechanism, and market confidence.
3. Do not keep all assets in a single stablecoin.

## On-Chain Token, Off-Chain Promise

Fiat-backed stablecoins have two sides:

- **On-chain**: USDT or USDC is a token that wallets can receive and transfer.
- **Off-chain**: redemption value depends on the issuer's reserves, banking relationships, and compliance status.

They are Web3 assets, but also centralized promises. Issuers such as Tether and Circle can freeze addresses in their contracts and have done so for law enforcement reasons.

If you want to reduce single-issuer risk, study DAI, LUSD, and other crypto-collateralized options. If you need maximum liquidity and acceptance, USDT and USDC are usually the main choices. There is no perfect stablecoin, only tradeoffs.

## Practical Suggestions

1. **For daily use, USDT and USDC are the most accepted.**
2. **For larger holdings, diversify issuer risk** instead of holding one stablecoin only.
3. **If you care about decentralization, study the collateral and governance structure** of DAI, LUSD, and similar assets.
4. **Avoid pure algorithmic stablecoins**, especially new "next-generation" versions.
5. **Check the network before transferring.** USDT on Ethereum, Tron, Solana, and other networks is not the same networked asset.
6. **Tron USDT is common for small transfers, but not always free.** TRC-20 USDT consumes energy and can burn TRX if you have no energy.

## USDT vs USDC

| | USDT | USDC |
|---|---|---|
| Issuer | Tether | Circle |
| Transparency | Quarterly reserve reports/attestations, still debated | Monthly third-party attestations, generally more transparent |
| Acceptance | Very broad globally, especially Asia and emerging markets | Stronger in US compliance and institutional contexts |
| Transfers | Very common on Tron and many chains; fee depends on network resources | Native on multiple chains; common in compliance-heavy contexts |
| Regulatory risk | Higher | Lower |
| Depeg history | Several small depegs, recovered | One major SVB-related depeg, recovered |

Simple conclusion: use what is convenient for your case. For large long-term holdings, many users split between USDT and USDC to reduce single-issuer risk.

## Quick Memory Table

| Concept | One-Sentence Version |
|---|---|
| Stablecoin | Token that tries to stay near 1 dollar. |
| USDT / USDC | Fiat-backed; depend on issuer reserves. |
| DAI / LUSD | Crypto-collateralized; depend on collateral and liquidations. |
| Algorithmic stablecoin | High risk; pure algorithmic designs have largely failed. |
| Depeg | Price moves away from the target; stable does not mean risk-free. |

## What to Read Next

- A very different type of asset: [10. NFTs](03-nft.md)
- Where stablecoins are often used: [11. What Is DeFi?](../04-applications/01-defi.md)

---

> If you remember one sentence:
> **Stablecoins are crypto's dollar-like assets, but they are not risk-free. Issuer, collateral, mechanism, and network all matter.**
