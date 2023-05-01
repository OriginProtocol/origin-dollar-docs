# Registry

Here is the full registry of OUSD smart contracts that have been deployed to the Ethereum mainnet.

{% hint style="success" %}
The main ERC20 address for Origin Dollar (OUSD) is: \
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

**OUSD Core**

Most of our contracts are upgradable via a well-known proxy wrapper and an implementation contract. The Vault is split into VaultAdmin and VaultCore to work around the maximum contract size limit on Ethereum

| Contract             | Address                                                                                                                    | ENS                                                                                                                                                     |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| OUSD                 | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)      | <p><a href="https://etherscan.io/address/ousd.eth">ousd.eth</a> </p><p><a href="https://etherscan.io/address/origindollar.eth">origindollar.eth</a></p> |
| OUSD Implementation  | [0x33db8d52d65F75E4cdDA1b02463760c9561A2aa1](https://etherscan.io/address/0x33db8d52d65F75E4cdDA1b02463760c9561A2aa1)      |                                                                                                                                                         |
| wOUSD                | [0xD2af830E8CBdFed6CC11Bab697bB25496ed6FA62](https://etherscan.io/address/0xD2af830E8CBdFed6CC11Bab697bB25496ed6FA62)      | [wousd.eth](https://etherscan.io/address/wousd.eth)                                                                                                     |
| wOUSD Implementation | [0xbf3b9b141cb3629f5bb8f721cba9265c92494539](https://etherscan.io/address/0xbf3b9b141cb3629f5bb8f721cba9265c92494539)      |                                                                                                                                                         |
| Vault                | [0xE75D77B1865Ae93c7eaa3040B038D7aA7BC02F70](https://etherscan.io/address/0xe75d77b1865ae93c7eaa3040b038d7aa7bc02f70)      | [originvault.eth](https://etherscan.io/address/originvault.eth)                                                                                         |
| VaultAdmin           | [0x6a16335a203d4151892ca1260cca9d500fe82298](https://etherscan.io/address/0x6a16335a203d4151892ca1260cca9d500fe82298#code) |                                                                                                                                                         |
| VaultCore            | [0x48cf14dea2f5dd31c57218877195913412d3278a](https://etherscan.io/address/0x48cf14dea2f5dd31c57218877195913412d3278a)      |                                                                                                                                                         |



**OGV Governance & Staking**

OGV can be locked in exchange for veOGV to get economic and governance rights over OUSD.&#x20;

| Contract      | Address                                                                                                               | ENS                                                                                                                                               |
| ------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| OGV           | [0x9c354503c38481a7a7a51629142963f98ecc12d0](https://etherscan.io/address/0x9c354503c38481a7a7a51629142963f98ecc12d0) | [ogv.eth](https://etherscan.io/address/ogv.eth)                                                                                                   |
| veOGV         | [0x0c4576ca1c365868e162554af8e385dc3e7c66d9](https://etherscan.io/address/0x0c4576ca1c365868e162554af8e385dc3e7c66d9) | <p><a href="https://etherscan.io/address/veogv.eth">veogv.eth</a><br><a href="https://etherscan.io/address/ogvstaking.eth">ogvstaking.eth</a></p> |
| RewardsSource | [0x7d82e86cf1496f9485a8ea04012afeb3c7489397](https://etherscan.io/address/0x7d82e86cf1496f9485a8ea04012afeb3c7489397) |                                                                                                                                                   |



**Strategies**

| Contract             | Address                                                                                                                    |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Aave                 | [0x5e3646A1Db86993f73E6b74A57D8640B69F7e259](https://etherscan.io/address/0x5e3646A1Db86993f73E6b74A57D8640B69F7e259)      |
| Compound             | [0x9c459eeb3FA179a40329b81C1635525e9A0Ef094](https://etherscan.io/address/0x9c459eeb3FA179a40329b81C1635525e9A0Ef094)      |
| Convex DAI+USDC+USDT | [0xEA2Ef2e2E5A749D4A66b41Db9aD85a38Aa264cb3](https://etherscan.io/address/0xEA2Ef2e2E5A749D4A66b41Db9aD85a38Aa264cb3#code) |
| Convex LUSD+3Crv     | [0x7A192DD9Cc4Ea9bdEdeC9992df74F1DA55e60a19](https://etherscan.io/address/0x7A192DD9Cc4Ea9bdEdeC9992df74F1DA55e60a19)      |
| Convex OUSD+3Crv     | [0x89eb88fedc50fc77ae8a18aad1ca0ac27f777a90](https://etherscan.io/address/0x89eb88fedc50fc77ae8a18aad1ca0ac27f777a90#code) |
| Morpho Compound      | [0x5A4eEe58744D1430876d5cA93cAB5CcB763C037D](https://etherscan.io/address/0x5A4eEe58744D1430876d5cA93cAB5CcB763C037D)      |
| Morpho Aave          | [0x79F2188EF9350A1dC11A062cca0abE90684b0197](https://etherscan.io/address/0x79f2188ef9350a1dc11a062cca0abe90684b0197)      |



**Yield Harvesting & Collection**

| Contract      | Address                                                                                                                    | ENS                                                                     |
| ------------- | -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Harvester     | [0x21fb5812d70b3396880d30e90d9e5c1202266c89](https://etherscan.io/address/0x21fb5812d70b3396880d30e90d9e5c1202266c89#code) | [originharvester.eth](https://etherscan.io/address/originharvester.eth) |
| Dripper       | [0x80c898ae5e56f888365e235ceb8cea3eb726cb58](https://etherscan.io/address/0x80c898ae5e56f888365e235ceb8cea3eb726cb58#code) | [origindripper.eth](https://etherscan.io/address/origindripper.eth)     |
| Token Buyback | [0x6C5cdfB47150EFc52072cB93Eea1e0F123529748](https://etherscan.io/address/0x6c5cdfb47150efc52072cb93eea1e0f123529748)      | [originbuyback.eth](https://etherscan.io/address/originbuyback.eth)     |



**Swapping**

Flipper is a gas-optimized way for users to swap in and out of OUSD at a fixed 1:1 rate with other stablecoins. This contract may become empty on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes.

| Contract | Address                                                                                                               | ENS                                                                 |
| -------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| Flipper  | [0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70](https://etherscan.io/address/0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70) | [originflipper.eth](https://etherscan.io/address/originflipper.eth) |



**Timelock & Multisigs**

| Contract            | Address                                                                                                               | ENS                                                                                                                                         |
| ------------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Governor / Timelock | [0x72426BA137DEC62657306b12B1E869d43FeC6eC7](https://etherscan.io/address/0x72426BA137DEC62657306b12B1E869d43FeC6eC7) | [origingovernor.eth](https://etherscan.io/address/origingovernor.eth) [origintimelock.eth](https://etherscan.io/address/origintimelock.eth) |
| 5 of 8              | [0xbe2AB3d3d8F6a32b96414ebbd865dBD276d3d899](https://etherscan.io/address/0xbe2AB3d3d8F6a32b96414ebbd865dBD276d3d899) | [originprotocol.eth](https://etherscan.io/address/originprotocol.eth)                                                                       |
| 2 of 9              | [0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC](https://etherscan.io/address/0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC) | [originstrategist.eth](https://etherscan.io/address/originstrategist.eth)                                                                   |

**Chainlink Keepers**

Chainlink Keepers are an automated and decentralized way for OUSD to perform regularly scheduled tasks.

| Keeper        | Address                                    | Purpose                  |
| ------------- | ------------------------------------------ | ------------------------ |
| OUSD Keeper 4 | 0xAAdf7D0f2E217168ACC90e5d39A42a24857620d5 | Executing a daily rebase |



**Stablecoins**

OUSD is backed by the following stablecoins:

| [USDT](https://etherscan.io/address/0xdac17f958d2ee523a2206206994597c13d831ec7) | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0xdac17f958d2ee523a2206206994597c13d831ec7) |
| ------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| [USDC](https://etherscan.io/address/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48) | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48) |
| [DAI](https://etherscan.io/address/0x6b175474e89094c44da98b954eedeac495271d0f)  | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x6b175474e89094c44da98b954eedeac495271d0f) |



**Oracles**

The following Chainlink oracles are used to protect the vault in case a backing stablecoin loses value. They also offer slippage protection when harvesting rewards tokens.

| Pair                                                                      | Contract                                                                                                              |
| ------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| [USDT/USD](https://data.chain.link/ethereum/mainnet/stablecoins/usdt-usd) | [0x3E7d1eAB13ad0104d2750B8863b489D65364e32D](https://etherscan.io/address/0x3E7d1eAB13ad0104d2750B8863b489D65364e32D) |
| [USDC/USD](https://data.chain.link/ethereum/mainnet/stablecoins/usdc-usd) | [0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6](https://etherscan.io/address/0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6) |
| [DAI/USD](https://data.chain.link/ethereum/mainnet/stablecoins/dai-usd)   | [0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9](https://etherscan.io/address/0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9) |
| [COMP/USD](https://data.chain.link/ethereum/mainnet/crypto-usd/comp-usd)  | [0xdbd020caef83efd542f4de03e3cf0c28a4428bd5](https://etherscan.io/address/0xdbd020caef83efd542f4de03e3cf0c28a4428bd5) |
| [AAVE/USD](https://data.chain.link/ethereum/mainnet/crypto-usd/aave-usd)  | [0x547a514d5e3769680Ce22B2361c10Ea13619e8a9](https://etherscan.io/address/0x547a514d5e3769680Ce22B2361c10Ea13619e8a9) |
| [CRV/USD](https://data.chain.link/ethereum/mainnet/crypto-usd/crv-usd)    | [0xcd627aa160a6fa45eb793d19ef54f5062f20f33f](https://etherscan.io/address/0xcd627aa160a6fa45eb793d19ef54f5062f20f33f) |
| [CVX/USD](https://data.chain.link/ethereum/mainnet/crypto-usd/cvx-usd)    | [0xd962fC30A72A84cE50161031391756Bf2876Af5D](https://etherscan.io/address/0xd962fC30A72A84cE50161031391756Bf2876Af5D) |

**Deprecated**

These contacts are no longer actively used but are included here for historical purposes.

| Contract                            | Address                                                                                                               |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Original OGN Staking                | [0x501804B374EF06fa9C427476147ac09F1551B9A0](https://etherscan.io/address/0x501804B374EF06fa9C427476147ac09F1551B9A0) |
| Original OGN Staking Implementation | [0x8cd68a1e0b79150455c5498882d5d5d3df2dde08](https://etherscan.io/address/0x8cd68a1e0b79150455c5498882d5d5d3df2dde08) |
| OUSD Compensation                   | [0x9C94df9d594BA1eb94430C006c269C314B1A8281](https://etherscan.io/address/0x9C94df9d594BA1eb94430C006c269C314B1A8281) |
| Old OUSD Vault                      | [0x277e80f3E14E7fB3fc40A9d6184088e0241034bD](https://etherscan.io/address/0x277e80f3E14E7fB3fc40A9d6184088e0241034bD) |
| Old Buyback Contract                | [0x77314EB392b2be47C014cde0706908b3307Ad6a9](https://etherscan.io/address/0x77314EB392b2be47C014cde0706908b3307Ad6a9) |

&#x20;
