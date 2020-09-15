# Supported Oracles

The OUSD oracle contract fetches prices from multiple reputable on-chain oracles and chooses the exchange rate that is most advantageous for the pool and the least beneficial for the individual. This is done for several reasons:

* First, we want to prevent arbitrageurs from draining the pool's funds if there is an error with one of the oracles being used. For example, if Chainlink says USDT is worth $0.50 when the consensus market price is still $1, an attacker would be able to deposit 1 DAI to withdraw 2 units of USDT if this was the only oracle that was used. However, if the Open Price Feed, a second oracle, says that USDT is worth $1, then the pool prices USDT correctly at and prevents funds from being drained.
* Secondly, we want to encourage long-term depositors of OUSD. Therefore, individuals that frequently enter and exit OUSD are slightly penalized by receiving the least beneficial exchange rate on both the buy-side and sell-side. The overall pool benefits when it accrues these negligible spreads.

{% tabs %}
{% tab title="DAI/USD" %}
The following oracles are used to fetch or compute a price for **DAI/USD:**

| Oracle | Pair | Contract |
| :--- | :--- | :--- |
| Open Price Feed | DAI/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| Chainlink | DAI/USD | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0 |
| Chainlink | DAI/ETH | 0x037E8F2125bF532F3e228991e051c8A7253B642c |
| Uniswap v2 | DAI/ETH | 0xA478c2975Ab1Ea89e8196811F51A7B7Ade33eB11 |
{% endtab %}

{% tab title="USDT/USD" %}
The following oracles are used to fetch or compute a price for **USDT/USD:**

| O**racle** | Pair | Contract |
| :--- | :--- | :--- |
| Chainlink | USDT/ETH | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE |
| Uniswap v2 | USDT/ETH | 0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852 |

\*\*\*\*
{% endtab %}

{% tab title="USDC/USD" %}
The following oracles are used to fetch or compute a price for **USDC/USD:**

| O**racle** | Pair | Contract |
| :--- | :--- | :--- |
| Maker | USDC/USD | 0x77b68899b99b686F415d074278a9a16b336085A0 |
| Chainlink | USDC/ETH | 0xdE54467873c3BCAA76421061036053e371721708 |
| Uniswap v2 | USDC/ETH | 0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc |
{% endtab %}

{% tab title="ETH/USD" %}
Since not all oracles have direct USD pairs, the protocol also fetches the prices for **ETH/USD** in order to calculate USD prices using ETH. Again, to be safe, the protocol chooses the most advantgeous for the fund instead of the individual. 

| Oracle | Pair | Contract |
| :--- | :--- | :--- |
| Open Price Feed | ETH/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| Maker | ETH/USD | 0x81FE72B5A8d1A857d176C3E7d5Bd2679A9B85763 |
| Chainlink | ETH/USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}
{% endtabs %}

It is possible that additional oracles will be added to the protocol over time. Support may also be removed if any of these oracles prove to be too unreliable or put OUSD holders funds in jeopardy. 

