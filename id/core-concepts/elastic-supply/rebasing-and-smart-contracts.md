# Rebasing & Kontrak Cerdas

Jika Anda menggunakan dompet multi-sig atau kontrak pintar lain yang ingin berpartisipasi dalam aspek rebasing OUSD, Anda harus memanggil fungsi`rebaseOptIn()` OUSD. Ini hanya berlaku untuk kontrak pintar karena dompet EOA standar didaftarkan secara otomatis.

{% hint style="info" %}
Dompet multi-sig atau kontrak pintar lainnya harus memanggil`rebaseOptIn()`untuk mendapatkan hasil.
{% endhint %}

Secara default, OUSD yang diadakan pada kontrak pintar tidak akan berpartisipasi dalam sifat rebasing token dan akan kehilangan hasil apa pun kecuali kontrak pintar secara eksplisit ikut serta. Ini meningkatkan komposisi OUSD dalam DeFi karena banyak protokol tidak dirancang dengan harapan bahwa saldo mungkin berubah. Untuk protokol DeFi lainnya, OUSD berfungsi seperti ERC-20 normal lainnya yang berperilaku baik hingga Anda memintanya untuk mengubahnya. This is a particularly useful attribute for automated market makers (AMM’s) like Uniswap which break when the number of tokens they are holding changes unexpectedly.

![The Gnosis Safe OUSD app will prompt you to opt in to yield](../../.gitbook/assets/ousd-app-in-gnosis-safe.png)

Smart contracts must explicitly opt-in to receiving yield via the rebasing mechanism. This fixes the issue with the expanding supply on AMM’s while still allowing multi-sig wallets and other smart contracts the opportunity to still participate and earn yield.

{% hint style="warning" %}
If you are deploying a contract and intend to call`rebaseOptIn()`to earn yield you cannot call it from the contract's constructor. The contract must be deployed before it can be called.
{% endhint %}

[Gnosis Safe](https://gnosis-safe.io) users are encouraged to use the Origin Dollar app which will prompt you to opt in to receiving yield. If you are using the "Old" [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) or another contract-based wallet, you will need the [proxy contract address for OUSD](../../smart-contracts/registry.md) and the corresponding [ABI](https://api.etherscan.io/api?module=contract\&action=getabi\&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Once you add those, you will be able to call the `rebaseOptIn()` function to opt into receiving yield via rebasing or`rebaseOptOut()` to turn it off again.



