# Registry

Here is the full registry of OUSD smart contracts that have been deployed to the Ethereum mainnet.

{% hint style="success" %}
The main ERC20 address for Origin Dollar \(OUSD\) is:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
Well-known addresses \(often proxy wrappers\):

| Contract | Address                                                                                                               | ENS                                                               |
|:-------- |:--------------------------------------------------------------------------------------------------------------------- |:----------------------------------------------------------------- |
| OUSD     | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86) | [ousd.eth](https://etherscan.io/address/ousd.eth)                 |
| Vault    | [0xE75D77B1865Ae93c7eaa3040B038D7aA7BC02F70](https://etherscan.io/address/0xe75d77b1865ae93c7eaa3040b038d7aa7bc02f70) | [originvault.eth](https://etherscan.io/address/originvault.eth)   |
| Oracle   | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4) | [originoracle.eth](https://etherscan.io/address/originoracle.eth) |

Internal implementation contracts. The Vault is split into VaultAdmin and VaultCore to work-around the maximum contract size limit on Ethereum:

| Contract         | Address                                                                                                                    |
|:---------------- |:-------------------------------------------------------------------------------------------------------------------------- |
| OUSD             | [0x8e54f5776ac2d0322d94640e070856a04e446656](https://etherscan.io/address/0x8e54f5776ac2d0322d94640e070856a04e446656#code) |
| VaultAdmin       | [0x84fB09fCb6fc5cc0DBA13FE5CF87A613e34a386a](https://etherscan.io/address/0x84fb09fcb6fc5cc0dba13fe5cf87a613e34a386a)      |
| VaultCore        | [0xE54f14FC3fBc5915D070DE4758bcF591541BD1c3](https://etherscan.io/address/0xe54f14fc3fbc5915d070de4758bcf591541bd1c3)      |
| Mix Oracle       | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4)      |
| Chainlink Oracle | [0x017aD99900b9581Cd40C815990890EE9F0858246](https://etherscan.io/address/0x017aD99900b9581Cd40C815990890EE9F0858246)      |
{% endtab %}

{% tab title="Strategies" %}
Well-known addresses \(proxy wrappers\):

| Strategy | Address                                                                                                               | Current Auto-Allocation |
|:-------- |:--------------------------------------------------------------------------------------------------------------------- |:----------------------- |
| Aave     | [0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce](https://etherscan.io/address/0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce) | 100% of DAI             |
| Compound | [0xD5433168Ed0B1F7714819646606DB509D9d8EC1f](https://etherscan.io/address/0xD5433168Ed0B1F7714819646606DB509D9d8EC1f) | 100% of USDC and USDT   |

Internal implementation contracts:

| Strategy | Address                                                                                                               |
|:-------- |:--------------------------------------------------------------------------------------------------------------------- |
| Aave     | [0xA4144d814F03a2Bb0429CcB89a77Cd3703658B61](https://etherscan.io/address/0xA4144d814F03a2Bb0429CcB89a77Cd3703658B61) |
| Compound | [0x543eDE303EC0Dd9023208d1738681b4cB65256DF](https://etherscan.io/address/0x543eDE303EC0Dd9023208d1738681b4cB65256DF) |
{% endtab %}

{% tab title="Oracles" %}
The following oracles are used to fetch or compute a price for **DAI/USD:**

| Oracle          | Pair    | Contract                                   |
|:--------------- |:------- |:------------------------------------------ |
| Open Price Feed | DAI/USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |
| Chainlink       | DAI/USD | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0 |
| Chainlink       | DAI/ETH | 0x037E8F2125bF532F3e228991e051c8A7253B642c |

The following oracles are used to fetch a price for **USDT/USD:**

| O**racle**      | Pair     | Contract                                   |
|:--------------- |:-------- |:------------------------------------------ |
| Chainlink       | USDT/ETH | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE |
| Open Price Feed | USDC/USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |

The following oracles are used to fetch a price for **USDC/USD:**

| O**racle**      | Pair     | Contract                                   |
|:--------------- |:-------- |:------------------------------------------ |
| Chainlink       | USDC/ETH | 0xdE54467873c3BCAA76421061036053e371721708 |
| Open Price Feed | USDC/USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |

Since not all oracles have direct USD pairs, the protocol also fetches the prices for **ETH/USD** in order to calculate USD prices using ETH. Again, to be safe, the protocol chooses the most advantageous for the fund instead of the individual.

| Oracle          | Pair    | Contract                                   |
|:--------------- |:------- |:------------------------------------------ |
| Open Price Feed | ETH/USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |
| Chainlink       | ETH/USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}

{% tab title="Governance" %}

<table>
  <thead>
    <tr>
      <th style="text-align:left">Contract</th>
      <th style="text-align:left">Address</th>
      <th style="text-align:left">ENS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">5 of 8 Multisig</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xe011fA2a6Df98c69383457d87a056Ed0103aA352">0xe011fA2a6Df98c69383457d87a056Ed0103aA352</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originprotocol.eth">originprotocol.eth</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">2 of 9 Multisig</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC">0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originstrategist.eth">originstrategist.eth</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Governor / Timelock</td>
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
| Contract                                                                        | Address                                                                                                               |
|:------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)  | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}

{% tab title="Staking" %}
| Contract    | Address                                    | ENS                                                                 |
|:----------- |:------------------------------------------ |:------------------------------------------------------------------- |
| OGN Staking | 0x501804B374EF06fa9C427476147ac09F1551B9A0 | [originstaking.eth](https://etherscan.io/address/originstaking.eth) |

Internal implementation contracts:

| Contract    | Address                                                                                                               |
|:----------- |:--------------------------------------------------------------------------------------------------------------------- |
| OGN Staking | [0x8cd68a1e0b79150455c5498882d5d5d3df2dde08](https://etherscan.io/address/0x8cd68a1e0b79150455c5498882d5d5d3df2dde08) |
{% endtab %}
{% endtabs %}



 

