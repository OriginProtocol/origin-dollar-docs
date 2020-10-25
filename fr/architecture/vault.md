# La voute

La Voute se situe au coeur du protocole. La voute est responsable de la création et du rachat des jetons OUSD en plus de rebalancer les fonds entre les différentes stratégies et la liquidation des jetons gagnés.

La fonction appelable la plus importante de la Voute est:

* `mint()` qui permet la conversion d'une pièce stable (stablecoin) en OUSD
* `mintMultiple()` qui permet de convertir plusieur pièce stable en OUSD en un seul appel
* `redeem()` qui permet d'échanger un nombre spécifique d'OUSD contre une autre pièce stable supportée.
* `redeemAll()` qui permet à l'utilisateur de convertire sa balance en entier d'OUSD en une pièce stable qui est prise en charge. Ceci est particulièerement utile puisque la balance des utilisateurs augmentent constament à mesure que le rendement augmente.
* `rebase()` permet la mise à our de la balance de touts les utilisateur selon les actifs qui sont actuellement stockés dans le pool.
* `allocate()` permet de déplacer certains actifs sous gestion dans une stratégie [Stategies](strategies.md) afin de maximiser le rendement et diversifier le risque.

Lors du rachat, c'est le protocole et non l'utilisateur qui décide quelle(s) pièce(s) stable(s) sera retourné à l'utilisateur. Cette décision est basée les ratios interne des actifs qui sont détenus dans le pool.



