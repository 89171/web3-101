# 13. DAOs

## One-Sentence Version

A DAO is a **decentralized autonomous organization**: a group that uses wallets and voting to manage a shared treasury or project. Ideally, no single CEO controls everything, and key rules live on-chain.

## How It Differs From a Company

A traditional company works top-down:

- Founders or CEO set direction.
- Board approves major decisions.
- Employees execute.
- Shareholders vote occasionally.

A DAO aims for a different structure:

- No single CEO has final authority, at least in theory.
- Governance token holders vote.
- Major decisions go through proposals.
- Treasury spending is controlled by voting or multisigs.
- Rules and execution are as transparent and on-chain as possible.

| | Company | DAO |
|---|---|---|
| Power source | Shares and management roles | Governance tokens or membership rights |
| Decisions | CEO and board | Proposals and votes |
| Treasury | Finance team and approvals | On-chain treasury and smart contracts or multisigs |
| Entry | Hiring or investment | Token or membership access |
| Transparency | Mostly internal | On-chain funds and votes are public; off-chain decisions may not be |
| Geography | Legal jurisdictions matter | Global by default, though legal issues remain |

## What DAOs Look Like in Practice

### 1. Protocol Governance DAOs

Common in DeFi. A protocol issues a governance token, and holders vote on:

- Fees
- Risk parameters
- Treasury spending
- New features or deployments

Examples: **Uniswap DAO**, **Aave DAO**, **MakerDAO**, **Compound DAO**.

This is one of the most practical DAO forms.

### 2. Investment DAOs

Groups pool capital and vote on investments.

Examples: **The LAO**, **MetaCartel Ventures**.

They resemble venture funds but coordinate through tokens, memberships, and proposals.

### 3. Collector DAOs

Groups pool money to buy something.

Famous example: **ConstitutionDAO**, which raised about 47 million dollars in 2021 to bid on an original copy of the US Constitution. It did not win, but thousands of people coordinated quickly.

### 4. Community or Culture DAOs

Communities organized around culture, media, identity, or shared interests. Token or NFT ownership may grant access.

Examples include early **Friends With Benefits (FWB)**.

These are hard to sustain because culture and governance are both hard.

### 5. Service DAOs

Professional groups that sell services as a DAO and distribute work internally.

Examples: **Raid Guild** for development, **LexDAO** for legal service experiments.

## How DAO Voting Works

### 1. On-Chain Voting

Proposals and votes happen on-chain. Each vote costs gas.

Pros: verifiable and can execute automatically.  
Cons: expensive and often low participation.

### 2. Off-Chain Voting

The most common tool is **Snapshot**. Users sign messages with wallets, and votes are counted based on token holdings at a snapshot time.

Execution usually depends on a multisig or team following the vote result.

Pros: free and easy.  
Cons: not fully automatic.

### 3. Delegation

You delegate voting power to someone else.

Pros: useful if you do not have time to study every proposal.  
Cons: power can concentrate among a few delegates.

## DAO Reality Check

DAOs sound idealistic, but real DAOs face many problems.

### 1. Low Voter Turnout

Many DAOs have very low participation. A small group of active voters and whales can decide outcomes.

### 2. Whale Control

Token-weighted voting gives more power to large holders. This is not so different from shareholder voting.

### 3. Governance Attacks

Attackers can borrow or acquire tokens, pass malicious proposals, and drain treasuries if safeguards are weak.

### 4. Slow Decisions

Discussion, proposal, voting, and execution can take weeks. This is hard when fast responses are needed.

Many protocols solve this with "governance sets direction, teams execute," which becomes more company-like.

### 5. Unclear Legal Status

In many countries, DAOs do not have clear legal status:

- Who signs contracts?
- Who gets sued?
- How are taxes handled?

Places such as Wyoming and the Marshall Islands have experimented with DAO LLC frameworks, but they are not universal.

### 6. Decentralization Theater

Some projects call themselves DAOs while founders retain real control through token concentration, admin keys, or veto powers.

## How to Judge Whether a DAO Is Real

Ask:

1. **Token distribution**: how much do founders and top holders control?
2. **Proposal history**: are there real votes with real consequences?
3. **Treasury control**: is it automatic, multisig-based, or founder-controlled?
4. **Emergency powers**: can the team override votes?

If these look centralized, it may be a traditional team using DAO branding.

## Quick Memory Table

| Key Point | One-Sentence Version |
|---|---|
| DAO essence | A group using wallets and voting to manage a shared project or treasury. |
| Voting power | Often comes from governance token holdings. |
| Tools | On-chain voting, Snapshot, delegation, multisigs. |
| Problems | Low turnout, whales, slow decisions, legal uncertainty. |
| Real or fake | Check token distribution, proposal history, treasury control, and veto powers. |

## What to Read Next

Part 4 ends here. Next: trading and safety.

-> [14. Centralized Exchanges vs Decentralized Exchanges](../05-trading-and-safety/01-cex-vs-dex.md)

---

> If you remember one sentence:
> **A DAO uses wallet-based voting to manage a project or treasury, but calling something a DAO does not make it decentralized.**
