# Stablecoin Evaluation Framework

While two stablecoins may both appear to be worth $1, there are many different ways a protocol can go about creating this price stability. In the not too distant past, we've seen what can happen when the real risk can be difficult to understand (UST). To help with this, we've created this framework as a clear, objective, and comprehensive way to evaluate whitelisting of new stablecoins as well as provide an audit trail for future investors to understand the DAO’s decision making process.

Risks are broken down into 4 main buckets:

* Financial Risk
* Governance Risk
* Security Risk
* Legal & Regulatory Risk

These risks are then measured through our **stablecoin scorecard** methodology to provide a quantitative measurement of a given stablecoin's risk. Below you will find some of the various inputs that go into the scorecard. Of course, even a stablecoin that scores well overall could still be unsuitable for OUSD, so it important to take all data into context.

### Financial Risk

#### Reserves

For a stablecoin to maintain its value, there must be something “backing” the asset, and the ability to mint or redeem for this established value stabilizes the peg, often done by arbitrageurs.

* Collateral: On-chain vs off-chain assets, stablecoins vs volatile assets, market cap of assets (shitcoins vs. blue chips)
* Collateral ratio: The higher the collateral ratio, the more likely the stablecoin is able to maintain its peg during market stresses, and the ratio requirement will vary based on the volatility of the collateral.&#x20;
* Collateral quality: This can be broken down into the volatility of the assets and how much liquidity is available for efficient liquidations.
* Minting mechanism: Minting helps maintain the $1 ceiling, supplying the market whenever the coin goes above peg - key questions include how is the coin minted, is it permissioned or permissionless, and are there any fees that can identify the natural ceiling.
* Redemption mechanism: Redemption maintains the floor value of $1, such that someone holding it may redeem it for underlying collateral value, the same questions apply as with minting.

#### Liquidity

Especially during times of stress, it’s important to understand how much of a stablecoin can be converted back into the 3 main stables (USDT/DAI/USDC) without redemption mechanisms.&#x20;

* Liquidity Depth: Typically on Curve, the more depth, the less slippage when swapping.
* DEX token (im)balance: When evaluating whether to enter or exit a pool, it’s important to bear in mind how far away the pool is from significant imbalance.
* Sustainability: If a pool is only sustained based on bribes, it’s likely that if the bribes stop, TVL will dry up and then the pool will become unbalanced and difficult to exit without slippage.

#### Longevity & Historical Performance&#x20;

Unlike stocks, past performance can often be a good predictor of future performance for stablecoins, especially a proven track record during market volatility and stress on the system.&#x20;

* Total Supply: A token with a higher market cap will have greater confidence in terms of its security, since the potential reward is higher for hackers.&#x20;
* Days Live: The length of time a token has been live can be a good signal for security (also known as the _Lindy Effect)_, as it will have had more time for scrutiny by hackers, especially when combined with market cap (Days live x Market Cap = AUC).&#x20;
* Volatility: This can be measured in terms of regular volatility as well as maximum volatility, indicating how often it has gone off peg and to what extent.&#x20;

### Governance Risk

#### Governance

For all kinds of (both centralized and decentralized) stablecoins, governance is really important, with different risks depending on the openness of the entity that controls it.&#x20;

* Transparency: How is governance carried out - is it in public? How thoroughly are proposals vetted?&#x20;
* Holders: Who are the major holders of both their DAO token and stablecoin?&#x20;
* Powers & Process: How quickly can code be shipped and through what process? Are there emergency powers?&#x20;
* Admin Keys: How do they manage access control? Is there a multi-sig policy in place?
* Centralization: Is there any significant risk to the future control of the asset, and is it decentralized or centralized? Identities: Who controls the the DAO and who are the core contributors, are they doxed or anonymous? Where are they located?

### Security Risk

#### Security & Audits

While certainly not foolproof, the more intelligent eyes on the code, typically the lower probability of a major security risk.&#x20;

* Audits: Which auditing firms, which code was reviewed, and when? Are audits continuous or one-time?&#x20;
* Smart contracts: Which code is being used, and how much, if any is recycled from other battle-tested protocols?&#x20;
* Bug Bounties: Are there any bug bounties available such as ImmuneFi?&#x20;
* External Safety Scores: There are some companies/projects that are now working on generating safety scores for various protocols, so it’s always good to have another datapoint from an independent source (although these scores could be influenced).&#x20;

### Legal & Regulatory Risk

#### Regulation

Stablecoins are under intense regulatory scrutiny, and there are several risks worth considering when it comes to sanctions and governmental actions.&#x20;

* Decentralization: Is this controlled by a centralized entity or is it just code?
* Censorship: Is it able to be censored at will and have funds frozen?&#x20;
* Privacy: How much privacy does this coin afford someone and is it easily used for AML or OFAC avoidance purposes?&#x20;
* Historical: Has it come under legal pressure before? And to what extent (ie. lawsuits & settlements)?
