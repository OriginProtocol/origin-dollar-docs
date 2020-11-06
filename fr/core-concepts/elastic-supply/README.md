# Offre élatisque

**Offre élastique. Prix stable.**

OUSD fonctionne différemment de la pluspart des autres jetons. Au lieu d'avoir le prix qui augmente lorsque la valeur des actifs sous gestion augmente\ (comme c'est le cas avec Compound cTokens ou Yearn yTokens\), la valeur d'un OUSD demeure constante, soit approximativement 1$. Le contrat ajuste constamment l'offre monétaire et met à jour automatiquement la balance du portefeuille de chacun des détenteur de jetons afin de refléter le rendement obtenu par le protocole.

{% hint style="info" %}
Considérez cela comme étant un intérêt couru dans votre compte de banque. L'unité de compte et la valeur d'un dollar américain ne change pas. Vous obtenez simplement plus de dollars US au fur et à mesure que vous générez de l'intérêt.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

Ce mécanisme est inspiré par une nouvelle appoche adoptée par [Ampleforth](https://www.ampleforth.org/), par contre, certaines différences méritent d'être soulignées:

1. OUSD est soutenu à 100% par d'autres monnaies stables et n'aura pas le même enjeu afin de maintenir l'ancrage au dollar. Compte tenu de la facilité de créer et de racheter des OUSD. nous pouvons compter sur l'arbitrage afin de maintenir l'ancrage au dollar.
2. OUSD rebassage devra seulement augmenter l'offre puisque le nombre d'OUSD créé est lié au gain réalisé par les stratégies sous-jacentes. Votre principal est protégé tant que rien n'impact négativement la stratégie sous-jacente de prêt/AMM et des protocoles de monnaies stables. Toute diminution de votre balance sera une indication d'un problème avec le système.
3. Contrairement à Ampleforth qui rebase chaque jour, l'offre monétaire d'OUSD est constamment mise à jour en temps réel à mesure que le rendement est généré.

