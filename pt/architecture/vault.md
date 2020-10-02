# Cofre

O cofre está no núcleo do protocolo. O cofre é responsável pela emissão/resgate de tokens OUSD, pelo reequilibrio de fundos entre as várias estratégias suportadas, e pela liquidação de tokens de recompensa.

As funções mais importantes do Cofre que podem ser chamadas publicamente são:

* `mint()`permite que uma única stablecoin suportada seja convertida para OUSD
* `mintMultiple()`allows multiple supported stablecoins to be converted to OUSD in a single call
* `redeem()`allows a specified amount of OUSD to be redeemed for other supported stablecoins.
* `redeemAll()`allows a user to redeem their entire balance of OUSD for other supported stablecoins. This is particularly useful since user balances are constantly growing as yield is accrued.
* `rebase()`updates the balances for all users based on the value of the assets currently stored in the pool.
* `allocate()`moves the assets under management into their prescribed [Stategies](strategies.md) to maximize yield and diversify risk.

On redemptions, it is the protocol and not the user that decides which stablecoin\(s\) to return to the user. This decision of which coin\(s\) to return is based on the internal ratios of the assets that are being held in the pool.



