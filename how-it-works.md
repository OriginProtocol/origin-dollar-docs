# How It Works

#### 100% Backed and Stable

Origin Dollar \(OUSD\) is a non-standard ERC-20 token for the Ethereum network. 

OUSD is a stable currency that is backed 1:1 by other proven stablecoins like USDT, USDC and DAI. As a result, 1 OUSD should always be very close to 1 USD in value.

{% hint style="success" %}
1 OUSD = 1 USD 
{% endhint %}

#### Minting OUSD

Users convert their existing stablecoins \(currently USDT, USDC, and DAI\) to OUSD at the official [Origin Dollar DApp](www.ousd.com). Issued OUSD begins accruing compounding yield immediately.

**Redeeming OUSD**

{% hint style="info" %}
There is a **0.5% exit fee** and you don't get to pick which stablecoin you will receive
{% endhint %}

Users can convert their OUSD back into other stablecoins at any time using the [Origin Dollar DApp](www.ousd.com). The 0.5% exit fee is charged upon redemption and is distributed in the form of additional yield to the remaining participants in the pool. This fee exists to incentivize long-term holders over short-term speculators. It's also a security feature as it makes it more difficult for attackers to take advantage of mispriced or lagging oracles to drain the pool.

Upon redemption, the smart contract will determine which stablecoin\(s\) to return to the user. Internally, the pool will try to maintain equal parts of each supported stablecoin and will liquidate whichever coin is in surplus. This lack of user optionality also acts to protect the pool in the event that any of the supported stablecoins lose their peg to the dollar.

#### A**utomated Yield Farming**

OUSD generates yields by deploying the underlying stablecoins that were deposited to the OUSD smart contract to other DeFi protocols such as Compound, Aave, Uniswap, Uniswap, and Curve. Initially, much of the pool's investment strategy will be directed through a single strategy \(FILL THIS IN LATER\), but it is expected there will be new diversified strategies added to the pool every month. Collected interest, trading fees, and rewards tokens are pooled and liquidated to produce OUSD-denominated yields. Over time, the protocol will programmatically move assets in and out of different liquidity pools in order to provide the best yield to the holders of OUSD. 

#### **Elastic Supply**

The generated returns are passed on to the holders of OUSD via constant rebasing of the money supply. OUSD constantly adjusts the money supply in response to the yield the protocol has generated. This allows the price of OUSD to stay pegged at $1 while the balances in token holders' wallets adjust in real-time to reflect yields that have been earned by the protocol.

The end result is a stablecoin that is easy to spend, earns outsized yields automatically, and is more desirable to hold than existing stablecoins.

