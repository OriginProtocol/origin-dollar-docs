# Registry

Here is the full registry of OUSD smart contracts that have been deployed to the Ethereum mainnet.

{% hint style="success" %}
The main ERC20 address for Origin Dollar (OUSD) is: \
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
Well-known addresses (often proxy wrappers):

| Contract | Address                                                                                                                | ENS                                                                                                                                                     |
| -------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| OUSD     | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)  | <p><a href="https://etherscan.io/address/ousd.eth">ousd.eth</a> </p><p><a href="https://etherscan.io/address/origindollar.eth">origindollar.eth</a></p> |
| Vault    | [0xE75D77B1865Ae93c7eaa3040B038D7aA7BC02F70](https://etherscan.io/address/0xe75d77b1865ae93c7eaa3040b038d7aa7bc02f70)  | [originvault.eth](https://etherscan.io/address/originvault.eth)                                                                                         |
| Oracle   | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4)  | [originoracle.eth](https://etherscan.io/address/originoracle.eth)                                                                                       |

Internal implementation contracts. The Vault is split into VaultAdmin and VaultCore to work-around the maximum contract size limit on Ethereum:

| Contract         | Address                                                                                                               |
| ---------------- | --------------------------------------------------------------------------------------------------------------------- |
| OUSD             | [0x33db8d52d65F75E4cdDA1b02463760c9561A2aa1](https://etherscan.io/address/0x33db8d52d65F75E4cdDA1b02463760c9561A2aa1) |
| VaultAdmin       | [0x3EB68D8f4992A0e34aA58cc3dF86A40814078cF6](https://etherscan.io/address/0x3EB68D8f4992A0e34aA58cc3dF86A40814078cF6) |
| VaultCore        | [0x226de75867B2f785BA19600e2a7e6eFccD57157B](https://etherscan.io/address/0x226de75867B2f785BA19600e2a7e6eFccD57157B) |
| Chainlink Oracle | [0xa7695eED05094E28AA575CB0cCa3CF17848a7981](https://etherscan.io/address/0xa7695eED05094E28AA575CB0cCa3CF17848a7981) |
{% endtab %}

{% tab title="Strategies" %}
Well-known addresses (proxy wrappers):

| Strategy | Address                                                                                                                    | Auto-Allocation            |
| -------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------- |
| Aave     | [0x5e3646A1Db86993f73E6b74A57D8640B69F7e259](https://etherscan.io/address/0x5e3646A1Db86993f73E6b74A57D8640B69F7e259)      | Manual allocation          |
| Compound | [0x9c459eeb3FA179a40329b81C1635525e9A0Ef094](https://etherscan.io/address/0x9c459eeb3FA179a40329b81C1635525e9A0Ef094)      | 100% of USDC, USDT and DAI |
| Convex   | [0xEA2Ef2e2E5A749D4A66b41Db9aD85a38Aa264cb3](https://etherscan.io/address/0xEA2Ef2e2E5A749D4A66b41Db9aD85a38Aa264cb3#code) | Manual allocation          |

Internal implementation contracts:

| Strategy | Address                                                                                                                    |
| -------- | -------------------------------------------------------------------------------------------------------------------------- |
| Aave     | [0xA050eBE34Be464902F7E0F7F451f4B5253d57114](https://etherscan.io/address/0xA050eBE34Be464902F7E0F7F451f4B5253d57114)      |
| Compound | [0xF37B4C48fd3ce4C8E7E8b2ad391a9480842F0b8E](https://etherscan.io/address/0xF37B4C48fd3ce4C8E7E8b2ad391a9480842F0b8E)      |
| Convex   | [0x08f3a0637851aA1B0E0750aA3d46E0E356f349aC](https://etherscan.io/address/0x08f3a0637851aa1b0e0750aa3d46e0e356f349ac#code) |
{% endtab %}

{% tab title="Oracles" %}
The following oracles are used to fetch or compute a price for **DAI/USD:**

| Oracle    | Pair    | Contract                                                                                                              |
| --------- | ------- | --------------------------------------------------------------------------------------------------------------------- |
| Chainlink | DAI/USD | [0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9](https://etherscan.io/address/0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9) |

The following oracles are used to fetch a price for **USDT/USD:**

| O**racle** | Pair     | Contract                                                                                                              |
| ---------- | -------- | --------------------------------------------------------------------------------------------------------------------- |
| Chainlink  | USDT/USD | [0x3E7d1eAB13ad0104d2750B8863b489D65364e32D](https://etherscan.io/address/0x3E7d1eAB13ad0104d2750B8863b489D65364e32D) |

The following oracles are used to fetch a price for **USDC/USD:**

| O**racle** | Pair     | Contract                                                                                                              |
| ---------- | -------- | --------------------------------------------------------------------------------------------------------------------- |
| Chainlink  | USDC/USD | [0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6](https://etherscan.io/address/0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6) |
{% endtab %}

{% tab title="Governance" %}


| Contract            | Address                                                                                                               | ENS                                                                                                                                                                            |
| ------------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 5 of 8 Multisig     | [0xbe2AB3d3d8F6a32b96414ebbd865dBD276d3d899](https://etherscan.io/address/0xbe2AB3d3d8F6a32b96414ebbd865dBD276d3d899) | [originprotocol.eth](https://etherscan.io/address/originprotocol.eth)                                                                                                          |
| 2 of 9 Multisig     | [0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC](https://etherscan.io/address/0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC) | [originstrategist.eth](https://etherscan.io/address/originstrategist.eth)                                                                                                      |
| Governor / Timelock | [0x72426BA137DEC62657306b12B1E869d43FeC6eC7](https://etherscan.io/address/0x72426BA137DEC62657306b12B1E869d43FeC6eC7) | <p><a href="https://etherscan.io/address/origingovernor.eth">origingovernor.eth</a></p><p><a href="https://etherscan.io/address/origintimelock.eth">origintimelock.eth</a></p> |
| OGN Buyback         | [0x77314EB392b2be47C014cde0706908b3307Ad6a9](https://etherscan.io/address/0x77314EB392b2be47C014cde0706908b3307Ad6a9) | [originbuyback.eth](https://etherscan.io/address/originbuyback.eth)                                                                                                            |
{% endtab %}

{% tab title="Stablecoins" %}
| Contract                                                                        | Address                                                                                                               |
| ------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)  | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}

{% tab title="Staking" %}
| Contract    | Address                                                                                                               | ENS                                                                 |
| ----------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| OGN Staking | [0x501804B374EF06fa9C427476147ac09F1551B9A0](https://etherscan.io/address/0x501804B374EF06fa9C427476147ac09F1551B9A0) | [originstaking.eth](https://etherscan.io/address/originstaking.eth) |

Internal implementation contracts:

| Contract    | Address                                                                                                               |
| ----------- | --------------------------------------------------------------------------------------------------------------------- |
| OGN Staking | [0x8cd68a1e0b79150455c5498882d5d5d3df2dde08](https://etherscan.io/address/0x8cd68a1e0b79150455c5498882d5d5d3df2dde08) |

OUSD compensation contract ([details](https://medium.com/originprotocol/origin-delivers-on-compensation-promise-claim-your-ousd-and-ogn-now-a9fa9b840476)):

| Contract          | Address                                                                                                               |
| ----------------- | --------------------------------------------------------------------------------------------------------------------- |
| OUSD Compensation | [0x9C94df9d594BA1eb94430C006c269C314B1A8281](https://etherscan.io/address/0x9C94df9d594BA1eb94430C006c269C314B1A8281) |
{% endtab %}

{% tab title="Swap" %}
| Contract | Address                                                                                                               | ENS                                                           |
| -------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| Swap     | [0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70](https://etherscan.io/address/0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70) | [originswap.eth](https://etherscan.io/address/originswap.eth) |
{% endtab %}
{% endtabs %}





&#x20;
