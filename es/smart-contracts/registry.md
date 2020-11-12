# Registro

Aquí está el registro completo de los contratos inteligentes de OUSD que se han implementado en la red principal de Ethereum.

{% hint style="success" %}
La dirección ERC20 principal para Origin Dollar \(OUSD\) es:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
Direcciones conocidas \ (a menudo envoltorios de proxy\):

| Contrato                | Dirección                                                                                                             | ENS                                                                   |
|:----------------------- |:--------------------------------------------------------------------------------------------------------------------- |:--------------------------------------------------------------------- |
| OUSD                    | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86) | [ousd.eth](https://etherscan.io/address/ousd.eth)                     |
| Bóveda                  | [0x277e80f3E14E7fB3fc40A9d6184088e0241034bD](https://etherscan.io/address/0x277e80f3E14E7fB3fc40A9d6184088e0241034bD) | [originvault.eth](https://etherscan.io/address/originvault.eth)       |
| Bloqueo de Tiempo       | [0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [origintimelock.eth](https://etherscan.io/address/origintimelock.eth) |
| 5 de 8 Multiples-firmas | [0xe011fA2a6Df98c69383457d87a056Ed0103aA352](https://etherscan.io/address/0xe011fA2a6Df98c69383457d87a056Ed0103aA352) | [originprotocol.eth](https://etherscan.io/address/originprotocol.eth) |
| Oráculo                 | [0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458](https://etherscan.io/address/0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458) | [originoracle.eth](https://etherscan.io/address/originoracle.eth)     |
| Gobernador              | [0x8a5fF78BFe0de04F5dc1B57d2e1095bE697Be76E](https://etherscan.io/address/0x8a5fF78BFe0de04F5dc1B57d2e1095bE697Be76E) | [origingovernor.eth](https://etherscan.io/address/origingovernor.eth) |

Contratos de ejecución interna:

| Contrato                   | Dirección                                                                                                             |
|:-------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| OUSD                       | [0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805](https://etherscan.io/address/0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805) |
| Administrador de la Bóveda | [0xfbbe3090E06721168979818Fe006A1fcb136e953](https://etherscan.io/address/0xfbbe3090E06721168979818Fe006A1fcb136e953) |
| Bóveda Central             | [0xB95423e3ca13ce5336Cb177B06cD4f647D2aAd57](https://etherscan.io/address/0xB95423e3ca13ce5336Cb177B06cD4f647D2aAd57) |
| Oráculos Mixtos            | [0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458](https://etherscan.io/address/0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458) |
| Oráculo de Chainlink       | [0x8DE3Ac42F800a1186b6D70CB91e0D6876cC36759](https://etherscan.io/address/0x8DE3Ac42F800a1186b6D70CB91e0D6876cC36759) |
| Oráculo Abierto de Uniswap | [0xa8f14F558aC70F5f52C37cD96d802ef9210023C5](https://etherscan.io/address/0xa8f14F558aC70F5f52C37cD96d802ef9210023C5) |
{% endtab %}

{% tab title="Strategies" %}
[Direcciones conocidas \ (a menudo envoltorios de proxy\):](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)

| [Estrategia](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Dirección](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)                                  | [Current Auto-Allocation](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
|:------------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |:-------------------------------------------------------------------------------------------------- |
| Curve \(USDT\)                                                                      | [0xe40e09cD6725E542001FcB900d9dfeA447B529C0](https://etherscan.io/address/0xe40e09cD6725E542001FcB900d9dfeA447B529C0) | 0%                                                                                                 |
| Curve \(USDC\)                                                                      | [0x67023c56548BA15aD3542E65493311F19aDFdd6d](https://etherscan.io/address/0x67023c56548BA15aD3542E65493311F19aDFdd6d) | 0%                                                                                                 |
| Aave                                                                                  | [0x051CaEFA90aDf261B8E8200920C83778b7B176B6](https://etherscan.io/address/0x051caefa90adf261b8e8200920c83778b7b176b6) | 100% of DAI                                                                                        |
| Compound                                                                              | [0x12115A32a19e4994C2BA4A5437C22CEf5ABb59C3](https://etherscan.io/address/0x12115A32a19e4994C2BA4A5437C22CEf5ABb59C3) | 100% of USDC and USDT                                                                              |

[Contratos de ejecución interna:](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)

| [Estrategia](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Dirección](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)                                  |
|:------------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| Curve \(USDT\)                                                                      | [0x641E3b5b081Fb2fb8B43D5a163649312a28e23Da](https://etherscan.io/address/0x641E3b5b081Fb2fb8B43D5a163649312a28e23Da) |
| Curve \(USDC\)                                                                      | [0xF92B0DE25660C18BEDaa55795986781d7899b0f9](https://etherscan.io/address/0xF92B0DE25660C18BEDaa55795986781d7899b0f9) |
| Aave                                                                                  | [0x5d9aA9f977E47eA0BFE61BA8b8f535aba02Be135](https://etherscan.io/address/0x5d9aA9f977E47eA0BFE61BA8b8f535aba02Be135) |
| Compound                                                                              | [0xFaf23Bd848126521064184282e8AD344490BA6f0](https://etherscan.io/address/0xFaf23Bd848126521064184282e8AD344490BA6f0) |
{% endtab %}

{% tab title="Stablecoins" %}
| [Contrato](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Dirección](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)                                  |
|:----------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)     | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)     | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)      | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}
{% endtabs %}

 

