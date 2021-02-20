# Реестр

Вот полный реестр смарт-контрактов OUSD, которые были развернуты в основной сети Ethereum.

{% hint style="success" %}
Основной адрес ERC20 для Origin Dollar \(OUSD \):   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
Общеизвестные адреса \(часто используемые прокси оболочки\):

| Контракт          | Адрес                                                                                                                 | ENS                                                               |
|:----------------- |:--------------------------------------------------------------------------------------------------------------------- |:----------------------------------------------------------------- |
| OUSD              | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86) | [ousd.eth](https://etherscan.io/address/ousd.eth)                 |
| Хранилище (Vault) | [0xE75D77B1865Ae93c7eaa3040B038D7aA7BC02F70](https://etherscan.io/address/0xe75d77b1865ae93c7eaa3040b038d7aa7bc02f70) | [originvault.eth](https://etherscan.io/address/originvault.eth)   |
| Оракул            | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4) | [originoracle.eth](https://etherscan.io/address/originoracle.eth) |

Контракты на внутреннюю реализацию. Хранилище разделено на VaultAdmin и VaultCore, чтобы обойти ограничение максимального размера контракта на Ethereum:

| Контракт          | Адрес                                                                                                                 |
|:----------------- |:--------------------------------------------------------------------------------------------------------------------- |
| OUSD              | [0x9d6975591E777D95Eef3bCC2a727846DA25d7083](https://etherscan.io/address/0x9d6975591E777D95Eef3bCC2a727846DA25d7083) |
| VaultAdmin        | [0xb5f7E47Bc7D271b3df4824BDcFBB279a719F8Ae6](https://etherscan.io/address/0xb5f7E47Bc7D271b3df4824BDcFBB279a719F8Ae6) |
| ЯдроХранилища     | [0xE54f14FC3fBc5915D070DE4758bcF591541BD1c3](https://etherscan.io/address/0xe54f14fc3fbc5915d070de4758bcf591541bd1c3) |
| Смешанные Оракулы | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4) |
| Оракул Chainlink  | [0x017aD99900b9581Cd40C815990890EE9F0858246](https://etherscan.io/address/0x017aD99900b9581Cd40C815990890EE9F0858246) |
{% endtab %}

{% tab title="Strategies" %}
Общеизвестные адреса \(прокси оболочки\):

| Стратегия   | Адрес                                                                                                                 | Auto-Allocation              |
|:----------- |:--------------------------------------------------------------------------------------------------------------------- |:---------------------------- |
| Aave        | [0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce](https://etherscan.io/address/0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce) | 100% DAI                     |
| Compound    | [0xD5433168Ed0B1F7714819646606DB509D9d8EC1f](https://etherscan.io/address/0xD5433168Ed0B1F7714819646606DB509D9d8EC1f) | 100% USDC и USDT             |
| Curve 3Pool | [0x3c5fe0a3922777343CBD67D3732FCdc9f2Fa6f2F](https://etherscan.io/address/0x3c5fe0a3922777343CBD67D3732FCdc9f2Fa6f2F) | Аллокация выбирается вручную |

Контракты на внутреннюю реализацию:

| Стратегия   | Адрес                                                                                                                 |
|:----------- |:--------------------------------------------------------------------------------------------------------------------- |
| Aave        | [0xd97fE382b923F75Ab8951915eCF07CBf12c102D4](https://etherscan.io/address/0xd97fE382b923F75Ab8951915eCF07CBf12c102D4) |
| Compound    | [0x3a2c387b84b28F438aaF53e6d0B8e790D084D1d1](https://etherscan.io/address/0x3a2c387b84b28F438aaF53e6d0B8e790D084D1d1) |
| Curve 3Pool | [0x9F2E2b1c5F6Ac748b61f07e88f912A1df33Dfe55](https://etherscan.io/address/0x9F2E2b1c5F6Ac748b61f07e88f912A1df33Dfe55) |
{% endtab %}

{% tab title="Oracles" %}
Следующие оракулы используются для получения или вычисления цены **DAI/USD:**

| Оракул                   | Пара    | Контракт                                   |
|:------------------------ |:------- |:------------------------------------------ |
| Открытый поток котировок | DAI/USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |
| Chainlink                | DAI/USD | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0 |
| Chainlink                | DAI/ETH | 0x037E8F2125bF532F3e228991e051c8A7253B642c |

Следующие оракулы используются для извлечения или вычисления цены **USDT/USD:**

| **Оракул**               | Пара     | Контракт                                   |
|:------------------------ |:-------- |:------------------------------------------ |
| Chainlink                | USDT/ETH | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE |
| Открытый поток котировок | USDC/USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |

Следующие оракулы используются для извлечения или вычисления цены **USDC/USD:**

| **Оракул**               | Пара     | Контракт                                   |
|:------------------------ |:-------- |:------------------------------------------ |
| Chainlink                | USDC/ETH | 0xdE54467873c3BCAA76421061036053e371721708 |
| Открытый поток котировок | USDC/USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |

Поскольку не все оракулы имеют прямые пары с долларом США, протокол также извлекает цены для **ETH/USD**, чтобы рассчитать цены в долларах США с использованием ETH. Опять же, на всякий случай протокол выбирает наиболее выгодный для фонда, а не для отдельных персон.

| Оракул                   | Пара    | Контракт                                   |
|:------------------------ |:------- |:------------------------------------------ |
| Открытый поток котировок | ETH/USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |
| Chainlink                | ETH/USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}

{% tab title="Governance" %}

<table>
  <thead>
    <tr>
      <th style="text-align:left">Контракт</th>
      <th style="text-align:left">Адрес</th>
      <th style="text-align:left">ENS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">5 из 8 мультиподписей</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xe011fA2a6Df98c69383457d87a056Ed0103aA352">0xe011fA2a6Df98c69383457d87a056Ed0103aA352</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originprotocol.eth">originprotocol.eth</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">2 из 9 мультиподписей</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC">0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originstrategist.eth">originstrategist.eth</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Регулятор / Временная блокировка</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x8e7bDFeCd1164C46ad51b58e49A611F954D23377">0x8e7bDFeCd1164C46ad51b58e49A611F954D23377</a>
      </td>
      <td style="text-align:left">
        <p><a href="https://etherscan.io/address/origingovernor.eth">origingovernor.eth</a>
        </p>
        <p><a href="https://etherscan.io/address/origintimelock.eth">origintimelock.eth</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>
{% endtab %}

{% tab title="Stablecoins" %}
| Контракт                                                                        | Адрес                                                                                                                 |
|:------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)  | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}

{% tab title="Staking" %}
| Контракт             | Адрес                                                                                                                 | ENS                                                                 |
|:-------------------- |:--------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------------- |
| Стейкинг токенов OGN | [0x501804B374EF06fa9C427476147ac09F1551B9A0](https://etherscan.io/address/0x501804B374EF06fa9C427476147ac09F1551B9A0) | [originstaking.eth](https://etherscan.io/address/originstaking.eth) |

Контракты на внутреннюю реализацию:

| Контракт             | Адрес                                                                                                                 |
|:-------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| Стейкинг токенов OGN | [0x8cd68a1e0b79150455c5498882d5d5d3df2dde08](https://etherscan.io/address/0x8cd68a1e0b79150455c5498882d5d5d3df2dde08) |
{% endtab %}

{% tab title="Compensation" %}
| Контракт         | Адрес                                                                                                                 |
|:---------------- |:--------------------------------------------------------------------------------------------------------------------- |
| Компенсация OUSD | [0x9C94df9d594BA1eb94430C006c269C314B1A8281](https://etherscan.io/address/0x9C94df9d594BA1eb94430C006c269C314B1A8281) |
{% endtab %}

{% tab title="Swap" %}
| Contract | Address                                                                                                               | ENS                                                           |
|:-------- |:--------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------- |
| Swap     | [0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70](https://etherscan.io/address/0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70) | [originswap.eth](https://etherscan.io/address/originswap.eth) |
{% endtab %}
{% endtabs %}



 

