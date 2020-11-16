# Rebasing & Smart Contracts

If you are using a multi-sig wallet or another smart contract that wishes to participate in the rebasing aspect of OUSD you must call OUSD’s`rebaseOptIn()` function. This only applies to smart contracts as standard EOA wallets are enrolled automatically.

{% hint style="info" %}
Multi-sig wallets or other smart contracts must call`rebaseOptIn()`to earn yield.
{% endhint %}

One of the challenges with rebasing currencies like OUSD is that they don’t work very well with automated market makers \(AMM’s\) like Uniswap or Balancer. These decentralized exchanges rely on supply and demand to determine the price of the assets being traded. It messes up the math when the amount of OUSD held by the contract changes unexpectedly due to new yield being generated. 

We previously added a [bandaid](https://medium.com/originprotocol/upgrades-to-the-ousd-smart-contracts-deliver-higher-yield-and-better-uniswap-support-aa592e51d3f2) that called Uniswap’s `sync()` function every time a `rebase()` was triggered on OUSD’s contracts. While this prevented users from seeing an ugly error message when they tried to trade OUSD on Uniswap, it still introduced loss into the system. After calling sync, Uniswap detects that there is more OUSD than USDT in the vault, which incorrectly pushes down the price of OUSD relative to USDT. While we can count on arbitrageurs to correct the price, it’s better if we can avoid this loss altogether. Given the ever-growing number of competitive AMM’s and forks of Uniswap, it would quickly become infeasible, not to mention gas-expensive, to try and special-case all of them.

After much discussion, we decided that the most scalable solution was to make smart contracts explicitly opt-in to receiving yield via the rebasing mechanism. This fixes the issue with the expanding supply on AMM’s while still allowing multi-sig wallets and other smart contracts the opportunity to still participate and earn yield.

If you are using a multi-sig wallet like [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) or [Gnosis Safe](https://gnosis-safe.io/), you will need the latest [implementation contract address for OUSD](../../smart-contracts/registry.md) and the corresponding [ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Once you add those, you will be able to call the `rebaseOptIn()` function to opt into receiving yield via rebasing or`rebaseOptOut()` to turn it off again.

{% hint style="warning" %}
If you are deploying a contract and intend to call`rebaseOptIn()`to earn yield you cannot call it from the contracts constructor. The contract must be deployed before it can be called.
{% endhint %}

[ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)

