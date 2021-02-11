# OUSD 如何运作

#### 100％ 稳定以由其他稳定比支持

Origin Dollar （OUSD）是用于以太坊网络的一个 ERC-20 代币。

OUSD 是个由 USDT，USDC 和 DAI 等其他经过验证的稳定币以 1：1 支持的稳定货币。 因此，1 OUSD 的价值应该始终非常接近 1 USD。

{% hint style="success" %}
1 OUSD = 1 USD
{% endhint %}

#### 铸造 OUSD

用户通过官方 [Origin Dollar DApp](www.ousd.com)将现有的稳定币（目前支持 USDT，USDC 和DAI）转换为 OUSD。 发行的 OUSD 立即开始累积复利。

**赎回 OUSD**

用户可以随时使用 [Origin Dollar DApp](www.ousd.com)将 OUSD 转换回其他稳定币。 A 0.5% exit fee is charged upon redemption and is distributed as additional yield to the remaining participants in the vault. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from syphoning stablecoins from the vault in the event of mispricings of of the underlying assets. 这项费用的存在是为了激励长期持有者而不是短期投机者。

赎回后，智能合约将确定将哪种稳定币退还给用户。 In the current implementation, the vault will return coins in the same ratio as the current holdings. This lack of user optionality also protects the vault as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
OUSD 有**0.5％ 的退出费** ，而且用户无法选择将收到的稳定币种.
{% endhint %}

#### 自**动收益耕作**

OUSD 通过将存储在 OUSD 智能合约中的稳定币部署到其他 DeFi 协议（例如 Compound，Aave，Uniswap，Balancer 和 Curve）来产生收益。 It is expected there will be new diversified strategies added to the vault every month. 得到的利息，交易费和奖励代币被收集并转换未稳定币，以产生以 OUSD 计价的收益。 随着时间的流逝，协议会将资产移入和移出不同的流动性池，以为 OUSD 持有者提供最佳收益。

#### **弹性供应**

通过不断调整货币供应量，产生的收益将传给 OUSD 的持有者。 OUSD会根据协议产生的收益不断调整货币供应量。 这允许 OUSD 的价格保持在 $1 不变，同时代币持有者的钱包中的余额会实时调整以反映协议所赚取的收益。

最终结果是一种易于消费，自动赚取超额收益，并且比现有稳定币更适合持有的稳定币。

