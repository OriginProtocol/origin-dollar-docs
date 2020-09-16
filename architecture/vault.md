# Vault

The vault is at the core of the protocol. The vault is responsible for minting/redeeming OUSD tokens, rebalancing funds between the various supported strategies, and liquidating rewards tokens.

The most important externally callable functions on the Vault are `mint()`   `mintMultiple()` `redeem()` and `redeemAll()`

* `mint()`allows a single stablecoin to be converted to OUSD
* `mintMultiple()`allows multiple stablecoins to be converted to OUSD in a single call
* `redeem()`allows a specified amount of OUSD to be redeemed for other supported stablecoins. 
* `redeemAll()`allows a user to redeem their entire balance of OUSD for other supported stablecoins. This is particularly useful since user balances are constantly growing as yield is accrued.

On redemptions, it is the protocol and not the user that decides which stablecoin\(s\) to return to the user. This decision of which coin\(s\) to return is based on the internal ratios of the assets that are being held in the pool.



