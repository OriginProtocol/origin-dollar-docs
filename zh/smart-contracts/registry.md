# 登记处

这是已部署到以太坊主网的 OUSD 智能合约的完整注册表。

{% hint style="success" %}
Origin Dollar（OUSD）的主要 ERC20 地址为：   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
知名的地址 \(often proxy wrappers\):

| 合约                  | 地址                                                                                                                    | ENS                                                                   |
|:------------------- |:--------------------------------------------------------------------------------------------------------------------- |:--------------------------------------------------------------------- |
| OUSD                | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86) | [ousd.eth](https://etherscan.io/address/ousd.eth)                     |
| 保险库 （Vault）         | [0x277e80f3E14E7fB3fc40A9d6184088e0241034bD](https://etherscan.io/address/0x277e80f3E14E7fB3fc40A9d6184088e0241034bD) | [originvault.eth](https://etherscan.io/address/originvault.eth)       |
| 时间锁（Timelock）       | [0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [origintimelock.eth](https://etherscan.io/address/origintimelock.eth) |
| 5 of 8 多钱（Multisig） | [0xe011fA2a6Df98c69383457d87a056Ed0103aA352](https://etherscan.io/address/0xe011fA2a6Df98c69383457d87a056Ed0103aA352) | [originprotocol.eth](https://etherscan.io/address/originprotocol.eth) |
| 神谕（Oracle）          | [0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458](https://etherscan.io/address/0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458) | [originoracle.eth](https://etherscan.io/address/originoracle.eth)     |
| Governor            | [0x8a5fF78BFe0de04F5dc1B57d2e1095bE697Be76E](https://etherscan.io/address/0x8a5fF78BFe0de04F5dc1B57d2e1095bE697Be76E) | [origingovernor.eth](https://etherscan.io/address/origingovernor.eth) |

内部 implementation 合约：

| 合约                  | 地址                                                                                                                    |
|:------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| OUSD                | [0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805](https://etherscan.io/address/0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805) |
| VaultAdmin          | [0xfbbe3090E06721168979818Fe006A1fcb136e953](https://etherscan.io/address/0xfbbe3090E06721168979818Fe006A1fcb136e953) |
| VaultCore           | [0xB95423e3ca13ce5336Cb177B06cD4f647D2aAd57](https://etherscan.io/address/0xB95423e3ca13ce5336Cb177B06cD4f647D2aAd57) |
| Mix Oracle          | [0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458](https://etherscan.io/address/0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458) |
| Chainlink Oracle    | [0x8DE3Ac42F800a1186b6D70CB91e0D6876cC36759](https://etherscan.io/address/0x8DE3Ac42F800a1186b6D70CB91e0D6876cC36759) |
| Open Uniswap Oracle | [0xa8f14F558aC70F5f52C37cD96d802ef9210023C5](https://etherscan.io/address/0xa8f14F558aC70F5f52C37cD96d802ef9210023C5) |
{% endtab %}

{% tab title="Strategies" %}
[Well-known addresses \(proxy wrappers\):](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)

| [Strategy](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Address](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)                                    | [Current Auto-Allocation](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
|:----------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |:-------------------------------------------------------------------------------------------------- |
| Curve \(USDT\)                                                                    | [0xe40e09cD6725E542001FcB900d9dfeA447B529C0](https://etherscan.io/address/0xe40e09cD6725E542001FcB900d9dfeA447B529C0) | 0%                                                                                                 |
| Curve \(USDC\)                                                                    | [0x67023c56548BA15aD3542E65493311F19aDFdd6d](https://etherscan.io/address/0x67023c56548BA15aD3542E65493311F19aDFdd6d) | 0%                                                                                                 |
| Aave                                                                                | [0x051CaEFA90aDf261B8E8200920C83778b7B176B6](https://etherscan.io/address/0x051caefa90adf261b8e8200920c83778b7b176b6) | 100% of DAI                                                                                        |
| Compound                                                                            | [0x12115A32a19e4994C2BA4A5437C22CEf5ABb59C3](https://etherscan.io/address/0x12115A32a19e4994C2BA4A5437C22CEf5ABb59C3) | 100% of USDC and USDT                                                                              |

[Internal implementation contracts:](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)

| [Strategy](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Address](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)                                    |
|:----------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| Curve \(USDT\)                                                                    | [0x641E3b5b081Fb2fb8B43D5a163649312a28e23Da](https://etherscan.io/address/0x641E3b5b081Fb2fb8B43D5a163649312a28e23Da) |
| Curve \(USDC\)                                                                    | [0xF92B0DE25660C18BEDaa55795986781d7899b0f9](https://etherscan.io/address/0xF92B0DE25660C18BEDaa55795986781d7899b0f9) |
| Aave                                                                                | [0x5d9aA9f977E47eA0BFE61BA8b8f535aba02Be135](https://etherscan.io/address/0x5d9aA9f977E47eA0BFE61BA8b8f535aba02Be135) |
| Compound                                                                            | [0xFaf23Bd848126521064184282e8AD344490BA6f0](https://etherscan.io/address/0xFaf23Bd848126521064184282e8AD344490BA6f0) |
{% endtab %}

{% tab title="Stablecoins" %}
| [Contract](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Address](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)                                    |
|:----------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)     | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)     | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)      | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}
{% endtabs %}

 

