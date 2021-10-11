# Offre élatisque

**Offre élastique. Prix stable.**

OUSD fonctionne différemment de la pluspart des autres jetons. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Le contrat ajuste constamment l'offre monétaire et met à jour automatiquement la balance du portefeuille de chacun des détenteur de jetons afin de refléter le rendement obtenu par le protocole.

{% hint style="info" %}
Considérez cela comme étant un intérêt couru dans votre compte de banque. L'unité de compte et la valeur d'un dollar américain ne change pas. Vous obtenez simplement plus de dollars US au fur et à mesure que vous générez de l'intérêt.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD is 100% backed by other stablecoins and does not have the same challenge maintaining the peg to the dollar. Compte tenu de la facilité de créer et de racheter des OUSD. nous pouvons compter sur l'arbitrage afin de maintenir l'ancrage au dollar.
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Votre principal est protégé tant que rien n'impact négativement la stratégie sous-jacente de prêt/AMM et des protocoles de monnaies stables. Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.
