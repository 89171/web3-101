# 附录 A：术语速查表

> 按字母 / 拼音排序。每条只给一句话定义，深入解释见各章节。

## A

- **AMM（Automated Market Maker，自动做市商）**：DEX 用数学公式自动定价的撮合方式，不用挂单簿。详见 [第 12 章](../04-applications/02-dex.md)。
- **Airdrop（空投）**：项目方免费发代币给一群用户，常用于早期推广和奖励参与者。
- **APY / APR**：年化收益率。APY 含复利，APR 不含。Web3 里常见但「保本高 APY」往往是陷阱。
- **Approve（授权）**：让某个合约能从你账户里转走某种代币的签名。**最常见的钓鱼对象**。

## B

- **Block（区块）**：账本上的「一页」，包含一段时间内的交易记录。
- **Blockchain（区块链）**：用密码学把一页页区块串成链的公开账本。详见 [第 2 章](../01-basics/02-what-is-blockchain.md)。
- **Blind sign（盲签）**：钱包无法解析签名内容，只能显示乱码。**永远不要盲签**。
- **Bridge（跨链桥）**：在不同链之间搬资产的设施，但**也是黑客攻击的重灾区**。
- **BRC-20**：比特币上的代币标准，结构和以太坊系完全不同。

## C

- **CEX（Centralized Exchange，中心化交易所）**：像 Binance、Coinbase 这种公司运营的交易所。详见 [第 14 章](../05-trading-and-safety/01-cex-vs-dex.md)。
- **Coin**：链自己的原生币，比如 BTC、ETH、SOL。详见 [第 8 章](../03-assets/01-tokens.md)。
- **Cold wallet（冷钱包）**：私钥不联网的钱包，主要指硬件钱包。详见 [第 6 章](../02-wallets/02-hot-vs-cold.md)。
- **Consensus（共识机制）**：链如何决定谁来记账、记的对不对。常见的有 PoW、PoS。

## D

- **DApp（Decentralized Application，去中心化应用）**：跑在区块链上、用智能合约的应用。
- **DAO（Decentralized Autonomous Organization）**：去中心化自治组织。详见 [第 13 章](../04-applications/03-dao.md)。
- **DeFi（Decentralized Finance）**：去中心化金融。详见 [第 11 章](../04-applications/01-defi.md)。
- **DEX（Decentralized Exchange）**：去中心化交易所。详见 [第 12 章](../04-applications/02-dex.md)。
- **Depeg（脱锚）**：稳定币的价格偏离了它锚定的法币价格。

## E

- **ENS（Ethereum Name Service）**：把以太坊地址解析成 `xxx.eth` 这种人类可读名字的服务。
- **ERC-20**：以太坊系链上的同质化代币标准。
- **ERC-721 / 1155**：以太坊系链上的非同质化代币（NFT）标准。
- **EVM（Ethereum Virtual Machine）**：以太坊的执行环境。「EVM 兼容链」意思是能跑以太坊的合约。
- **EOA（Externally Owned Account）**：普通用户的账户，由私钥控制。区别于「合约账户」。

## F

- **Faucet（水龙头）**：免费领测试币的网站，开发或学习时用。
- **Farming（流动性挖矿）**：把资产提供给协议、赚奖励代币的活动。
- **Fungible（同质化）**：每一份都等价，可互换。
- **FUD / FOMO**：FUD = Fear, Uncertainty, Doubt（散布恐慌打压价格）；FOMO = Fear of Missing Out（怕错过的恐慌性买入）。

## G

- **Gas**：链上操作的网络使用费，用链的原生币付。详见 [第 4 章](../01-basics/04-what-is-gas.md)。
- **Gwei**：以太坊上 Gas 价格的单位。1 ETH = 10⁹ Gwei。
- **Governance Token（治理代币）**：持有就有 DAO 投票权的代币，如 UNI、AAVE。

## H

- **Hash（哈希）**：一段内容的「数字指纹」。改一个字，指纹完全变。区块链用它把区块串成链。
- **Hardware wallet（硬件钱包）**：把私钥存在专门设备里的冷钱包，如 Ledger、Trezor。
- **Hot wallet（热钱包）**：私钥存在联网设备里的钱包，如 MetaMask、手机钱包。
- **Honeypot（蜜罐）**：合约设计成「能买不能卖」的诈骗代币。

## I

- **Impermanent Loss（无常损失）**：流动性提供者因为池子里两种资产价格分歧而少赚的损失。
- **IPFS**：去中心化的文件存储网络，NFT 的图片常存在这里。

## K

- **KYC（Know Your Customer）**：身份认证。CEX 通常要求；DEX 协议层通常不需要，但前端入口可能有限制。

## L

- **Layer 1（L1）**：独立的底层公链，比如以太坊、Solana。
- **Layer 2（L2）**：建在 L1 之上的扩容方案，通常更便宜更快，安全模型要看它如何依赖 L1。详见 [第 3 章](../01-basics/03-chains-and-layers.md)。
- **LP（Liquidity Provider，流动性提供者）**：往 AMM 池子里存资产、赚手续费的人。
- **Liquidation（清算）**：抵押品价值跌破阈值时，系统强制卖掉你的抵押品来还债。

## M

- **Mainnet（主网）**：链的正式网络，跟「测试网」相对。
- **Mempool（内存池）**：等待被打包进区块的交易暂存区。
- **Meme coin（模因币）**：靠社区文化和情绪驱动、没什么基本面的代币，如 DOGE、PEPE。
- **MetaMask**：最主流的浏览器插件钱包。
- **MEV（Maximal Extractable Value）**：验证者、区块构建者或搜索者通过交易排序获利的空间，包括「夹子攻击」。
- **Mint（铸造）**：把一个 NFT 或代币首次「铸造出来」上链的动作。
- **Multi-sig（多签）**：需要多个私钥共同签名才能动账户的设置，常用于 DAO 金库。

## N

- **NFT（Non-Fungible Token）**：非同质化代币。详见 [第 10 章](../03-assets/03-nft.md)。
- **Node（节点）**：参与维护一条链、保存账本副本的电脑。

## O

- **Oracle（预言机）**：把链下数据（如价格、天气）喂给链上合约的服务。Chainlink 是最主流的。
- **Order book（挂单簿）**：传统交易所的撮合方式，CEX 用，部分 DEX 也用。

## P

- **PoW（Proof of Work）**：靠算力竞争记账权的共识机制，比特币用的就是这个。
- **PoS（Proof of Stake）**：靠质押代币获得记账权的共识机制，以太坊 2022 年后改用 PoS。
- **Permit / Permit2**：一种离线授权签名，**不上链不花 Gas，但风险极高**。
- **Public key（公钥）/ Address（地址）**：可以公开告诉别人的「保险箱编号」。
- **Private key（私钥）**：真正控制资产的钥匙，**绝不能告诉任何人**。

## R

- **Rebase**：代币机制的一种，按一定规则增减所有持有者的余额。
- **Restaking（再质押）**：把质押凭证再次质押到其他协议赚奖励。EigenLayer 是代表。
- **Rug pull（跑路盘）**：项目方抽走流动性、卷款跑路。
- **revoke.cash**：检查和取消代币授权的常用工具。

## S

- **Seed phrase / Mnemonic（助记词）**：一套钱包的 12 或 24 个英文单词恢复钥匙，能派生出私钥，**等同于全部资产**。
- **Smart contract（智能合约）**：部署在链上的程序，按规则自动执行。
- **Snapshot**：链下投票工具，用签名计票，不花 Gas。
- **Slippage（滑点）**：下单价格和实际成交价格的差距。
- **Stablecoin（稳定币）**：锚定法币（多为美元）的代币，如 USDT、USDC、DAI / USDS。详见 [第 9 章](../03-assets/02-stablecoins.md)。
- **Staking（质押）**：把代币锁进协议、参与共识或赚奖励的活动。

## T

- **Testnet（测试网）**：链的「演练场」，币没价值，用来开发和学习。
- **Token**：在某条链上发行的代币（区别于链原生的 Coin）。
- **TVL（Total Value Locked）**：DeFi 协议里锁定的总资产价值，常用来衡量协议规模。

## U

- **USDT / USDC**：两个主流的法币储备型稳定币。
- **Uniswap**：最早、最大的 AMM 类 DEX。

## V

- **Validator（验证者）**：PoS 共识机制下负责记账的角色，对应 PoW 的「矿工」。

## W

- **Wallet（钱包）**：管理私钥、发起签名的工具。本身不存资产，资产在链上。详见 [第 5 章](../02-wallets/01-wallet-basics.md)。
- **Web3**：用户自己拥有账号和资产的互联网。详见 [第 1 章](../01-basics/01-what-is-web3.md)。
- **wETH（Wrapped ETH）**：「包装版 ETH」，符合 ERC-20 标准，能跟其他代币一样在合约里用。1 ETH = 1 wETH。

## Z

- **ZK / Zero-Knowledge Proof（零知识证明）**：一种密码学技术，让一方证明「我知道某件事」而不暴露细节。zk Rollup 类 L2 用的就是这技术。

---

[← 返回 README](../../README.md)
