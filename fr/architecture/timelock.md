# Verrouillage temporel

{% hint style="danger" %}
Lorsque tout sera testé, le verrouillage temporel sera ajouté. D'ici là, les contrats seront gouvernées par Origin selon la méthode multi-sig (5 sur 8). Cela permettera une réponse plus rapide si un incident critique devait être découvert.
{% endhint %}

Le verrouillage temporel du contrat impose une période d'attente de 48 heures avant qu'il ne soit possible d'exécuter quelques changements que ce soit aux contrats OUSD. Le verrouillage temporel peut être appelé par notre multi-sig and est le propriétaore de nos contrats [ERC-20](erc-20.md), [Vault](vault.md), and [Strategies](strategies.md). Les actions d'administration à retardement donne à l'usager la chance de retirer des OUSD si l'administrateur est compromis, malveillant ou s'il entreprend un changement pour lequel l'utilisateur n'est pas d'accord.

{% hint style="info" %}
Le verrouillage temporel est une mesure de sécurité qui donne aux détenteurs de OUSD 48 heures pour retirer leurs fonds s'ils ont une objections à une proposition de mise à jour du protocole.
{% endhint %}

OUSD utilise une version légèrement modifiée de [Compound Timelock](https://compound.finance/docs/governance) qui a été auditer par [audited by OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). Les trois différences notoires sont:

1. OUSD utilisera initialement une prédiode d'attente plus courte (48 heures) que Compound (72 heures) pour permettre une réponse plus rapide si un enjeu survenait.
2. Après le délais de 48 heure, n'importe qui est libre d'exécuter un appel, pas seulement le propriétaire du contrat.
3. Les dépôts (mais pas les retraits ou les transferts) pourront être immédiatement gelés sans le délais nécessaire de 48 heures. Ceci sera utile seulement si une vulnérabilité majeure serait découverte.





