# Как это работает

#### На 100% поддерживаемый и стабильный

Origin Dollar (OUSD) is an ERC-20 compliant token for the Ethereum network.

OUSD - это стабильная валюта, которая в соотношении 1:1 поддерживается другими стейблкоинами, такими как USDT, USDC и DAI. В результате 1 OUSD всегда должен быть очень близок к стоимости 1 USD.

{% hint style="success" %}
1 OUSD = 1 доллар США
{% endhint %}

#### Buying OUSD

Users can convert their existing stablecoins (currently USDT, USDC, and DAI) to OUSD at the official [Origin Dollar DApp](https://www.ousd.com). Received OUSD begins accruing compounding yield immediately.

The Origin DApp will intelligently route user's transactions to give them the best available price while taking slippage and gas costs into consideration. This means that the DApp will sometimes encourage users to buy OUSD that is already in circulation versus minting fresh OUSD from the vault. The OUSD DApp will choose from multiple sources of liquidity and will suggest the option that gives the user the best possible rate.

**Selling OUSD**

Users can convert their OUSD back into other stablecoins at any time using the [Origin Dollar DApp](https://www.ousd.com). The Origin DApp will intelligently route user's transactions to give them the best available price while taking slippage, gas costs, and the vault's exit fee into consideration. This means that the DApp will often help users sell their OUSD on AMM's instead of redeeming OUSD with the vault and incurring the protocol's exit fee.

A 0.5% exit fee is charged upon redemption with the vault. This fee is distributed as additional yield to the remaining participants in the vault (ie. other OUSD holders). The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from siphoning stablecoins from the vault in the event of mispriced underlying assets. The fee exists to incentivize long-term holders over short-term speculators.

Upon redemption, the vault will determine which stablecoin(s) to return to the user. In the current implementation, the vault will return coins in the same ratio as the current holdings. This lack of user optionality also protects the vault as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
Redemptions on the OUSD vault incur a** 0.5% exit fee** and the user doesn't get to pick which stablecoins they receive. Users can often avoid this fee by selling to an AMM instead.
{% endhint %}

#### **Автоматизированное получение дохода**

OUSD generates yields by deploying the underlying stablecoins that were deposited to the OUSD smart contract to other DeFi protocols such as Compound, Aave, and Curve. There may be new diversified strategies added to the vault in the future. Collected interest, trading fees, and rewards tokens are pooled and converted to stablecoins to produce OUSD-denominated yields. Over time, the protocol will move assets in and out of different liquidity pools in order to provide the best yield to the holders of OUSD.

#### **Гибкое предложение**

The generated returns are passed on to the holders of OUSD via constant rebasing of the money supply. OUSD constantly adjusts the money supply in response to the yield the protocol has generated. This allows the price of OUSD to stay pegged at $1 while the balances in token holders' wallets adjust in real-time to reflect yields that have been earned by the protocol.

The end result is a stablecoin that is easy to spend, earns outsized yields automatically, and is more desirable to hold than existing stablecoins.
