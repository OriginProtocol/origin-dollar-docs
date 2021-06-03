# Rebasing & Hợp đồng thông minh

Nếu bạn đang sử dụng ví đa chữ ký hoặc hợp đồng thông minh khác muốn tham gia rebasing OUSD thì bạn phải gọi hàm`rebaseOptIn ()` OUSD. Điều này chỉ áp dụng với hợp đồng thông minh vì ví EOA tiêu chuẩn được đăng ký tự động.

{% hint style="info" %}
Ví nhiều đa chữ ký hoặc các hợp đồng thông minh khác phải gọi`rebaseOptIn ()`để kiếm được lợi nhuận.
{% endhint %}

By default, OUSD that is held on smart contracts will not participate in the rebasing nature of the token and will forfeit any yield unless the smart contract explicitly opts-in. This increases the composability of OUSD within DeFi as many protocols weren't designed with the expectation that balances might change. To other DeFi protocols, OUSD works just like any other normal, well-behaved ERC-20 until you ask it to change. This is a particularly useful attribute for automated market makers \(AMM’s\) like Uniswap which break when the number of tokens they are holding changes unexpectedly.

Smart contracts must explicitly opt-in to receiving yield via the rebasing mechanism. This fixes the issue with the expanding supply on AMM’s while still allowing multi-sig wallets and other smart contracts the opportunity to still participate and earn yield.

{% hint style="warning" %}
If you are deploying a contract and intend to call`rebaseOptIn()`to earn yield you cannot call it from the contract's constructor. The contract must be deployed before it can be called.
{% endhint %}

If you are using a multi-sig wallet like [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) or [Gnosis Safe](https://gnosis-safe.io/), you will need the [proxy contract address for OUSD](../../smart-contracts/registry.md) and the corresponding [ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Once you add those, you will be able to call the `rebaseOptIn()` function to opt into receiving yield via rebasing or`rebaseOptOut()` to turn it off again.





