# Địa chỉ các hợp đồng

Đây là bản liệt kê đầy đủ các hợp đồng thông minh OUSD đã được triển khai cho mạng chính Ethereum.

{% hint style="success" %}
Địa chỉ ERC20 chính của Origin Dollar \ (OUSD \) là:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
Địa chỉ phổ biến

| Hợp đồng | Địa chỉ                                                                                                               | ENS                                                               |
|:-------- |:--------------------------------------------------------------------------------------------------------------------- |:----------------------------------------------------------------- |
| OUSD     | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86) | [ousd.eth](https://etherscan.io/address/ousd.eth)                 |
| Vault    | [0xE75D77B1865Ae93c7eaa3040B038D7aA7BC02F70](https://etherscan.io/address/0xe75d77b1865ae93c7eaa3040b038d7aa7bc02f70) | [originvault.eth](https://etherscan.io/address/originvault.eth)   |
| Oracle   | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4) | [originoracle.eth](https://etherscan.io/address/originoracle.eth) |

Các hợp đồng thực hiện nội bộ. Vault được chia thành VaultAdmin và VaultCore để giải quyết giới hạn kích thước hợp đồng tối đa trên Ethereum:

| Hợp đồng         | Địa chỉ                                                                                                               |
|:---------------- |:--------------------------------------------------------------------------------------------------------------------- |
| OUSD             | [0x23DCc0Cc5F08b9D85daF8d29490c7f74a655b359](https://etherscan.io/address/0x23DCc0Cc5F08b9D85daF8d29490c7f74a655b359) |
| VaultAdmin       | [0x8E55b527901BC88206a1cE5C292B2404bcb8F76D](https://etherscan.io/address/0x8e55b527901bc88206a1ce5c292b2404bcb8f76d) |
| VaultCore        | [0xA4D15507112c0DB37E1320Bf3Fff8891DFd1D2Ed](https://etherscan.io/address/0xA4D15507112c0DB37E1320Bf3Fff8891DFd1D2Ed) |
| Oracle kết hợp   | [0x843530DC8005e13dEA30CEa2394FF60635f38cc4](https://etherscan.io/address/0x843530DC8005e13dEA30CEa2394FF60635f38cc4) |
| Chainlink Oracle | [0x017aD99900b9581Cd40C815990890EE9F0858246](https://etherscan.io/address/0x017aD99900b9581Cd40C815990890EE9F0858246) |
{% endtab %}

{% tab title="Strategies" %}
Địa chỉ phổ biến \(proxy wrappers\):

| Chiến lược  | Địa chỉ                                                                                                               | Tự động phân bổ   |
|:----------- |:--------------------------------------------------------------------------------------------------------------------- |:----------------- |
| Aave        | [0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce](https://etherscan.io/address/0x9f2b18751376cF6a3432eb158Ba5F9b1AbD2F7ce) | 100% DAI          |
| Compound    | [0xD5433168Ed0B1F7714819646606DB509D9d8EC1f](https://etherscan.io/address/0xD5433168Ed0B1F7714819646606DB509D9d8EC1f) | 100% USDC và USDT |
| Curve 3Pool | [0x3c5fe0a3922777343CBD67D3732FCdc9f2Fa6f2F](https://etherscan.io/address/0x3c5fe0a3922777343CBD67D3732FCdc9f2Fa6f2F) | Phân bổ thủ công  |

Các hợp đồng thực hiện nội bộ:

| Chiến lược  | Địa chỉ                                                                                                               |
|:----------- |:--------------------------------------------------------------------------------------------------------------------- |
| Aave        | [0xd97fE382b923F75Ab8951915eCF07CBf12c102D4](https://etherscan.io/address/0xd97fE382b923F75Ab8951915eCF07CBf12c102D4) |
| Compound    | [0x3a2c387b84b28F438aaF53e6d0B8e790D084D1d1](https://etherscan.io/address/0x3a2c387b84b28F438aaF53e6d0B8e790D084D1d1) |
| Curve 3Pool | [0x9F2E2b1c5F6Ac748b61f07e88f912A1df33Dfe55](https://etherscan.io/address/0x9F2E2b1c5F6Ac748b61f07e88f912A1df33Dfe55) |
{% endtab %}

{% tab title="Oracles" %}
Các oracle sau được sử dụng để tìm nạp hoặc tính giá cho **DAI/USD:**

| Oracle    | Cặp     | Hợp đồng                                                                                                              |
|:--------- |:------- |:--------------------------------------------------------------------------------------------------------------------- |
| Chainlink | DAI/USD | [0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9](https://etherscan.io/address/0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9) |

Các oracle sau được sử dụng để định giá **USDT/USD:**

| O**racle** | Cặp      | Hợp đồng                                                                                                              |
|:---------- |:-------- |:--------------------------------------------------------------------------------------------------------------------- |
| Chainlink  | USDT/USD | [0x3E7d1eAB13ad0104d2750B8863b489D65364e32D](https://etherscan.io/address/0x3E7d1eAB13ad0104d2750B8863b489D65364e32D) |

Các oracle sau được sử dụng để định giá **USDT/USD:**

| O**racle** | Cặp      | Hợp đồng                                                                                                              |
|:---------- |:-------- |:--------------------------------------------------------------------------------------------------------------------- |
| Chainlink  | USDC/USD | [0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6](https://etherscan.io/address/0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6) |
{% endtab %}

{% tab title="Governance" %}

<table>
  <thead>
    <tr>
      <th style="text-align:left">Hợp đồng</th>
      <th style="text-align:left">Địa chỉ</th>
      <th style="text-align:left">ENS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">5 trên 8 chữ ký</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xbe2AB3d3d8F6a32b96414ebbd865dBD276d3d899">0xbe2AB3d3d8F6a32b96414ebbd865dBD276d3d899</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originprotocol.eth">originprotocol.eth</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">2 trên 9 chữ ký</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC">0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/originstrategist.eth">originstrategist.eth</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Quản trị viên / Khoá thời gian</td>
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
| Hợp đồng                                                                        | Address                                                                                                               |
|:------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------------- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)  | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}

{% tab title="Staking" %}
| Hợp đồng  | Địa chỉ                                                                                                               | ENS                                                                 |
|:--------- |:--------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------------- |
| Stake OGN | [0x501804B374EF06fa9C427476147ac09F1551B9A0](https://etherscan.io/address/0x501804B374EF06fa9C427476147ac09F1551B9A0) | [originstaking.eth](https://etherscan.io/address/originstaking.eth) |

Các hợp đồng thực hiện nội bộ:

| Hợp đồng  | Địa chỉ                                                                                                               |
|:--------- |:--------------------------------------------------------------------------------------------------------------------- |
| Stake OGN | [0x8cd68a1e0b79150455c5498882d5d5d3df2dde08](https://etherscan.io/address/0x8cd68a1e0b79150455c5498882d5d5d3df2dde08) |

Hợp đồng bồi thường OUSD \ ([chi tiết](https://medium.com/originprotocol/origin-delivers-on-compensation-promise-claim-your-ousd-and-ogn-now-a9fa9b840476)\):

| Hợp đồng        | Địa chỉ                                                                                                               |
|:--------------- |:--------------------------------------------------------------------------------------------------------------------- |
| Bồi thường OUSD | [0x9C94df9d594BA1eb94430C006c269C314B1A8281](https://etherscan.io/address/0x9C94df9d594BA1eb94430C006c269C314B1A8281) |
{% endtab %}

{% tab title="Swap" %}
| Contract | Address                                                                                                               | ENS                                                           |
|:-------- |:--------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------- |
| Swap     | [0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70](https://etherscan.io/address/0xcecaD69d7D4Ed6D52eFcFA028aF8732F27e08F70) | [originswap.eth](https://etherscan.io/address/originswap.eth) |
{% endtab %}
{% endtabs %}



 

