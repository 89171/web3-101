# 05. Wallets, Addresses, Private Keys, and Seed Phrases

## One-Sentence Version

A wallet is a **key manager**. An address is like a **public safe number**. A private key is the **key itself**. A seed phrase is the **master recovery key** for a wallet.

> **This is one of the most important chapters in the handbook.**  
> Most Web3 asset losses happen because people misunderstand keys, seed phrases, or signatures.

> Here, I recommend [BloFin Wallet](https://wallet.blofin.com/app)￼. It supports both private keys and seed phrases, and offers features such as asset management, Swap/Bridge, on-chain access, earning, payments, and cards. It also has a built-in Polymarket module — my favorite prediction market — and is backed by the BloFin exchange, making it more secure.

## It Is Not the Same as a Web2 Username and Password

A common beginner mistake is thinking: "A wallet is my Web3 account, and the private key is my password."

That is wrong.

| | Web2 Username/Password | Web3 Wallet |
|---|---|---|
| Who creates it? | A server when you register | You generate it locally |
| Who stores it? | The platform | You |
| Forgot it? | Click "forgot password" | No one can recover it for you |
| Leaked? | Change password | Assets may be lost immediately |
| Who can ban it? | The platform | No platform can reset your private key |

Important: **a Web3 wallet has no password reset button. Customer support cannot reset your private key. If you lose your key, the assets controlled by that key may be lost forever.**

This is the cost of self-custody. If no one can seize your assets, no one can recover them for you either.

## How These Four Terms Fit Together

Analogy:

> You have a safe. The **address** is the safe number, and anyone can send things to it.  
> The **private key** is the key that opens the safe.  
> The **seed phrase** is the master recovery blueprint that can recreate the key.  
> The **wallet app** is the keychain that helps you manage keys and interact with blockchains.

### Address

An address is a public string, for example:

```text
0x742d35Cc6634C0532925a3b844Bc9e7595f0bEb7
```

It is safe to share your address. People need it to send you assets.

Common address formats:

- Ethereum-style chains (EVM chains and many L2s): start with `0x`
- Bitcoin: often starts with `1`, `3`, or `bc1`
- Solana: a base58 string without `0x`
- Tron: starts with `T`

Important: when transferring, always check **asset + network + recipient address** together.

- The same `0x` address can exist on Ethereum, Base, Arbitrum, BNB Chain, and other EVM networks. Assets still live on the specific network where they were sent.
- If you withdraw from an exchange on the wrong network, recovery may be difficult or impossible, especially if the recipient is an exchange or someone else's address.
- Wallets and exchanges often block incompatible address formats, but you should not rely on that as your safety strategy.

### Private Key

A private key is a long secret string, for example:

```text
0x4c0883a69102937d6231471b5dbb6204fe5129617082792ae468d01a3f362318
```

It controls the assets at an address. Whoever has the private key can act as the owner of that address.

> **Anyone or any website asking for your private key is almost certainly trying to steal from you.**  
> Customer support, airdrops, account unlocks, and verification forms do not need your private key.

### Seed Phrase

A seed phrase is usually 12 or 24 English words:

```text
witch collapse practice feed shame open despair creek road again ice least
```

A seed phrase is more accurately a wallet's **master recovery key**. It can derive private keys for many addresses. It is easier to write down than a raw private key, but it is just as dangerous if leaked.

So: **seed phrase = master key for the wallet = access to your assets**.

### Wallet App

Wallet apps such as MetaMask, Rabby, Phantom, imToken, OKX Wallet, and Trust Wallet help you:

1. Generate seed phrases and private keys.
2. Store keys encrypted on your device, or manage another signing model such as MPC.
3. Send transactions and sign messages.
4. View balances and interact with apps.

The wallet app **does not store your assets**. Assets are on-chain. The wallet manages the keys that can move them.

- Deleting MetaMask does not delete your assets. If you have the seed phrase, you can restore the wallet.
- A polished wallet UI cannot protect you from leaking the seed phrase or signing a malicious transaction. Choose trusted wallets, keep devices clean, and read every signature prompt.

## One Seed Phrase, Many Chains

Many people think: "I created an Ethereum wallet in MetaMask, so it only controls Ethereum."

Not exactly.

> **One seed phrase can usually generate addresses across many mainstream chains.**

The same seed phrase may generate an Ethereum address in MetaMask, a Solana address in Phantom, and a Bitcoin address in a Bitcoin wallet.

There is one detail: different wallets may use different **derivation paths**, so importing the same seed phrase into different apps may not always show the same address. When recovering, use the original wallet app or confirm the derivation path if the address looks different.

This means:

1. **Convenience**: one seed phrase can often recover many addresses.
2. **Risk**: if that seed phrase leaks, all addresses derived from it may be compromised.

## How to Store a Seed Phrase

### Do

1. **Write it on paper**, preferably with ink that does not fade.
2. **Store physical copies** in safe places, such as a safe, a secure drawer, or separate trusted locations.
3. **Verify it during wallet setup** if the wallet asks you to re-enter words.
4. **Consider a metal backup** for larger holdings, because it is more fire and water resistant.

### Do Not

1. **Do not take screenshots.** Cloud photo backups get hacked.
2. **Do not store it in notes apps, email, or cloud drives.**
3. **Do not send it to anyone**, including friends, family, or support staff.
4. **Do not enter it into websites**, except when restoring inside a trusted wallet app.
5. **Do not share your screen while the seed phrase is visible.**

### A Commonly Ignored Risk: Life Events

If something happens to you and your family has no idea where your seed phrase is, the assets may be lost forever. Blockchains do not know inheritance law.

If you hold meaningful value, consider writing a digital asset instruction letter for trusted family members or legal representatives. Keep it secure, but make sure someone knows that an entry point exists.

## One Wallet or Multiple Wallets?

Best practice: **separate wallets by purpose**.

| Wallet | Purpose | Amount |
|---|---|---|
| **Vault wallet** | Long-term holdings | Large amounts, ideally hardware wallet |
| **Daily wallet** | Transfers, DeFi, normal use | Small usable amount |
| **Test wallet** | New projects, airdrops, unknown links | Tiny amount |

Every link you click and every signature you approve carries some risk. Keeping everything in one active wallet is like carrying all your savings in your pocket.

## What If Something Goes Wrong?

| Situation | What to Do |
|---|---|
| Phone lost, seed phrase safe | Install the wallet on a new device and restore. |
| Wallet app deleted, seed phrase safe | Reinstall and restore. |
| Seed phrase lost, wallet still logged in | Immediately move assets to a new wallet whose seed phrase you have backed up. |
| Seed phrase lost, app deleted | Assets are likely permanently lost. |
| Seed phrase exposed | Assume compromise. Move all assets to a new wallet immediately. |

## Quick Memory Table

| Concept | One-Sentence Version | Public or Private |
|---|---|---|
| Address | Public receiving identifier | **Public** |
| Private key | The key that controls assets | **Secret** |
| Seed phrase | Master recovery key that derives private keys | **Secret** |
| Wallet app | Tool for managing keys and signing | App is public; keys are secret |

## What to Read Next

- To store larger assets more safely: [06. Hot Wallets vs Cold Wallets](02-hot-vs-cold.md)
- To understand what "Confirm" actually does: [07. What Is Signing?](03-signing.md)

---

> If you remember one sentence:
> **Whoever controls the seed phrase controls the assets. If the seed phrase leaks, no one can reliably save you.**
