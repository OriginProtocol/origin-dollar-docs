# Offre élatisque

**Offre élastique. Prix stable.**

OUSD fonctionne différemment de la pluspart des autres jetons. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Instead, the contracts constantly adjust the monetary supply and automatically updates the balance in every token holder’s wallet to reflect the yield that has been earned by the protocol.&#x20;

{% hint style="info" %}
Considérez cela comme étant un intérêt couru dans votre compte de banque. L'unité de compte et la valeur d'un dollar américain ne change pas. Vous obtenez simplement plus de dollars US au fur et à mesure que vous générez de l'intérêt.
{% endhint %}

![](../../.gitbook/assets/ousd\_docs\_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD is 100% backed by other stablecoins and does not have the same challenge maintaining the peg to the dollar. Given the ease of minting and redeeming OUSD, we can count on arbitrageurs to ensure the peg is maintained.&#x20;
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Votre principal est protégé tant que rien n'impact négativement la stratégie sous-jacente de prêt/AMM et des protocoles de monnaies stables. Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which only rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts. Chainlink Keepers ensure at least one rebase occurs every day.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.
