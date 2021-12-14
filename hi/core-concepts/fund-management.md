# Fund Management

The OUSD smart contract aggregates all users' stablecoin deposits into a single pool of assets that then get deployed into earning strategies based on preset allocations. In contrast to Yearn Vaults, TokenSets, or Zapper opportunities, users do not select individual strategies. All deposited stablecoins and consequently all OUSD tokens are fungible.&#x20;

The weighting of how assets are distributed between the supported strategies is decided by OGN holders using weekly snapshot voting. Ultimately, we believe it should be up to the community to decide what the right balance of risk/reward is appropriate for OUSD. We encourage the community to favor high-yield strategies while still maintaining diversification across multiple strategies to remove single points of failure and minimize risk.&#x20;

**How strategy allocation voting works:**

* New snapshot proposals will be posted on the [OGN governance portal ](https://vote.orignprotocol.com)around midnight Tuesday UTC (7pm eastern Monday)&#x20;
* Each proposal will use "weighted voting", with options for each coin/strategy combination. OGN holders can spread their votes among different listed strategies.
* The poll will be open for 48 hours, ending around midnight Thursday UTC (7pm eastern on Wednesday)
* During this time, those interested can discuss allocation changes in a thread in the #governance channel on [Origin's Discord](https://www.originprotocol.com/discord).
* After the voting time has ended, members of the [Strategist multi-sig](https://etherscan.io/address/0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC) will submit, verify, and execute transactions to change OUSD to the determined allocation percentages for the week.
* These allocations will be executed for strategies that use all stablecoins first (like Convex), then each stablecoin will be allocated to the remaining strategies according to the ratio of votes for that stablecoin / strategy combination.
* If the strategist multi-sig members deem any of the allocations unsafe to the funds behind OUSD, they may choose to not execute those. In addition, the multi-sig members may decline to execute minor adjustments where the gas costs would be greater than the expected benefits. The strategist multi-sig will continue to have the ability to instantly pause rebasing and capital to protect OUSD funds.
* Community members can use the [Strategy Validator tool](https://analytics.ousd.com/strategist) to more easily decode which actions  are being performed by the Strategist multi-sig.
* Please note it is inefficient to move in and out of the Convex strategy frequently and some funds need to always remain outside of Convex in order to accommodate withdrawals.

****
