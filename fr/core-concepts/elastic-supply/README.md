# Offre élatisque

**Offre élastique. Prix stable.**

OUSD fonctionne différemment de la pluspart des autres jetons. Au lieu d'avoir le prix qui augmente lorsque la valeur des actifs sous gestion augmente\ (comme c'est le cas avec Compound cTokens ou Yearn yTokens\), la valeur d'un OUSD demeure constante, soit approximativement 1$. Le contrat ajuste constamment l'offre monétaire et met à jour automatiquement la balance du portefeuille de chacun des détenteur de jetons afin de refléter le rendement obtenu par le protocole.

{% hint style="info" %}
Considérez cela comme étant un intérêt couru dans votre compte de banque. L'unité de compte et la valeur d'un dollar américain ne change pas. Vous obtenez simplement plus de dollars US au fur et à mesure que vous générez de l'intérêt.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

Ce mécanisme est inspiré par une nouvelle appoche adoptée par [Ampleforth](https://www.ampleforth.org/), par contre, certaines différences méritent d'être soulignées:

1. OUSD est soutenu à 100% par d'autres monnaies stables et n'aura pas le même enjeu afin de maintenir l'ancrage au dollar. Compte tenu de la facilité de créer et de racheter des OUSD. nous pouvons compter sur l'arbitrage afin de maintenir l'ancrage au dollar.
2. OUSD rebasing should only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Any decrease in your balance would be an indication of trouble in the system.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated.

