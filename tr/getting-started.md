# Başlamak

Bu belgeler, OUSD'nin nasıl çalıştığını açıklamayı, potansiyel riskleri ve faydaları iletmeyi ve kod tabanımıza katkıda bulunmak veya OUSD'yi ürünlerine entegre etmek isteyen geliştiriciler için bir kılavuz sağlamayı amaçlamaktadır. İşte dalmanız ve başlamanız için birkaç yol.

**Basmak veya itfa**

OUSD Mint, herkesin [DApp](www.ousd.com) ve [Metamask](https://www.metamask.io)gibi web-3 özellikli bir kripto para birimi cüzdanı kullanarak OUSD jetonları oluşturmasına veya ticaretine izin verir. Bu, OUSD almanın yerel yoludur, özellikle piyasayı diğer borsalarda hareket ettirme riskini alabilecek büyük bir miktar istiyorsanız.

**Borsalarda Satın Alın**

For small amounts, the easiest way to start earning with OUSD is to buy it on an exchange. We anticipate that OUSD will soon be available on many more decentralized and centralized exchanges.

Decentralized exchanges:

* [Uniswap'te OUSD satın alın](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86&use=v2)
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
