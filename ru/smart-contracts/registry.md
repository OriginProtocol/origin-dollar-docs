# Реестр

Вот полный реестр смарт-контрактов OUSD, которые были развернуты в основной сети Ethereum.

{% hint style="success" %}
Основной адрес ERC20 для Origin Dollar \(OUSD \):   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
Общеизвестные адреса \(часто используемые прокси оболочки\):

| Контракт              | Адрес                                                                                                                 | ENS                                                                   |
|:--------------------- |:--------------------------------------------------------------------------------------------------------------------- |:--------------------------------------------------------------------- |
| OUSD                  | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86) | [ousd.eth](https://etherscan.io/address/ousd.eth)                     |
| Хранилище (Vault)     | [0x277e80f3E14E7fB3fc40A9d6184088e0241034bD](https://etherscan.io/address/0x277e80f3E14E7fB3fc40A9d6184088e0241034bD) | [originvault.eth](https://etherscan.io/address/originvault.eth)       |
| Временная блокировка  | [0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [origintimelock.eth](https://etherscan.io/address/origintimelock.eth) |
| 5 из 8 мультиподписей | [0xe011fA2a6Df98c69383457d87a056Ed0103aA352](https://etherscan.io/address/0xe011fA2a6Df98c69383457d87a056Ed0103aA352) | [originprotocol.eth](https://etherscan.io/address/originprotocol.eth) |
| Оракул                | [0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458](https://etherscan.io/address/0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458) | [originoracle.eth](https://etherscan.io/address/originoracle.eth)     |
| Управляющий           | [0x8a5fF78BFe0de04F5dc1B57d2e1095bE697Be76E](https://etherscan.io/address/0x8a5fF78BFe0de04F5dc1B57d2e1095bE697Be76E) | [origingovernor.eth](https://etherscan.io/address/origingovernor.eth) |

Контракты на внутреннюю реализацию:

| Контракт               | Адрес                                                                                                                 |
|:---------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| OUSD                   | [0xB72b3f5523851C2EB0cA14137803CA4ac7295f3F](https://etherscan.io/address/0xB72b3f5523851C2EB0cA14137803CA4ac7295f3F) |
| АдминистраторVault     | [0x69A8b2AE6a3606B766Be99C42328459167F51B25](https://etherscan.io/address/0x69A8b2AE6a3606B766Be99C42328459167F51B25) |
| ЯдроХранилища          | [0x553845F9c44C43224620055eCa64C6cC79f5DdFD](https://etherscan.io/address/0x553845F9c44C43224620055eCa64C6cC79f5DdFD) |
| Смешанные Оракулы      | [0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458](https://etherscan.io/address/0x4d4f5e7a1FE57F5cEB38BfcE8653EFFa5e584458) |
| Оракул Chainlink       | [0x8DE3Ac42F800a1186b6D70CB91e0D6876cC36759](https://etherscan.io/address/0x8DE3Ac42F800a1186b6D70CB91e0D6876cC36759) |
| Открыть Оракул Uniswap | [0xa8f14F558aC70F5f52C37cD96d802ef9210023C5](https://etherscan.io/address/0xa8f14F558aC70F5f52C37cD96d802ef9210023C5) |
{% endtab %}

{% tab title="Strategies" %}
[Общеизвестные адреса \(прокси оболочки\):](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)

| [Стратегия](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)    | [Адрес](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)                                      | [Текущая аллокация](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
|:--------------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |:-------------------------------------------------------------------------------------------- |
| [Накапливание](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0x47211B1D1F6Da45aaEE06f877266E072Cf8BaA74](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [100%](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)              |

[Контракты на внутреннюю реализацию:](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)

| [Стратегия](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)    | [Адрес](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)                                      |
|:--------------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| [Накапливание](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0x5B57e808b0ddCF097e25C5f5E3d8d3c2b0D26319](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}

{% tab title="Stablecoins" %}
| [Контракт](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Адрес](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)                                      |
|:----------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)     | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)     | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)      | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}
{% endtabs %}





 

