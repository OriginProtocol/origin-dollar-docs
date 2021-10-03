# Registro

Aquí está el registro completo de los contratos inteligentes de OUSD que se han implementado en la red principal de Ethereum.

{% hint style="success" %}
La dirección ERC20 principal para Origin Dollar \(OUSD\) es:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
Direcciones conocidas \ (a menudo envoltorios de proxy\):

| Contrato | Dirección                                                                                                             | ENS                                                               |
|:-------- |:--------------------------------------------------------------------------------------------------------------------- |:----------------------------------------------------------------- |
| OUSD     | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86) | [ousd.eth](https://etherscan.io/address/ousd.eth)                 |
| Bóveda   | [0xE75D77B1865Ae93c7eaa3040B038D7aA7BC02F70](https://etherscan.io/address/0xe75d77b1865ae93c7eaa3040b038d7aa7bc02f70) | [originvault.eth](https://etherscan.io/address/originvault.eth)   |
| Oráculo  | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4) | [originoracle.eth](https://etherscan.io/address/originoracle.eth) |

Contratos de ejecución interna. El bóveda se divide en VaultAdmin y VaultCore para solucionar el límite máximo de tamaño de contrato en Ethereum:

| Contrato                   | Dirección                                                                                                             |
|:-------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| OUSD                       | [0x23DCc0Cc5F08b9D85daF8d29490c7f74a655b359](https://etherscan.io/address/0x23DCc0Cc5F08b9D85daF8d29490c7f74a655b359) |
| Administrador de la Bóveda | [0x8E55b527901BC88206a1cE5C292B2404bcb8F76D](https://etherscan.io/address/0x8e55b527901bc88206a1ce5c292b2404bcb8f76d) |
| Bóveda Central             | [0xA4D15507112c0DB37E1320Bf3Fff8891DFd1D2Ed](https://etherscan.io/address/0xA4D15507112c0DB37E1320Bf3Fff8891DFd1D2Ed) |
| Oráculos Mixtos            | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4) |
| Oráculo de Chainlink       | [0x017aD99900b9581Cd40C815990890EE9F0858246](https://etherscan.io/address/0x017aD99900b9581Cd40C815990890EE9F0858246) |
{% endtab %}

{% tab title="Strategies" %}
Direcciones conocidas \(envoltorios de proxy\):

| Estrategia  | Dirección                                                                                                             | Asignación automática |
|:----------- |:--------------------------------------------------------------------------------------------------------------------- |:--------------------- |
| Aave        | [0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce](https://etherscan.io/address/0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce) | 100% de DAI           |
| Compound    | [0xD5433168Ed0B1F7714819646606DB509D9d8EC1f](https://etherscan.io/address/0xD5433168Ed0B1F7714819646606DB509D9d8EC1f) | 100% de USDC y USDT   |
| Curve 3Pool | [0x3c5fe0a3922777343CBD67D3732FCdc9f2Fa6f2F](https://etherscan.io/address/0x3c5fe0a3922777343CBD67D3732FCdc9f2Fa6f2F) | Asignación manual     |

Contratos de ejecución interna:

| Estrategia  | Dirección                                                                                                             |
|:----------- |:--------------------------------------------------------------------------------------------------------------------- |
| Aave        | [0xd97fE382b923F75Ab8951915eCF07CBf12c102D4](https://etherscan.io/address/0xd97fE382b923F75Ab8951915eCF07CBf12c102D4) |
| Compound    | [0x3a2c387b84b28F438aaF53e6d0B8e790D084D1d1](https://etherscan.io/address/0x3a2c387b84b28F438aaF53e6d0B8e790D084D1d1) |
| Curve 3Pool | [0x9F2E2b1c5F6Ac748b61f07e88f912A1df33Dfe55](https://etherscan.io/address/0x9F2E2b1c5F6Ac748b61f07e88f912A1df33Dfe55) |
{% endtab %}

{% tab title="Oracles" %}
Los siguientes oráculos se utilizan para obtener o calcular un precio de **DAI/USD:**

| Oráculo   | Par     | Contrato                                                                                                              |
|:--------- |:------- |:--------------------------------------------------------------------------------------------------------------------- |
| Chainlink | DAI/USD | [0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9](https://etherscan.io/address/0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9) |

Los siguientes oráculos se utilizan para obtener o calcular un precio de **USDT/USD:**

| **Oráculo** | Par      | Contrato                                                                                                              |
|:----------- |:-------- |:--------------------------------------------------------------------------------------------------------------------- |
| Chainlink   | USDT/USD | [0x3E7d1eAB13ad0104d2750B8863b489D65364e32D](https://etherscan.io/address/0x3E7d1eAB13ad0104d2750B8863b489D65364e32D) |

Los siguientes oráculos se utilizan para obtener o calcular un precio de **USDC/USD:**

| **Oráculo** | Par      | Contrato                                                                                                              |
|:----------- |:-------- |:--------------------------------------------------------------------------------------------------------------------- |
| Chainlink   | USDC/USD | [0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6](https://etherscan.io/address/0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6) |
{% endtab %}

{% tab title="Governance" %}

<table>
  <thead>
    <tr>
      <th style="text-align:left">Contrato</th>
      <th style="text-align:left">Dirección</th>
      <th style="text-align:left">ENS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">5 de 8 Multiples-firmas</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xbe2AB3d3d8F6a32b96414ebbd865dBD276d3d899">0xbe2AB3d3d8F6a32b96414ebbd865dBD276d3d899</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originprotocol.eth">originprotocol.eth</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">2 de 9 Multiples-firmas</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC">0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originstrategist.eth">originstrategist.eth</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Gobernador / Timelock</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x830622bdd79cc677ee6594e20bbda5b26568b781">0x830622BDd79CC677eE6594E20bBda5B26568b781</a>
      </td>
      <td style="text-align:left">
        <p><a href="https://etherscan.io/address/origingovernor.eth">origingovernor.eth</a>
        </p>
        <p><a href="https://etherscan.io/address/origintimelock.eth">origintimelock.eth</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Recompra de OGN</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x7294CD3C3eb4097b03E1A61EB2AD280D3dD265e6">0x7294CD3C3eb4097b03E1A61EB2AD280D3dD265e6</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originbuyback.eth">originbuyback.eth</a>
      </td>
    </tr>
  </tbody>
</table>
{% endtab %}

{% tab title="Stablecoins" %}
| Contrato                                                                        | Dirección                                                                                                             |
|:------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)  | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}

{% tab title="Staking" %}
| Contrato       | Dirección                                                                                                             | ENS                                                                 |
|:-------------- |:--------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------------- |
| Staking de OGN | [0x501804B374EF06fa9C427476147ac09F1551B9A0](https://etherscan.io/address/0x501804B374EF06fa9C427476147ac09F1551B9A0) | [originstaking.eth](https://etherscan.io/address/originstaking.eth) |

Contratos de ejecución interna:

| Contrato       | Dirección                                                                                                             |
|:-------------- |:--------------------------------------------------------------------------------------------------------------------- |
| Staking de OGN | [0x8cd68a1e0b79150455c5498882d5d5d3df2dde08](https://etherscan.io/address/0x8cd68a1e0b79150455c5498882d5d5d3df2dde08) |

Contrato de compensación OUSD \([detalles](https://medium.com/originprotocol/origin-delivers-on-compensation-promise-claim-your-ousd-and-ogn-now-a9fa9b840476)\):

| Contrato             | Dirección                                                                                                             |
|:-------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| Compensación de OUSD | [0x9C94df9d594BA1eb94430C006c269C314B1A8281](https://etherscan.io/address/0x9C94df9d594BA1eb94430C006c269C314B1A8281) |
{% endtab %}

{% tab title="Swap" %}
| Contrato | Dirección                                                                                                             | ENS                                                           |
|:-------- |:--------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------- |
| Canjeo   | [0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70](https://etherscan.io/address/0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70) | [originswap.eth](https://etherscan.io/address/originswap.eth) |
{% endtab %}
{% endtabs %}



 

