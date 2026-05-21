# 07. What Is Signing?

## One-Sentence Version

Signing means using your private key to **stamp approval on a piece of data**. Many thefts happen because users are tricked into stamping the wrong thing.

## Every "Confirm" Is a Signature

In Web2:

> You log in with a username and password -> click buttons -> the server records what you did.

The server is the referee.

In Web3, the chain does not know who you are. It only checks signatures:

> You want to do something -> your wallet signs the action with your private key -> the signature is sent with the action -> the chain verifies that the signature matches your address -> the action is accepted.

Transfers, approvals, swaps, minting, voting, and many logins involve signatures.

That is why your first line of defense is: **read what you are signing**.

## Two Major Types of Signatures

### 1. Transaction Signatures

These go on-chain, cost gas, and change blockchain state.

Examples:

- Send 100 USDT to another address.
- Swap 1 ETH for USDC.
- Mint an NFT or vote on-chain.

Characteristics:

- They show gas fees.
- They leave an on-chain record.
- The action may still be complex and hard to read.

### 2. Message Signatures

These do not go on-chain by themselves and do not cost gas. They prove that your address signed some message.

Examples:

- Sign in with Ethereum.
- Submit a signature to an off-chain system.
- Authorize another party to act with your assets in certain ways.

Characteristics:

- They feel harmless because they do not cost gas.
- They may still be used by contracts or off-chain systems to do serious things.
- Wallets may show confusing text or raw data.

Many thefts involve message signatures because users do not feel the same caution as they do with gas-paying transactions.

## Signature Types to Watch Carefully

### `approve` / `setApprovalForAll`

Approval signatures let a contract move your tokens.

Normal use: before swapping USDC on Uniswap, you approve the Uniswap contract to spend your USDC.

Risks:

- An unlimited approval lets the contract move that token later.
- A phishing site can trick you into approving an attacker contract.
- `setApprovalForAll` can allow someone to move an entire NFT collection.

Defenses:

- Check the spender address.
- Avoid unlimited approvals when possible.
- Regularly review and revoke unused approvals with tools such as [revoke.cash](https://revoke.cash/) after verifying the current official domain.

### `permit` / `permit2`

These are off-chain approvals. One signature, with no gas cost, can grant spending permission.

Risk: because no gas is paid and nothing appears on-chain immediately, users treat it casually. A fake airdrop can ask you to sign a "free verification" that is actually permission to move your stablecoins.

Defense: good wallets try to parse permit signatures into readable text such as "approve X USDC to address Y." Check amount and spender. If the wallet cannot parse it and you cannot understand it, do not sign.

### Blind Signing

Blind signing means the wallet cannot explain what you are signing and only shows raw data.

Risk: you do not know what you are approving.

Defense: unless you fully trust the source and understand why blind signing is needed, do not blind sign. Legitimate apps should usually make wallet prompts readable.

## A Typical Scam Flow

1. You see "Project X airdrop, claim now" on social media.
2. You open the site and connect your wallet.
3. The site says "sign to verify identity." No gas is required, so it feels safe.
4. You sign.
5. Your USDC or USDT disappears.

What happened? The "verification" was a `permit` signature authorizing the attacker to move your stablecoins. They submitted the signature on-chain and drained the assets.

On-chain, it looks valid because your address signed the authorization.

## Signature Safety Checklist

Before signing, ask:

1. **How did I reach this site?** Links from comments, DMs, and random chat messages are risky.
2. **Is the domain correct?** Phishing domains often swap similar letters.
3. **What does the wallet show?** Modern wallets like Rabby often highlight dangerous signatures.
4. **Is this a transaction or a message signature?** Message signatures deserve extra caution.
5. **Do the amount and counterparty match?** Check token, amount, and address.
6. **Unsure? Close it.** Missing an airdrop is better than losing a wallet.

## A Useful Habit

When a wallet popup appears, pause for 5 seconds. Web2 trained people to click "OK" quickly. In Web3, that habit is dangerous.

## Quick Memory Table

| Type | On-Chain? | Gas? | Risk |
|---|---|---|---|
| Transfer | Yes | Yes | Medium |
| `approve` / `setApprovalForAll` | Yes | Yes | High |
| `permit` / `permit2` | No by itself | No | Very high |
| Normal login message | No | No | Low to medium |
| Blind signing | Maybe | Maybe | Avoid |

## What to Read Next

Part 2 ends here. Next we look at on-chain assets.

-> [08. Tokens, Coins, and Token Standards](../03-assets/01-tokens.md)

---

> If you remember one sentence:
> **Every Web3 "Confirm" is a private-key stamp. Gas-free signatures can be the most dangerous, so pause before signing.**
