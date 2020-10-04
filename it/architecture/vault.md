# Vault

Il Vault è il cuore del protocollo. Il vaulta è il responsabile del conio/riscatto dei token OUSD, del ribilanciamento dei fondi tra le varie strategie supportate, e della liquidazione dei token di ricompensa.

The most important publicly callable functions on the Vault are:

* `mint()`allows a single supported stablecoin to be converted to OUSD
* `mintMultiple()`allows multiple supported stablecoins to be converted to OUSD in a single call
* `redeem()`allows a specified amount of OUSD to be redeemed for other supported stablecoins.
* `redeemAll()`allows a user to redeem their entire balance of OUSD for other supported stablecoins. This is particularly useful since user balances are constantly growing as yield is accrued.
* `rebase()`updates the balances for all users based on the value of the assets currently stored in the pool.
* `allocate()`moves the assets under management into their prescribed [Stategies](strategies.md) to maximize yield and diversify risk.

On redemptions, it is the protocol and not the user that decides which stablecoin\(s\) to return to the user. This decision of which coin\(s\) to return is based on the internal ratios of the assets that are being held in the pool.



