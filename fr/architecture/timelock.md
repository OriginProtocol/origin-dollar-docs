# Verrouillage temporel

{% hint style="danger" %}
Lorsque tout sera testé, le verrouillage temporel sera ajouté. D'ici là, les contrats seront gouvernées par Origin selon la méthode multi-sig (5 sur 8). Cela permettera une réponse plus rapide si un incident critique devait être découvert.
{% endhint %}

Le verrouillage temporel du contrat impose une période d'attente de 48 heures avant qu'il ne soit possible d'exécuter quelques changements que ce soit aux contrats OUSD. Le verrouillage temporel peut être appelé par notre multi-sig and est le propriétaore de nos contrats [ERC-20](erc-20.md), [Vault](vault.md), and [Strategies](strategies.md). Time-delaying admin actions gives users a chance to exit OUSD if its admins become malicious, are compromised, or make a change that the users do not like.

{% hint style="info" %}
The timelock is a safety measure that gives OUSD holders 48 hours to withdraw their funds if they have objections to any proposed upgrades to the protocol.
{% endhint %}

OUSD is using a slightly modified version of the [Compound Timelock](https://compound.finance/docs/governance) which has been [audited by OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). The 3 notable differences are:

1. OUSD will initially use a shorter wait period \(48 hours\) than Compound \(72 hours\) to allow for a faster response if any issues are discovered.
2. Once the 48 hours have passed, anyone is free to execute the call, not just the owner of the contract.
3. Deposits \(but not withdrawals or transfers\) can be immediately frozen without requiring the 48 waiting period. This is in case a major vulnerability is discovered.





