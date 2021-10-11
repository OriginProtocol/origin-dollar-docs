# Fund Management

The OUSD smart contract aggregates all users' stablecoin deposits into a single pool of deployable assets. Funds are then allocated across one or more** **earning strategies at any given moment in time. The Vault favors high-yield strategies but also seeks to maintain diversification across multiple strategies. Diversification removes single points of failures and mitigates risks.

In contrast to Yearn Vaults, TokenSets, or Zapper opportunities, users do not select individual strategies. All deposited stablecoins and consequently all OUSD tokens are fungible. Once our full governance structure is implemented, these decisions will be made with input from OUSD governance token holders. OGN holders are encouraged to participate in creating and voting on proposals that impact the protocol in the [OGN governance portal](https://vote.originprotocol.com).

**Earning Strategies**

Earning strategies put deployed capital to work across various DeFi platforms. The Vault will determine which strategies are active and what percentage of deployed capital they will receive. These strategies will be upgraded and replaced over time.

**Strategist**

The initial version of the OUSD Vault smart contract gives each valid strategy a simple weight between 0% and 100% to perform simple asset allocation. These weights will be shifted often via updates by Origin in the short-term and by decentralized governance in the long-term. 

**Diversification**

Diversification across multiple underlying DeFi [platforms](supported-strategies/) will reduce smart contract and other systemic risks. The smart contract will calculate current and expected APYs in an effort to provide competitive returns to OUSD holders. Over time, the Vault contract will be upgraded to intelligently and autonomously shift between strategies without any manual intervention. For example, the Vault will automatically shift capital between various lending strategies to optimize for yields.

However, it is still expected that certain risk parameters or decisions on whether certain strategies will be included in the automated decision-making engine will be made through governance votes. 
