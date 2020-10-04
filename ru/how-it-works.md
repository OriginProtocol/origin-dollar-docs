# How It Works

#### 100% Backed and Stable

Origin Dollar \(OUSD\) is an ERC-20 compliant token for the Ethereum network.

OUSD is a stable currency that is backed 1:1 by other stablecoins like USDT, USDC and DAI. As a result, 1 OUSD should always be very close to 1 USD in value.

{% hint style="success" %}
1 OUSD = 1 USD
{% endhint %}

#### "Чеканка" OUSD

Пользователи конвертируют свои существующие стейблкоины \ (в настоящее время USDT, USDC и DAI \) в OUSD в официальном [Origin Dollar DApp](www.ousd.com). Выпущенные OUSD немедленно начинают приносить доход от начисления сложных процентов.

**Вомещение OUSD**

Пользователи могут конвертировать свои OUSD в другие стейблкоины в любое время, используя [Origin Dollar DApp](www.ousd.com). При выкупе взимается комиссия в размере 0,5%, которая распределяется как дополнительный доход между оставшимися участниками пула. Комиссия служит функцией безопасности, чтобы злоумышленникам было сложнее обмануть запаздывающих оракулов, не давая им поглощать стейблкоины из пула в случае неверной оценки базовых активов. Комиссия существует для того, чтобы заинтересовывать долгосрочных держателей, а не краткосрочных спекулянтов.

Upon redemption, the smart contract will determine which stablecoin\(s\) to return to the user. In the current implementation, the pool will return coins in the same ratio as the current holdings. This lack of user optionality also protects the pool as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
There is a **0.5% exit fee** and the user doesn't get to pick which stablecoins they receive.
{% endhint %}

#### A**utomated Yield Farming**

OUSD generates yields by deploying the underlying stablecoins that were deposited to the OUSD smart contract to other DeFi protocols such as Compound, Aave, Uniswap, Balancer, and Curve. It is expected there will be new diversified strategies added to the pool every month. Collected interest, trading fees, and rewards tokens are pooled and converted to stablecoins to produce OUSD-denominated yields. Over time, the protocol will move assets in and out of different liquidity pools in order to provide the best yield to the holders of OUSD.

#### **Elastic Supply**

The generated returns are passed on to the holders of OUSD via constant rebasing of the money supply. OUSD constantly adjusts the money supply in response to the yield the protocol has generated. This allows the price of OUSD to stay pegged at $1 while the balances in token holders' wallets adjust in real-time to reflect yields that have been earned by the protocol.

The end result is a stablecoin that is easy to spend, earns outsized yields automatically, and is more desirable to hold than existing stablecoins.

