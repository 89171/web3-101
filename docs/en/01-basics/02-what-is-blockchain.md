# 02. What Is a Blockchain?

## One-Sentence Version

A blockchain is a **public ledger maintained by a network, visible to everyone, and hard for any single party to tamper with**.

## First Think "Ledger," Not "Chain"

The word blockchain sounds technical, but the core idea is simple: it is a ledger.

Imagine this:

> You and 9 friends keep accounts in a group chat. Whenever someone sends money, they post a message like "A sends 10 dollars to B." Everyone copies the message into their own notebook.

This simple game already has many blockchain properties:

- **Public**: everyone sees every transaction.
- **Decentralized**: no single group admin controls the ledger.
- **Hard to tamper with**: if you secretly edit your notebook, the other 9 notebooks disagree.
- **No bank needed**: A and B can transact without a third party.

A blockchain scales this "10-person ledger game" to thousands of computers around the world and uses cryptography to enforce the rules.

## Blocks and Chains

One-by-one messages are messy, so the group changes the rules:

> Every 10 minutes, all transactions from that period are packed into one page. Everyone checks the page, and if it is valid, they add it to the notebook.

That page is a **block**.

To stop someone from tearing out a page and rewriting history, they add another rule:

> At the top of each page, write the fingerprint of the previous page.

That fingerprint is a **hash**. If you change even one character on the previous page, the fingerprint changes completely, and the next page no longer matches.

Each page points to the previous page. These pages form a one-way chain.

So: **blocks of records + each block pointing to the previous block = blockchain**.

## Who Maintains the Ledger?

In a group of friends, people know each other. A global network of computers does not. So how can it trust participants?

Blockchains turn ledger maintenance into a game with rewards and penalties:

- Anyone can join as a block producer or validator, depending on the chain.
- Participants compete or are selected to add the next block.
- If they do it correctly, they earn rewards. In PoW systems this is often called mining rewards; in PoS systems it is usually validator rewards.
- If they cheat or make invalid blocks, they lose opportunities, and in PoS they may lose part of their stake.

Common mechanisms:

| Mechanism | How It Selects Block Producers | Analogy | Example |
|---|---|---|---|
| **PoW** (Proof of Work) | Whoever solves a computational puzzle first gets to add the block | A race to answer first | Bitcoin |
| **PoS** (Proof of Stake) | Validators stake assets and are selected by protocol rules | Put down a deposit, lose it if you misbehave | Ethereum after 2022 |

The key idea: **honest behavior is economically rewarded, and cheating is expensive**.

## How Immutable Is "Immutable"?

"Immutable" does not mean history is physically impossible to rewrite.

It means:

> **You can try to rewrite it, but the cost is usually too high to be worth it.**

To alter an old transaction, an attacker would need to:

1. Change the old block.
2. Recompute its fingerprint.
3. Recompute every later block that points to it.
4. Convince enough of the network to accept the attacker's version.

The final step is the hard one. On large networks like Bitcoin and Ethereum, controlling enough hash power or stake is extremely expensive. Even if an attacker succeeded, market confidence would likely collapse, reducing the value of what they tried to steal.

So a more accurate version of "immutable" is: **not impossible to change, but usually not economically practical to tamper with**.

## What Problem Does This Solve?

You might ask: why not just use a normal payment app?

That works if **you trust the platform**.

But what if:

- Your account is frozen and you cannot withdraw.
- The platform changes the rules and blocks certain transactions.
- The platform fails and its ledger disappears.
- You need to send money across borders where traditional rails are restricted.

Web2 is efficient because we trust platforms. If that trust fails, the system fails.

Blockchain takes another approach: **instead of trusting one platform, design a system where no single party needs to be fully trusted**.

This does not mean blockchain is always better. It is slower, more expensive, and less forgiving than normal databases. But in situations with high trust costs, such as cross-border settlement, censorship resistance, and long-term asset proofs, it can be valuable.

## Common Misunderstandings

**"Blockchain = Bitcoin"**  
No. Bitcoin was the first major blockchain application, but blockchain is the underlying technology.

**"Blockchain data is encrypted, so others cannot see it"**  
Usually the opposite. On public chains, transaction data is public. What is hidden is not the transaction history, but the real-world identity behind an address.

**"Blockchain is always better than a database"**  
No. Blockchains are slower, more expensive, and costly to store data on. They are worth using when multiple parties need to coordinate without fully trusting one another. For an internal company order database, use a database.

## What to Read Next

- To understand different chains: [03. Public Chains, Layer 1, and Layer 2](03-chains-and-layers.md)
- To understand transaction fees: [04. What Is Gas?](04-what-is-gas.md)

---

> If you remember one sentence:
> **A blockchain is a public ledger maintained by a network, using rules and economic incentives to make participants cooperate honestly.**
