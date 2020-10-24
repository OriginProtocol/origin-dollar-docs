# Vue d'ensemble

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD est basé sur une séries de contrats intelligents. Chacun de ces contrats est imbriqués dans un contrat auxillière qui peut être mis à jour via le protocole de gouvernance.

À l'interne, la propriété de ce pool est calculée à l'aide d'un système de crédit au prorata de chaque participants. Le contrat ERC-20 gère la conversion en dollar US lorsque la balance est affichée ou qu'un transfère entre portefeuille est initité.

La voute est responsable de la création et la destruction des OUSD. It also enforces the percentage of assets that are deployed to each of the supported [Strategies](../core-concepts/supported-strategies/). To optimize gas costs, the vault maintains a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.



