# 06. Hot Wallets vs Cold Wallets

## One-Sentence Version

A hot wallet is connected to the internet and convenient but riskier. A cold wallet keeps signing keys offline and is safer but less convenient.

## What Makes a Wallet Hot or Cold?

The key question:

> **Can the private key or signing ability be exposed through an internet-connected device?**

- Private keys or signing ability available on a phone, computer, or browser extension -> **hot wallet**
- Private keys kept in an offline device or offline backup -> **cold wallet**

Internet-connected devices can be attacked through phishing sites, malicious extensions, clipboard malware, remote control tools, or unknown vulnerabilities. Hot wallets cannot reduce that risk to zero.

Cold wallets aim to keep private keys away from online environments. If the key never appears on an internet-connected computer, remote attackers have a much harder job.

## Hot Wallets: Convenient for Daily Use

### What They Are

Common hot wallets include:

- **Browser extension wallets**: MetaMask, Rabby, Phantom
- **Mobile wallets**: imToken, OKX Wallet, TokenPocket, Trust Wallet
- **Exchange app Web3 wallet entries**: some are self-custody wallets, some use MPC, and some are closer to custodial products. Always check who controls the key or recovery method.

Most self-custody hot wallets store encrypted keys on your phone or computer and use them to sign when needed. MPC wallets split signing ability into multiple parts, so their safety model is different.

### Advantages

- Free and easy to install.
- Smooth website connections and signing.
- Good for frequent activity: transfers, DeFi, airdrops, NFT minting.

### Risks

Hot wallet safety depends heavily on device and browser security. Common failure modes:

- Malicious browser extensions.
- Phishing signatures.
- Clipboard malware replacing addresses.
- Remote control malware reading wallet files or tricking signatures.

Principle: **only keep amounts in a hot wallet that you can tolerate losing**.

## Cold Wallets: Better for Long-Term Storage

### What They Are

Main types:

**1. Hardware wallets** (recommended for most users)

These are dedicated devices that protect private keys using a security chip or isolated signing environment. When you sign, the transaction data goes into the device. The device signs internally and returns only the signature. The private key does not appear on your computer.

Common brands:

- **Ledger**: mainstream hardware wallet brand from France
- **Trezor**: Czech brand with strong open-source focus
- **Keystone / OneKey**: teams with Chinese roots, known for QR-code signing options

**2. Paper wallets or offline devices**

You can store a seed phrase on paper and use a never-online device for signing. This can be secure in theory, but it is operationally difficult and not recommended for beginners.

### Advantages

- Malware on your computer cannot directly steal the private key.
- Suitable for large, long-term holdings.
- Reduces stress when browsing Web3 sites with a separate daily wallet.

### Disadvantages

- You need to buy a device.
- Signing is slower.
- The device can be lost or damaged, so you still need a seed phrase backup.
- You must buy from the official website or authorized sellers. Second-hand or unknown devices may be compromised.

## Exchange Accounts Are Not Wallets

Many beginners think: "My coins are on Binance or OKX. Is that a cold wallet?"

No. If assets are on an exchange, the on-chain private keys belong to the exchange, not you.

- Your balance is an entry in the exchange database.
- Your asset safety depends heavily on the exchange's operation, risk controls, and compliance situation.
- If the exchange fails, is hacked, or freezes withdrawals, you may not recover your funds.

Crypto has an old saying:

> **Not your keys, not your coins.**

Exchanges are useful for trading and fiat on/off ramps. They are not ideal for long-term storage.

## A Simple Storage Model

| Use | Where | Rough Share |
|---|---|---|
| Large, long-term, rarely moved | Hardware wallet | 70%+ |
| Daily use and DeFi | Hot wallet | 10%-20% |
| Trading | Centralized exchange | As needed |
| Testing new projects | Fresh hot wallet | Tiny amount |

The principle: **the more often a wallet interacts with unknown sites, the less value it should hold**.

## Hardware Wallet Questions

**"What if the hardware wallet breaks or is lost?"**  
Buy a new one and restore with the seed phrase. The device is replaceable. The seed phrase is not.

**"Can hardware wallets hold all chains?"**  
Mainstream hardware wallets support Bitcoin, Ethereum and many L2s, Solana, and other major chains. Check specific models for niche chains.

**"What should I do when it arrives?"**

1. Check packaging and signs of tampering.
2. Download companion software from the official website.
3. Generate the seed phrase yourself on the device. Never use a pre-printed seed phrase.
4. Test with a small transfer before moving large amounts.

**"Can the hardware wallet itself be my seed backup?"**  
No. The hardware wallet uses the seed to derive keys. You still need a separate paper or metal backup.

## Quick Memory Table

| | Hot Wallet | Cold Wallet |
|---|---|---|
| Key exposure | Internet-connected environment | Offline or isolated device |
| Main risk | Malware, phishing, bad signatures | Physical loss, bad backup |
| Best use | Daily activity | Long-term holdings |
| Convenience | High | Lower |
| Cost | Often free | Hardware cost |

## What to Read Next

- To understand wallet confirmations: [07. What Is Signing?](03-signing.md)
- To jump to assets: [08. Tokens, Coins, and Token Standards](../03-assets/01-tokens.md)

---

> If you remember one sentence:
> **Cold storage for large holdings, hot wallets for small daily use, and exchanges are not self-custody wallets.**
