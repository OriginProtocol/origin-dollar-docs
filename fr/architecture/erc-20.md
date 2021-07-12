# Vue d'ensemble

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD est basé sur une séries de contrats intelligents. Chacun de ces contrats est imbriqués dans un contrat auxillière qui peut être mis à jour via le protocole de gouvernance.

À l'interne, la propriété de ce pool est calculée à l'aide d'un système de crédit au prorata de chaque participants. Le contrat ERC-20 gère la conversion en dollar US lorsque la balance est affichée ou qu'un transfère entre portefeuille est initité.

La voute est responsable de la création et la destruction des OUSD. En plus, elle détermine le pourcentage d'actifs qui doit être déployés afin de soutenir chacune des [Strategies](../core-concepts/supported-strategies/). Pour optimiser les coûts de transaction, la voute maintien un tampon qui permet la majorité des dépôts et des retraits sans devoir liquider des actifs.



