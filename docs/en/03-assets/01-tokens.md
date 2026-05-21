# 08. Tokens, Coins, and Token Standards

## One-Sentence Version

A **coin** is the native currency of a blockchain. A **token** is an asset issued on top of a blockchain, usually through a smart contract.

Both are often called "tokens" casually, but their origins are different.

## Coin vs Token

| | Coin | Token |
|---|---|---|
| Issued by | The blockchain protocol itself | Anyone deploying a contract or using a token program |
| Examples | BTC, ETH, SOL, BNB | USDT, UNI, SHIB, PEPE |
| Main role | Pay gas, secure the chain, staking | Stablecoins, governance, points, memes, app assets |
| To create one | Build or use a blockchain | Deploy a contract or token program |

Analogy:

> A **coin** is like a country's native currency.  
> A **token** is like a gift card, membership card, or arcade token issued inside that country.

Ethereum is a chain. ETH is Ethereum's native coin. USDT, UNI, and meme tokens on Ethereum are tokens issued on Ethereum.

## What Is a Token Standard?

You may see terms such as **ERC-20**, **ERC-721**, **ERC-1155**, **SPL**, and **BRC-20**. These are token standards.

A token standard is an interface convention. It tells wallets, exchanges, and apps: "Tokens following this standard behave in these expected ways."

Common examples:

| Standard | Where | Used For |
|---|---|---|
| **ERC-20** | Ethereum and EVM chains | Fungible tokens such as USDT and UNI |
| **ERC-721** | Ethereum and EVM chains | Non-fungible tokens, or NFTs |
| **ERC-1155** | Ethereum and EVM chains | Both fungible and non-fungible assets, common in games |
| **SPL** | Solana | Solana token standard |
| **BRC-20** | Bitcoin ecosystem | Experimental token structure on Bitcoin |

Beginner shortcut: **an ERC-20 token is usually a fungible token on Ethereum or an EVM-compatible chain.**

## Fungible vs Non-Fungible

- **Fungible**: each unit is interchangeable. 1 USDT is the same as another 1 USDT.
- **Non-fungible**: each item is unique. NFT #1 and NFT #2 are different objects.

ERC-20 is fungible. ERC-721 is non-fungible. ERC-721 assets are what people usually call NFTs.

## Common Beginner Trap: Same Name, Different Chain

Anyone can issue a token on-chain. This creates a major beginner trap:

> **The same token name on different chains may refer to different assets or different versions of an asset.**

Example: USDT exists on many networks:

- USDT on Ethereum (ERC-20)
- USDT on Tron (TRC-20)
- USDT on BNB Chain (BEP-20)
- USDT on Solana (SPL)

They all represent USDT issued by Tether and attempt to track 1 dollar, but they live on different networks.

If you withdraw from an exchange on the wrong network, several things can happen:

- The exchange blocks the withdrawal because the address format is incompatible.
- The asset arrives on a network the recipient does not support, making recovery difficult.
- The recipient address is not yours, making recovery almost impossible.

So do not only ask "Is this USDT?" Ask: **USDT on which network?**

Even worse, scammers can issue fake tokens with the same name.

For example:

> Real Ethereum USDT contract: `0xdAC17F958D2ee523a2206206994597C13D831ec7`  
> A scammer can issue a token also named USDT with a completely different contract address.

Wallets may show token names by default. Names are not enough. Contract addresses matter.

Safety habits:

1. **Check the network when withdrawing or bridging.**
2. **Check the contract address**, not just the name. Use official websites, CoinGecko, or CoinMarketCap.
3. **Ignore unknown tokens that appear in your wallet.**

## "A Weird Token Appeared in My Wallet. Can I Touch It?"

Usually, no.

Scammers often send dust tokens or scam airdrops with names such as `Visit website to claim` or `Reward 1000 USDT`.

Common tricks:

1. **Phishing website**: the token name tells you to visit a scam site.
2. **Fake swap or approval**: you try to sell it, but the signature approves real assets to an attacker.
3. **Wallet tracking**: interacting with it helps link multiple wallets.

Correct response: **treat it as invisible**. Hide it in your wallet if possible. Do not sell, transfer, approve, or investigate out of curiosity.

## Token Types by Use

| Type | Purpose | Examples |
|---|---|---|
| **Stablecoins** | Track fiat prices and act as trading medium | USDT, USDC, DAI |
| **Governance tokens** | Voting rights in protocols | UNI, AAVE |
| **Exchange or platform tokens** | Ecosystem utility, fees, membership | BNB, OKB |
| **Meme coins** | Community culture and speculation | DOGE, SHIB, PEPE |
| **GameFi/SocialFi tokens** | Points or currency for apps | Various |
| **RWA tokens** | Tokenized real-world assets | PAXG, tokenized Treasuries |

The key question is: **where does the token's value come from?** Stablecoins depend on reserves or mechanisms. Governance tokens depend on protocol value and voting power. Meme coins depend mostly on attention and emotion.

## Quick Memory Table

| Concept | One-Sentence Version |
|---|---|
| Coin | Native asset of a chain, used for gas and security. |
| Token | Asset issued on a chain by a contract or token program. |
| ERC-20 | Fungible token standard on Ethereum/EVM. |
| Same name, different chain | Always verify network and contract. |
| Unknown wallet token | Ignore it. Do not interact. |

## What to Read Next

- The most-used token category: [09. Stablecoins](02-stablecoins.md)
- Non-fungible assets: [10. NFTs](03-nft.md)

---

> If you remember one sentence:
> **Coins come from chains; tokens come from contracts or token programs. Always verify token, network, and address together.**
