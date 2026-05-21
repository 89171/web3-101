# 10. NFTs

## One-Sentence Version

An NFT is a **unique on-chain certificate**. It is not usually the image itself. It proves that a certain token ID belongs to a certain address.

## Correcting the Biggest Misunderstanding

Many people think: "NFT = the monkey picture."

More accurately:

> **An NFT is an on-chain record saying that item X is currently owned by address Y.**

The image is usually not stored fully on-chain. It is often stored on a server or IPFS, while the NFT stores a pointer to metadata.

When you buy an NFT, you usually receive:

1. The on-chain record that a token ID belongs to your address.
2. Metadata such as image, video, or description, often stored off-chain.
3. Any project-specific rights, such as community access or commercial licensing, depending on the project's terms.

You usually do **not** automatically receive:

- Copyright to the image, unless explicitly granted.
- The ability to stop others from right-click-saving the image.

Analogy:

> Buying an NFT is like buying a certificate of ownership. Others can take photos of the artwork, but the ownership record still points to you.

## NFT vs Fungible Token

| | Fungible Token (ERC-20) | Non-Fungible Token (ERC-721) |
|---|---|---|
| Analogy | Money | Property deed or concert ticket |
| Each unit | Interchangeable | Unique |
| Fractional? | Yes, 0.5 token is possible | Standard NFTs are whole items unless wrapped or fractionalized |
| Identified by | Balance amount | Token ID |
| Examples | USDT, ETH | CryptoPunks #1234, a ticket NFT |

NFTs are useful when **this specific thing is different from all other things**.

## Common NFT Use Cases

### 1. Digital Art and Collectibles

The first NFT boom was mostly avatars and digital art.

Examples: CryptoPunks, Bored Ape Yacht Club, Art Blocks.

Notes:

- Prices are highly volatile.
- Value depends on community, brand, and culture more than technology.
- Most projects do not survive long cycles.

### 2. Domains and Identity

NFTs can map human-readable names to addresses.

Examples:

- **ENS**: `.eth` names, such as `vitalik.eth`
- **SNS**: `.sol` names on Solana
- **Unstoppable Domains**

Use: instead of pasting a long address, send to `alice.eth`.

### 3. Credentials and Memberships

NFTs can prove participation or membership:

- Early supporter badges.
- POAPs for event attendance.
- Community access passes.

Some are non-transferable, often called soulbound tokens. Their purpose is identity, not trading.

### 4. Game Items

Game items such as equipment, skins, or land can be represented as NFTs.

Ideal: players truly own items, can sell them, and maybe use them across games.  
Reality: most blockchain games have struggled with user experience and sustainability.

### 5. Real-World Asset Certificates

NFTs can represent ownership proofs for real-world assets such as real estate, luxury goods, or collectibles. This is still early because legal systems must recognize the connection between on-chain records and real-world rights.

## How to Evaluate an NFT Project

This is not investment advice, but these questions help reduce obvious mistakes:

1. **Who is the team?** Anonymous teams can disappear more easily.
2. **What does it do beyond being an image?**
3. **What rights or utility does holding it provide?**
4. **How liquid is it?** Check floor price and actual trading volume.
5. **What is the price history?** Many NFTs are down 90%+ from highs.

Better mindset:

> **Treat NFTs as hobby spending, not guaranteed investments.**

If you buy because you like the art or want to support the creator, fine. If you buy only because you expect resale profits, be ready to lose everything.

## NFT Safety Risks

NFT users are frequent phishing targets because minting is exciting, links spread fast, and signatures are confusing.

Common traps:

1. **Fake mint sites**: a project uses `a.com`; scammers create `a-mint.com`.
2. **"Free NFT" spam**: a wallet receives an NFT titled "click to claim." Do not touch it.
3. **`setApprovalForAll` phishing**: one approval lets an attacker move all NFTs from that collection.
4. **OTC phishing**: a stranger DMs you with a fake marketplace link.

Defenses:

- Enter mint links only from official websites or verified official social posts.
- Do not click, approve, transfer, or sell unknown NFTs in your wallet.
- Revoke unused NFT approvals using trusted tools after verifying the domain.
- Store expensive NFTs in a cold wallet, not a daily hot wallet.

## Copyright

"If I buy an NFT, can I use the image commercially?"

Answer: **it depends on the license**.

Common models:

- **Commercial rights**: you may use the image commercially.
- **Personal use only**: avatar and sharing are allowed, commercial use is not.
- **Ownership record only**: the project keeps the copyright.

Read the project's license before buying. Otherwise, you may think you bought IP rights when you only bought a token pointing to an image.

## Quick Memory Table

| Key Point | One-Sentence Version |
|---|---|
| NFT essence | On-chain record that a unique token ID belongs to an address. |
| ERC-721 | Main NFT standard. |
| Uses | Collectibles, domains, memberships, game items, asset certificates. |
| Value | Depends on community, rights, and utility, not just technology. |
| Biggest safety risk | `setApprovalForAll` phishing. |
| Mindset | Hobby spending first, investment second if at all. |

## What to Read Next

Part 3 ends here. Next we move to application layers: DeFi, DEXs, and DAOs.

-> [11. What Is DeFi?](../04-applications/01-defi.md)

---

> If you remember one sentence:
> **An NFT is a unique on-chain certificate, not usually the file itself. The biggest practical risk is malicious approval.**
