# Управление средствами

Смарт-контракт OUSD объединяет все задепонированные стейблкоины пользователей в единый пул инвестиционных активов. Затем средства распределяются по одной или нескольким стратегиям получения прибыли**** в любой момент времени. Vault отдает предпочтение высокодоходным стратегиям, но также стремится поддерживать диверсификацию по нескольким стратегиям. Диверсификация устраняет единые точки сбоя и снижает риски.

В отличие от Yearn Vaults, TokenSets или Zapper, пользователи не выбирают индивидуальные стратегии. All deposited stablecoins and consequently all OUSD tokens are fungible.

**Earning Strategies**

Earning strategies put deployed capital to work across various DeFi platforms. The Vault will determine which strategies are active and what percentage of deployed capital they will receive. These strategies will be upgraded and replaced over time.

**Strategist**

The initial version of the OUSD Vault smart contract gives each valid strategy a simple weight between 0% and 100% to perform simple asset allocation. These weights will be shifted often via updates by Origin in the short-term and by decentralized governance in the long-term.

**Diversification**

Diversification across multiple underlying DeFi [platforms](supported-strategies/) will reduce smart contract and other systemic risks. The smart contract will calculate current and expected APYs in an effort to provide competitive returns to OUSD holders. Over time, the Vault contract will be upgraded to intelligently and autonomously shift between strategies without any manual intervention. For example, the Vault will automatically shift capital between various lending strategies to optimize for yields.

However, it is still expected that certain risk parameters or decisions on whether certain strategies will be included in the automated decision-making engine will be made through governance votes. 

