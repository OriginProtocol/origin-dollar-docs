# Registry

Here is the full registry of OUSD smart contracts that have been deployed to the Ethereum mainnet.

{% hint style="success" %}
The main ERC20 address for Origin Dollar \(OUSD\) is:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
Well-known addresses \(often proxy wrappers\):

| Contract | Address | ENS |
| :--- | :--- | :--- |
| OUSD | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)  | [ousd.eth](https://etherscan.io/address/ousd.eth) |
| Vault | [0xE75D77B1865Ae93c7eaa3040B038D7aA7BC02F70](https://etherscan.io/address/0xe75d77b1865ae93c7eaa3040b038d7aa7bc02f70) | [originvault.eth](https://etherscan.io/address/originvault.eth) |
| Oracle | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4) | [originoracle.eth](https://etherscan.io/address/originoracle.eth) |

Internal implementation contracts. The Vault is split into VaultAdmin and VaultCore to work-around the maximum contract size limit on Ethereum:

| Contract | Address |
| :--- | :--- |
| OUSD | [0x9d6975591E777D95Eef3bCC2a727846DA25d7083](https://etherscan.io/address/0x9d6975591E777D95Eef3bCC2a727846DA25d7083) |
| VaultAdmin | [0xb5f7E47Bc7D271b3df4824BDcFBB279a719F8Ae6](https://etherscan.io/address/0xb5f7E47Bc7D271b3df4824BDcFBB279a719F8Ae6) |
| VaultCore | [0xE54f14FC3fBc5915D070DE4758bcF591541BD1c3](https://etherscan.io/address/0xe54f14fc3fbc5915d070de4758bcf591541bd1c3) |
| Mix Oracle | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4) |
| Chainlink Oracle | [0x017aD99900b9581Cd40C815990890EE9F0858246](https://etherscan.io/address/0x017aD99900b9581Cd40C815990890EE9F0858246) |
{% endtab %}

{% tab title="Strategies" %}
Well-known addresses \(proxy wrappers\):

| Strategy | Address | Auto-Allocation |
| :--- | :--- | :--- |
| Aave | [0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce](https://etherscan.io/address/0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce) | 100% of DAI |
| Compound | [0xD5433168Ed0B1F7714819646606DB509D9d8EC1f](https://etherscan.io/address/0xD5433168Ed0B1F7714819646606DB509D9d8EC1f) | 100% of USDC and USDT |
| Curve 3Pool | [0x3c5fe0a3922777343CBD67D3732FCdc9f2Fa6f2F](https://etherscan.io/address/0x3c5fe0a3922777343CBD67D3732FCdc9f2Fa6f2F) | Manual allocation |

Internal implementation contracts:

| Strategy | Address |
| :--- | :--- |
| Aave | [0xd97fE382b923F75Ab8951915eCF07CBf12c102D4](https://etherscan.io/address/0xd97fE382b923F75Ab8951915eCF07CBf12c102D4) |
| Compound | [0x3a2c387b84b28F438aaF53e6d0B8e790D084D1d1](https://etherscan.io/address/0x3a2c387b84b28F438aaF53e6d0B8e790D084D1d1) |
| Curve 3Pool | [0x9F2E2b1c5F6Ac748b61f07e88f912A1df33Dfe55](https://etherscan.io/address/0x9F2E2b1c5F6Ac748b61f07e88f912A1df33Dfe55) |
{% endtab %}

{% tab title="Oracles" %}
The following oracles are used to fetch or compute a price for **DAI/USD:**

| Oracle | Pair | Contract |
| :--- | :--- | :--- |
| Chainlink | DAI/USD | [0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9](https://etherscan.io/address/0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9) |

The following oracles are used to fetch a price for **USDT/USD:**

| O**racle** | Pair | Contract |
| :--- | :--- | :--- |
| Chainlink | USDT/USD | [0x3E7d1eAB13ad0104d2750B8863b489D65364e32D](https://etherscan.io/address/0x3E7d1eAB13ad0104d2750B8863b489D65364e32D) |

The following oracles are used to fetch a price for **USDC/USD:**

| O**racle** | Pair | Contract |
| :--- | :--- | :--- |
| Chainlink | USDC/USD | [0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6](https://etherscan.io/address/0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6) |
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
    <tr>
      <td style="text-align:left">OGN Buyback</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x7294CD3C3eb4097b03E1A61EB2AD280D3dD265e6">0x7294CD3C3eb4097b03E1A61EB2AD280D3dD265e6</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originbuyback.eth">originbuyback.eth</a>
      </td>
    </tr>
  </tbody>
</table>
{% endtab %}

{% tab title="Stablecoins" %}
| Contract | Address |
| :--- | :--- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}

{% tab title="Staking" %}
| Contract | Address | ENS |
| :--- | :--- | :--- |
| OGN Staking | [0x501804B374EF06fa9C427476147ac09F1551B9A0](https://etherscan.io/address/0x501804B374EF06fa9C427476147ac09F1551B9A0) | [originstaking.eth](https://etherscan.io/address/originstaking.eth) |

Internal implementation contracts:

| Contract | Address |
| :--- | :--- |
| OGN Staking | [0x8cd68a1e0b79150455c5498882d5d5d3df2dde08](https://etherscan.io/address/0x8cd68a1e0b79150455c5498882d5d5d3df2dde08) |
{% endtab %}

{% tab title="Compensation" %}
| Contract | Address |
| :--- | :--- |
| OUSD Compensation | [0x9C94df9d594BA1eb94430C006c269C314B1A8281](https://etherscan.io/address/0x9C94df9d594BA1eb94430C006c269C314B1A8281) |
{% endtab %}

{% tab title="Swap" %}
| Contract | Address | ENS |
| :--- | :--- | :--- |
| Swap | [0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70](https://etherscan.io/address/0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70) | [originswap.eth](https://etherscan.io/address/originswap.eth) |
{% endtab %}
{% endtabs %}



 

