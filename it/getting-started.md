# Per partire

Questa documentazione ha lo scopo di spiegare il funzionamento di OUSD, di comunicare i potenziali rischi e benefici, di fornire una guida per sviluppatori che volessero contribuire allo sviluppo del nostro codebase o ad integrare OUSD nei loro prodotti. Ecco qui alcuni modi per cominciare.

**Mint o Redeem**

Il Minting di OUSD consente a chiunque di creare o scambiare token OUSD utilizzando la nostra [DApp](www.ousd.com) e un wallet critpo abilitato per il web-3 come ad esempio [Metamask](https://www.metamask.io). Questo è il modo nativo per ottenere OUSD, specialmente se si desidera un grande quantità che potrebbe comportare una notevole variazione di mercato in altri exchange.

**Acquista negli Exchange**

Per piccoli importi, il modo più semplice di cominciare a guadagnare con OUSD è comprarlo in un exchange. Prevediamo che OUSD sarà presto disponibile in molti più exchange sia decentralizzati sia centralizzati.

Exchange Decentralizzati:

* [Acquista OUSD su Uniswap](https://app.uniswap.org/#/swap?outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Acquista OUSD su Mooniswap](https://mooniswap.exchange/#/swap?outputToken=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)
* [Acquista OUSD su Sushiswap](https://exchange.sushiswapclassic.org/#/swap?inputCurrency=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86&outputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7)

Exchange Centralizzati:

* [Acquista OUSD su Virgox](https://virgox.com/exchange/141)
* [Acquista OUSD su Dharma App](https://www.dharma.io/)\(disponibile solo in USA\)

**Aggiungi OUSD sul tuo wallet**

{% hint style="success" %}
L'address ERC20 principale per Origin Dollar \(OUSD\) è    
** 0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
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

