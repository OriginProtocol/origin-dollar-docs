# How It Works

#### 100% Backed and Stable

Origin Dollar \(OUSD\) is an ERC-20 compliant token for the Ethereum network. 

OUSD is a stable currency that is backed 1:1 by other stablecoins like USDT, USDC and DAI. As a result, 1 OUSD should always be very close to 1 USD in value.

{% hint style="success" %}
1 OUSD = 1 USD 
{% endhint %}

#### Minting OUSD

Users convert their existing stablecoins \(currently USDT, USDC, and DAI\) to OUSD at the official [Origin Dollar DApp](www.ousd.com). Issued OUSD begins accruing compounding yield immediately.

**Redeeming OUSD**

Users can convert their OUSD back into other stablecoins at any time using the [Origin Dollar DApp](www.ousd.com). A 0.5% exit fee is charged upon redemption and is distributed as additional yield to the remaining participants in the vault. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from siphoning stablecoins from the vault in the event of mispriced underlying assets. The fee exists to incentivize long-term holders over short-term speculators.

Upon redemption, the smart contract will determine which stablecoin\(s\) to return to the user. In the current implementation, the vault will return coins in the same ratio as the current holdings. This lack of user optionality also protects the vault as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
There is a **0.5% exit fee** and the user doesn't get to pick which stablecoins they receive.
{% endhint %}

#### A**utomated Yield Farming**

OUSD generates yields by deploying the underlying stablecoins that were deposited to the OUSD smart contract to other DeFi protocols such as Compound, Aave, and Curve. There may be new diversified strategies added to the vault in the future. Collected interest, trading fees, and rewards tokens are pooled and converted to stablecoins to produce OUSD-denominated yields. Over time, the protocol will move assets in and out of different liquidity pools in order to provide the best yield to the holders of OUSD. 

#### **Elastic Supply**

The generated returns are passed on to the holders of OUSD via constant rebasing of the money supply. OUSD constantly adjusts the money supply in response to the yield the protocol has generated. This allows the price of OUSD to stay pegged at $1 while the balances in token holders' wallets adjust in real-time to reflect yields that have been earned by the protocol.

The end result is a stablecoin that is easy to spend, earns outsized yields automatically, and is more desirable to hold than existing stablecoins.

