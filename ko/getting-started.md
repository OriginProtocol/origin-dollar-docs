# 시작하기

이 문서는 OUSD의 작동 방식을 설명하고, 잠재적인 리스크와 이점을 전달하며, 코드베이스에 기여하거나 OUSD를 제품에 통합하려는 개발자를 위한 가이드를 제공하기 위한 것입니다. 지금 바로 시작할 수있는 몇 가지 방법이 있습니다.

**발행(Mint) 또는 상환(Redeem)**

OUSD 발행(Mint) 를 사용하면 누구나 [디앱(DApp)](www.ousd.com) 및 [메타마스크(Metamask)](https://www.metamask.io)와 같은 웹-3 지원 암호화폐 지갑을 사용하여 OUSD 토큰을 생성하거나 거래 할 수 있습니다. 이것은 특히 다른 거래소에서 시장을 움직일 위험이있는 많은 금액을 원할 경우 OUSD를 얻는 기본 방법입니다.

**거래소에서 구매**

For small amounts, the easiest way to start earning with OUSD is to buy it on an exchange. We anticipate that OUSD will soon be available on many more decentralized and centralized exchanges.

Decentralized exchanges:

* [Buy OUSD on 1inch](https://app.1inch.io/#/1/swap/USDT/OUSD)
* [Buy OUSD on Uniswap v3](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Buy OUSD on Uniswap v2](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86&use=v2)
* [Buy OUSD on Sushiswap](https://exchange.sushiswapclassic.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)

Centralized exchanges:

* Buy OUSD on KuCoin
  * [OUSD/USDT](https://trade.kucoin.com/OUSD-USDT)
  * [OUSD/BTC](https://trade.kucoin.com/OUSD-BTC)
* Buy OUSD on Virgox
  * [OUSD/USDT](https://virgox.com/exchange/141)
* [Buy OUSD on Dharma App](https://www.dharma.io/) \(US only\)

**Adding OUSD to Your Wallet**

{% hint style="success" %}
The main ERC20 address for Origin Dollar \(OUSD\) is:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

If your OUSD does not automatically show up in your wallet, you should be able to add it manually using the address above. If you are planning on [storing your OUSD in a multi-sig wallet](core-concepts/elastic-supply/rebasing-and-smart-contracts.md), be sure to opt-in to receive yield. We want to have OUSD supported by as many wallets as possible and included on all the various lists of well-known tokens. We would greatly appreciate any help you can offer in this area.

**Integrating OUSD**

OUSD is a non-standard ERC-20 token that requires custom integration work for most applications that wish to support it. In particular, it is important for developers to understand how our elastic supply works as this can easily cause unexpected behavior.

If you are a wallet provider or crypto exchange that is interested in supporting OUSD, please refer to the following guides:

{% page-ref page="core-concepts/elastic-supply/rebasing-and-smart-contracts.md" %}

{% page-ref page="smart-contracts/architecture.md" %}

{% page-ref page="smart-contracts/api/" %}

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies.

**Getting Help**

Please join the Origin Dollar \#engineering room in Origin's [Discord](www.originprotocol.com/discord) server.  Our team and members of our community look forward to helping you build. Your questions help us improve, so please don't hesitate to ask if you can't find what you are looking for here.

