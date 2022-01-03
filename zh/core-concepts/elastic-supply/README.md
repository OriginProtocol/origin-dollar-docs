# 弹性供应

**弹性供应。 价格稳定。**

OUSD 与大多数代币的运作方式不同。 Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Instead, the contracts constantly adjust the monetary supply and automatically updates the balance in every token holder’s wallet to reflect the yield that has been earned by the protocol.&#x20;

{% hint style="info" %}
您可以将其视为银行帐户中的利息。 美元的帐户单位和价值不变。 当您赚取利息时，您将获得更多美元。
{% endhint %}

![](../../.gitbook/assets/ousd\_docs\_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD is 100% backed by other stablecoins and does not have the same challenge maintaining the peg to the dollar. Given the ease of minting and redeeming OUSD, we can count on arbitrageurs to ensure the peg is maintained.&#x20;
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. 只要基础贷款 / AMM和稳定币协议没有任何问题，您的资金就会受到保护。 Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which only rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts. Chainlink Keepers ensure at least one rebase occurs every day.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.
