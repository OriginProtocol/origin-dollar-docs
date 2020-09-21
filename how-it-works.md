# OUSD 如何运作

## 100％ 稳定以由其他稳定比支持

Origin Dollar \(OUSD\) is an ERC-20 compliant token for the Ethereum network.

OUSD is a stable currency that is backed 1:1 by other stablecoins like USDT, USDC and DAI. 因此，1 OUSD 的价值应该始终非常接近 1 USD。

{% hint style="success" %}
1 OUSD = 1 USD
{% endhint %}

## 铸造 OUSD

用户通过官方 [Origin Dollar DApp](https://github.com/oplabs/origin-dollar-docs/tree/0c8c4fe1b7fa9ae3c66881983a8cf542864e9cd7/www.ousd.com)将现有的稳定币\（目前支持 USDT，USDC 和DAI \）转换为 OUSD。 发行的 OUSD 立即开始累积复利。

**赎回 OUSD**

Users can convert their OUSD back into other stablecoins at any time using the [Origin Dollar DApp](https://github.com/oplabs/origin-dollar-docs/tree/0c8c4fe1b7fa9ae3c66881983a8cf542864e9cd7/www.ousd.com). A 0.5% exit fee is charged upon redemption and is distributed as additional yield to the remaining participants in the pool. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from syphoning stablecoins from the pool in the event of mispricings of of the underlying assets. The fee exists to incentivize long-term holders over short-term speculators.

Upon redemption, the smart contract will determine which stablecoin\(s\) to return to the user. In the current implementation, the pool will return coins in the same ratio as the current holdings. This lack of user optionality also protects the pool as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
There is a **0.5% exit fee** and the user doesn't get to pick which stablecoins they receive.
{% endhint %}

## 自**动收益耕作**

OUSD generates yields by deploying the underlying stablecoins that were deposited to the OUSD smart contract to other DeFi protocols such as Compound, Aave, Uniswap, Balancer, and Curve. It is expected there will be new diversified strategies added to the pool every month. Collected interest, trading fees, and rewards tokens are pooled and converted to stablecoins to produce OUSD-denominated yields. Over time, the protocol will move assets in and out of different liquidity pools in order to provide the best yield to the holders of OUSD.

## **弹性供应**

通过不断调整货币供应量，产生的收益将传给 OUSD 的持有者。 OUSD会根据协议产生的收益不断调整货币供应量。 这允许 OUSD 的价格保持在 $1 不变，同时代币持有者的钱包中的余额会实时调整以反映协议所赚取的收益。

最终结果是一种易于消费，自动赚取超额收益，并且比现有稳定币更适合持有的稳定币。

