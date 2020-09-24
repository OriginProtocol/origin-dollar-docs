# Diversification

The initial version of the OUSD Vault smart contract gives each valid strategy a simple weight between 0% and 100% to perform simple asset allocation. These weights will be shifted often via updates by Origin in the short-term and by decentralized governance in the long-term.

Diversification across multiple underlying DeFi [platforms](../supported-strategies/) will reduce smart contract and other systemic risks. The smart contract will calculate current and expected APYs in an effort to provide competitive returns to OUSD holders. Over time, the Vault contract will be upgraded to intelligently and autonomously shift between strategies without any manual intervention. For example, the Vault will automatically shift capital between various lending strategies to optimize for yields.

However, it is still expected that certain risk parameters or decisions on whether certain strategies will be included in the automated decision-making engine will be made through governance votes. 

