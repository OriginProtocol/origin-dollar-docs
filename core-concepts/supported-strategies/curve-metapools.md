# Curve MetaPools

MetaPools are Curve pools that allow for one token to trade with another underlying base pool. 3Pool is the most common base pool and it is the only one currently supported by our strategy codebase. For example, a TUSD MetaPool using 3Pool as base pool enables users to seamlessly trade between TUSD and 3Pool (DAI/USDC/USDT).

Having 3Pool as base pool is helpful in multiple ways:

* Prevents diluting existing pools
* Allows Curve to list less liquid assets
* More volume and more trading fees for the DAO

MetaPool liquidity providers can then deposit the LP tokens to Convex gauge to earn boosted CRV and CVX rewards.

### OUSD MetaPool

From Curve's point of view, the OUSD MetaPool is no different from any other MetaPool running on Curve's contracts. The difference for our strategy is the way we withdraw and deploy funds to the pool.

In the interest of causing a minimal negative effect to MetaPool balance, we deploy liquidity to both sides of the pool - USDT/DAI/USDC and OUSD. This ensures that, after deploying liquidity, the balance of the pool (share of 3Pool tokens to OUSD) doesn't change - since we deploy equal amounts to both sides of the pool. When the MetaPool is more heavily balanced towards 3Pool tokens, we deploy extra OUSD to preserve the pool balance, but never more than a 1:2 ratio (3Crv to OUSD).

This approach of providing (in most cases) double the liquidity to the OUSD MetaPool has a non-negligible, positive effect of the funds deployed to that pool earning double the rewards.

#### Non-Backed OUSD

It is important to note that OUSD deployed to OUSD MetaPool isn't minted by the Vault in a classic manner where it would be backed by a stablecoin. All OUSD minted for providing pool liquidity is not backed. When the strategy removes liquidity from the MetaPool alongside 3Pool tokens, the OUSD is also removed and burned.

We recognize that remaining fully collateralized is an important bedrock component of OUSD. _The non-backed OUSD held in the MetaPool is controlled by the protocol and it never enters circulation without generating profit for the protocol._ When traders add or remove OUSD from the MetaPool, it has an effect similar to redeeming or minting OUSD since our strategy is capable of burning or creating new supply to maintain the pool's balance. Ultimately, OUSD can still be redeemed at any time for the underlying collateral on a 1:1 basis.

We have completed extensive testing in forked Mainnet node environment simulating how flash loans could mint large amounts of OUSD, deploy liquidity to OUSD and then redeem it, manipulating the MetaPool at various stages of that procedure. No vulnerabilities have been found. It is also important to consider that funds can never be deployed to OUSD MetaPool as a result of OUSD mint (we have disabled this option of the OUSD MetaPool strategy) or withdrawn from MetaPool as a result of OUSD redeem. On top of that our approach of deploying & withdrawing from OUSD MetaPool has also been audited by OpenZeppelin.

| Resources      |                                                                                  |
| -------------- | -------------------------------------------------------------------------------- |
| Official site  | [https://www.convexfinance.com/](https://www.convexfinance.com/)                 |
| Developer docs | [https://docs.convexfinance.com/](https://docs.convexfinance.com/convexfinance/) |
| GitHub         | [https://github.com/convex-eth](https://github.com/convex-eth)                   |
| Discord        | [https://discord.com/invite/uAwvZfs9qU](https://discord.com/invite/uAwvZfs9qU)   |
