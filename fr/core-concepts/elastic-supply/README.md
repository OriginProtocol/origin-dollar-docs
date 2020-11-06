# Offre élatisque

**Offre élastique. Prix stable.**

OUSD fonctionne différemment de la pluspart des autres jetons. Au lieu d'avoir le prix qui augmente lorsque la valeur des actifs sous gestion augmente\ (comme c'est le cas avec Compound cTokens ou Yearn yTokens\), la valeur d'un OUSD demeure constante, soit approximativement 1$. Instead, the contracts constantly adjust the monetary supply and automatically updates the balance in every token holder’s wallet to reflect the yield that has been earned by the protocol.

{% hint style="info" %}
Think of it as interest accruing in your bank account. The unit of account and value for the US dollar doesn’t change. You just get more US dollars over time as you earn interest.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org/), but there are some key differences that are worth highlighting:

1. OUSD is 100% backed by other stablecoins and will not have the same challenge maintaining the peg to the dollar. Given the ease of minting and redeeming OUSD, we can count on arbitrageurs to ensure the peg is maintained.
2. OUSD rebasing should only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Any decrease in your balance would be an indication of trouble in the system.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated.

