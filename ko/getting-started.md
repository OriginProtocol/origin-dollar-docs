# 시작하기

이 문서는 OUSD의 작동 방식을 설명하고, 잠재적인 리스크와 이점을 전달하며, 코드베이스에 기여하거나 OUSD를 제품에 통합하려는 개발자를 위한 가이드를 제공하기 위한 것입니다. 지금 바로 시작할 수있는 몇 가지 방법이 있습니다.

**발행(Mint) 또는 상환(Redeem)**

OUSD 발행(Mint) 를 사용하면 누구나 [디앱(DApp)](www.ousd.com) 및 [메타마스크(Metamask)](https://www.metamask.io)와 같은 웹-3 지원 암호화폐 지갑을 사용하여 OUSD 토큰을 생성하거나 거래 할 수 있습니다. 이것은 특히 다른 거래소에서 시장을 움직일 위험이있는 많은 금액을 원할 경우 OUSD를 얻는 기본 방법입니다.

**거래소에서 구매**

소액의 경우, OUSD로 수익 창출을 시작하는 가장 쉬운 방법은 유니스왑(Uniswap_과 같은 탈중앙화 거래소(DEX) 에서 구입하는 것입니다. 현재 사용할 수 있는 쌍(pair) 은 다음과 같습니다:

* [Buy OUSD on Uniswap](https://app.uniswap.org/#/swap?outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Buy OUSD on Mooniswap](https://mooniswap.exchange/#/swap?outputToken=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)

또한 OUSD는 조만간 추가적인 탈중앙화 및 중앙 집중식 거래소에서 널리 사용 가능할 것으로 예상됩니다.

**지갑에 OUSD 추가**

{% hint style="success" %}
오리진달러\(OUSD\) 의 대표 ERC20 주소:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

OUSD가 지갑에 자동으로 표시되지 않는 경우 위 주소를 사용하여 수동으로 추가 할 수 있습니다. 오리진은 OUSD를 가능한 한 많은 지갑에서 지원하고, 잘 알려진 토큰의 모든 목록에 포함시키고 싶습니다. 혹시 해당 분야에서 도움을 주실 수 있다면, 진심으로 감사하겠습니다.

**OUSD 통합**

OUSD는 비표준 ERC-20 토큰으로 이를 지원하려는 대부분의 애플리케이션들은 커스텀(custom) 통합 작업이 필요합니다. 특히 개발자가 탄력적 공급이 어떻게 작동하는지 이해하는 것이 중요합니다. 이는 예상치 못한 동작을 쉽게 일으킬 수 있기 때문입니다.

만약, OUSD 지원에 관심이 있는 지갑 공급자 또는 암호화폐 거래소인 경우에는 다음 가이드를 참고하시길 바랍니다:

{% page-ref page="smart-contracts/architecture.md" %}

{% page-ref page = "smart-contracts / api.md"%}

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies.

**Getting Help**

Please join the Origin Dollar \#engineering room in Origin's [Discord](www.originprotocol.com/discord) server.  Our team and members of our community look forward to helping you build. Your questions help us improve, so please don't hesitate to ask if you can't find what you are looking for here.

