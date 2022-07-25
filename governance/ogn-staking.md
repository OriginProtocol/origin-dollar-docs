# OGV Staking

### Why Staking

Origin Dollar is built for the long term. As such, we need community governance that is similarly focused on the long term good of the protocol. We incentivize long term thinking by having users lock up governance tokens (OGV) for a period of time in exchange for voting power (veOGV). The longer a user chooses to lockup for, the more voting power they receive. This ensures that voting power goes to those who have an interest in the long term success of the protocol.

To incentivize people to provide governance, staking is rewarded. Stakers will receive both OGV inflation and a percentage of protocol yield.

### Voting Power Calculation

To get veOGV voting power, you lockup OGV for a chosen duration. You cannot withdraw the locked up OGV amount until this lockup period is over. veOGV cannot be transfered. Rewards can be collected at any time, and are given in unlocked OGV.

The amount of veOGV you receive is based on how much OGV you lock up and the end date of the lockup. The farther into the future the end date is, the higher the multiplier. Two users whose locks end at the same date in the future (and thus have the same skin in the game per ogv) have the same multiplier.

The lockup multiplier curve is exponential. Each year forward has a 1.8 times larger multiplier.

A lockup for 4 years will be approximately 10.5 times larger than a lockup for 30 days. (1.8 \* 1.8 \* 1.8 \* 1.8 = 10.5). Similarly, a 1 year lockup placed 4 years into the future will be roughly 10.5 times larger in OGV terms than the same lockup placed now. Extending lockups works similarly. If you extend your lockup by a year, you immediately receive a 1.8 times multiplier on your veOGV for that stake, since the end date has moved forward by a year.

The maximum lockup duration is 4 years. The minimum is 30 days.

Over time the effective voting power of old lockups is diluted by newer lockups having larger multipliers.

When the lockup period ends, you keep your voting (and rewards) power.

### Rewards

Rewards for staking OGV can be claimed at any time.

OGV has a front loaded inflation schedule. This inflation goes to OGV stakers.

| OGV per month inflation | Start month |
| ----------------------- | ----------- |
| 100,000,000             | 0           |
| 80,000,000              | 1           |
| 56,000,000              | 3           |
| 33,600,000              | 7           |
| 16,800,000              | 15          |
| 6,720,000               | 27          |
| 2,016,000               | 47          |

It is possible that in the future a percentage of yield from OUSD will be used to buy back OGV from the market and distribute it as rewards to stakers.

{% hint style="info" %}
Visit [the OUSD Governance DApp](https://governance.ousd.com/stake) in a web3-enabled browser to stake your OGV.
{% endhint %}

OGV is currently available on [Huobi](https://www.huobi.com/exchange/ogv\_usdt/), [Gate.io](https://www.gate.io/trade/OGV\_USDT), and [Uniswap](https://app.uniswap.org/#/swap?outputCurrency=0x9c354503C38481a7A7a51629142963F98eCC12D0\&chain=mainnet).

