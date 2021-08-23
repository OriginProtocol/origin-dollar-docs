# 레지스트리\(Registry\)

다음은 이더리움\(Ethereum\) 메인 넷 상에 배포 된 OUSD 스마트 컨트렉트의 전체 레지스트리\(registry\) 입니다.

{% hint style="success" %}
오리진달러\(OUSD\) 의 대표 ERC20 주소:  
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

{% tabs %}
{% tab title="Core" %}
잘 알려진 주소  \(흔한 프록시 래퍼 \):

| 컨트렉트 | 주소 | ENS |
| :--- | :--- | :--- |
| OUSD | [0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86](https://etherscan.io/address/0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86) | [ousd.eth](https://etherscan.io/address/ousd.eth) |
| 금고\(Vault\) | [0x277e80f3E14E7fB3fc40A9d6184088e0241034bD](https://etherscan.io/address/0x277e80f3E14E7fB3fc40A9d6184088e0241034bD) | [originvault.eth](https://etherscan.io/address/originvault.eth) |
| 타임락\(Timelock\) | [0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [origintimelock.eth](https://etherscan.io/address/origintimelock.eth) |
| 5/8 멀티시그\(multi-sig\) | [0xe011fA2a6Df98c69383457d87a056Ed0103aA352](https://etherscan.io/address/0xe011fA2a6Df98c69383457d87a056Ed0103aA352) | [originprotocol.eth](https://etherscan.io/address/originprotocol.eth) |
| 오라클 | [0xCf67e56965AD7CEC05eBf88bAd798A875E0460EB](https://etherscan.io/address/0xCf67e56965AD7CEC05eBf88bAd798A875E0460EB) | [originoracle.eth](https://etherscan.io/address/originoracle.eth) |
| Governor | [0x8a5fF78BFe0de04F5dc1B57d2e1095bE697Be76E](https://etherscan.io/address/0x8a5fF78BFe0de04F5dc1B57d2e1095bE697Be76E) | [origingovernor.eth](https://etherscan.io/address/origingovernor.eth) |

내부 실행 컨트랙트:

| 컨트렉트 | 주소 |
| :--- | :--- |
| OUSD | [0xB72b3f5523851C2EB0cA14137803CA4ac7295f3F](https://etherscan.io/address/0xB72b3f5523851C2EB0cA14137803CA4ac7295f3F) |
| VaultAdmin | [0x69A8b2AE6a3606B766Be99C42328459167F51B25](https://etherscan.io/address/0x69A8b2AE6a3606B766Be99C42328459167F51B25) |
| VaultCore | [0x553845F9c44C43224620055eCa64C6cC79f5DdFD](https://etherscan.io/address/0x553845F9c44C43224620055eCa64C6cC79f5DdFD) |
| Mix Oracle | [0xCf67e56965AD7CEC05eBf88bAd798A875E0460EB](https://etherscan.io/address/0xCf67e56965AD7CEC05eBf88bAd798A875E0460EB) |
| Chainlink Oracle | [0x8DE3Ac42F800a1186b6D70CB91e0D6876cC36759](https://etherscan.io/address/0x8DE3Ac42F800a1186b6D70CB91e0D6876cC36759) |
| Open Uniswap Oracle | [0xa8f14F558aC70F5f52C37cD96d802ef9210023C5](https://etherscan.io/address/0xa8f14F558aC70F5f52C37cD96d802ef9210023C5) |
{% endtab %}

{% tab title="Strategies" %}
[Well-known addresses \(proxy wrappers\):](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)

| [Strategy](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Address](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Current Allocation](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| :--- | :--- | :--- |
| [Compound](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0x47211B1D1F6Da45aaEE06f877266E072Cf8BaA74](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [100%](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |

[Internal implementation contracts:](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428)

| [Strategy](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Address](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| :--- | :--- |
| [Compound](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0x5B57e808b0ddCF097e25C5f5E3d8d3c2b0D26319](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}

{% tab title="Stablecoins" %}
| [Contract](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [Address](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| :--- | :--- |
| [USDT](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xdac17f958d2ee523a2206206994597c13d831ec7](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [USDC](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
| [DAI](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) | [0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/address/0x52BEBd3d7f37EC4284853Fd5861Ae71253A7F428) |
{% endtab %}
{% endtabs %}
