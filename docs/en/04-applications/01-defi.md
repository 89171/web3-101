# 11. What Is DeFi?

## One-Sentence Version

DeFi means **decentralized finance**. It rebuilds parts of banking, trading, lending, and asset management with smart contracts. Core rules run on-chain, but teams, frontends, governance, and regulation still matter.

## How It Differs From Banks

Traditional finance depends on centralized institutions:

- Save money for interest -> bank
- Borrow money -> bank
- Exchange currencies -> bank or broker
- Buy stocks -> broker
- Buy insurance -> insurer

These institutions mainly perform rule-based accounting and risk management.

DeFi asks:

> **If financial rules can be written clearly, why not put them into code on a blockchain and let the code execute them?**

That code is a **smart contract**: a program deployed on-chain that anyone can call. Ideally, the protocol layer does not care who you are. In practice, frontends, oracles, governance multisigs, and regulations can still affect access and outcomes.

| | Traditional Finance | DeFi |
|---|---|---|
| Rule execution | Institutions and IT systems | Smart contracts |
| Identity checks | KYC, credit checks, risk teams | Protocol layer usually does not check identity; frontends may restrict access |
| Hours | Business hours | 24/7 |
| Cross-border | Complex | The chain itself is global |
| When things go wrong | Support, regulators, courts | Usually little direct help |

## Example: DeFi Lending vs Bank Lending

### Borrowing from a Bank

1. Submit ID, income proof, credit report, and other documents.
2. Wait for approval.
3. The bank decides whether you can borrow and at what rate.
4. You sign a contract.
5. You repay on schedule; missed payments affect credit.

The bank needs to know who you are and whether you can repay.

### Borrowing on Aave

1. Open Aave and connect a wallet.
2. Deposit collateral, such as ETH.
3. Borrow USDC.
4. Repay when you want.
5. If collateral value falls too far, the protocol liquidates collateral automatically.

The protocol does not care who you are. It cares whether your collateral is enough.

This is why DeFi lending is usually **overcollateralized**. You may need to deposit 120%-200% or more in value to borrow 100%, depending on asset volatility and protocol parameters.

It sounds strange: why borrow if you already have assets? Many users do not want to sell ETH or other assets, but need stablecoins temporarily.

## Main DeFi Categories

### 1. DEXs

Decentralized exchanges let users swap tokens on-chain.

Examples: **Uniswap**, **Curve**, **Jupiter**.

The next chapter explains how DEXs and AMMs work: [12. DEXs and AMMs](02-dex.md).

### 2. Lending Protocols

Users deposit assets to earn interest or borrow against collateral.

Examples: **Aave**, **Compound**, **Spark**.

Where does interest come from? Borrowers. Rates are usually determined by supply and demand. If many people want to borrow, deposit rates rise. If few borrow, deposit rates fall.

### 3. Yield Farming

Users provide assets to protocols, often as liquidity, and receive fees or reward tokens.

High APY can be tempting: 10%, 50%, or even hundreds of percent. Be careful:

- Higher APY usually means higher risk.
- Rewards often come from newly issued project tokens that can collapse in price.
- Principal is not guaranteed. Risks include impermanent loss and protocol hacks.

### 4. Derivatives

On-chain perpetuals, futures-like contracts, and options.

Examples: **dYdX**, **GMX**, **Hyperliquid**.

Beginners should be very cautious. Leverage trading is already dangerous on centralized exchanges, and on-chain versions are not easier.

### 5. Stablecoin Issuance

Some DeFi protocols issue stablecoins.

Examples: **MakerDAO / Sky** for the DAI / USDS system, **Liquity** for LUSD.

### 6. Staking and Restaking

Users stake ETH to help secure Ethereum and earn rewards, or restake staking positions into other protocols for additional rewards.

Examples: **Lido** for liquid staking, **EigenLayer** for restaking.

## Real DeFi Risks

DeFi removes some intermediaries, but it also moves responsibility to users.

### 1. Smart Contract Risk

Code can have bugs. A bug can drain an entire protocol.

Defense: prefer older, well-known, audited protocols with long operating history, visible TVL, and clear risk disclosures. Audits help but do not guarantee safety.

### 2. Economic Design Risk

The code may work as written, but the economic model may fail under stress.

Example: UST did not collapse mainly because of a simple code bug. Its economic design failed under a bank-run-like scenario.

### 3. Oracle Risk

Lending protocols need prices. They usually rely on oracles such as Chainlink. If an oracle is attacked or fails, liquidations and arbitrage can break.

### 4. Governance and Centralization Risk

Some "decentralized" protocols still have powerful teams, admin keys, upgrade controls, or concentrated governance tokens.

### 5. Regulatory Risk

Regulators increasingly pay attention to DeFi. Some projects face enforcement actions, and some frontends may add KYC or region blocking.

### 6. User Error

Wrong signature, wrong chain, phishing site, forgotten approvals. In DeFi, operational responsibility is mostly yours.

## Beginner-Friendly DeFi Path

If you want to try DeFi, start with tiny amounts:

1. Put a small amount of ETH on an L2 such as Base or Arbitrum.
2. Make a simple ETH <-> USDC swap on Uniswap.
3. Deposit a small amount of USDC into Aave to see how lending works.
4. Withdraw when finished.

Do not chase high APY or new protocols first. Understand the mechanism before increasing size.

## Quick Memory Table

| Key Point | One-Sentence Version |
|---|---|
| DeFi | Financial services rebuilt with smart contracts. |
| Biggest difference | Protocol rules are in code; identity often matters less at protocol layer. |
| Why overcollateralized? | Protocols cannot rely on your credit history. |
| High APY | Usually high risk. |
| Main risks | Contract bugs, economic design, oracles, governance, regulation, user error. |
| Beginner path | L2, tiny amounts, mature protocols. |

## What to Read Next

- How DEXs price trades: [12. DEXs and AMMs](02-dex.md)
- What DAOs are: [13. DAOs](03-dao.md)

---

> If you remember one sentence:
> **DeFi replaces some financial intermediaries with code, but it does not remove risk. It often transfers risk to you.**
