# FAQ

**Where can I buy OUSD?**

Check out [Getting Started](https://docs.ousd.com/getting-started) to see a variety of options.

**What are the costs to mint and redeem OUSD?**

As with any Ethereum transaction, you will need Ether to interact with the OUSD smart contract. We have taken measures to reduce gas usage where possible, but these costs can vary.

Anytime you mint or redeem OUSD, there will be an exchange rate applied to your stablecoins deposited or withdrawn. You can read more about this in [Price Oracles](https://docs.ousd.com/core-concepts/price-oracles).

To encourage long-term holding of OUSD and to protect the protocol from attackers, an exit fee of 0.25% is charged on all redeems. You can read more about this in [How It Works](https://docs.ousd.com/how-it-works).

**How soon will my balance increase once I have OUSD?**

The amount of OUSD in your wallet will grow each time there is a positive rebase event. You can read more about this in [Elastic Supply](https://docs.ousd.com/core-concepts/elastic-supply). The supply is currently rebased several times per day and is usually correlated with how many people are minting and redeeming OUSD.

**Why does OUSD not grow when it's held in Uniswap, SushiSwap, etc?**

By default, rebase events don't affect the supply of OUSD that is sitting in smart contracts. These contracts can opt in to receiving additional OUSD if they are capable of handling elastic supply tokens. You can read more about this in [Rebasing & Smart Contracts](https://docs.ousd.com/core-concepts/elastic-supply/rebasing-and-smart-contracts).

**How is it possible for the APY to be so high?**

You can read about our various strategies in [Yield Generation](https://docs.ousd.com/core-concepts/yield-generation). We currently get most of the yield from harvesting rewards tokens (namely COMP and CRV). Additionally, the yield increases as more OUSD is held in smart contracts that do not opt into rebasing since the underlying collateral continues to earn for the average OUSD holder.

**Why is my balance increasing at a slower rate than the advertised APY?**

OUSD balances increase when the supply is rebased. But the size of each rebase varies wildly depending on how much the vault has earned since the last rebase. And while most rebases collect a small amount earnings from lending strategies, other rebases involve liquidating rewards tokens or collecting fees. As a result, the yield will vary significantly during short time periods.

**What about the hack? Is OUSD safe?**

On November 7th 2020, OUSD was exploited for 7M USD due to a previously undetected reentrancy bug. You can read more [details about the hack](https://medium.com/originprotocol/urgent-ousd-has-hacked-and-there-has-been-a-loss-of-funds-7b8c4a7d534c) on our blog as well as the [detailed compensation plan](https://medium.com/originprotocol/origin-dollar-ousd-detailed-compensation-plan-faa73f87442e) for taking care of the affected users. Origin Dollar was relaunched in December after completing multiple audits and security upgrades. You can learn more about the steps taken to secure the protocol in our [relaunch announcement](https://medium.com/originprotocol/origin-dollar-ousd-is-back-b8ee0c601dad).
