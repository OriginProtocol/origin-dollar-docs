# Elastik Tedarik

**Elastik Tedarik. Sabit Fiyat.**

OUSD, çoğu tokendan farklı çalışır. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Bunun yerine, sözleşmeler parasal arzı sürekli olarak ayarlar ve her bir token sahibinin cüzdanındaki bakiyeyi protokol tarafından kazanılan verimi yansıtacak şekilde otomatik olarak günceller.

{% hint style="bilgi" %}
Banka hesabınıza faiz tahakkuk ettiğini düşünün. ABD dolarının hesap birimi ve değeri değişmez. Faiz kazandıkça zamanla daha fazla ABD doları kazanırsınız.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD is 100% backed by other stablecoins and does not have the same challenge maintaining the peg to the dollar. OUSD'yi basmanın ve paraya çevirmenin kolaylığı göz önüne alındığında, pegin korunmasını sağlamak için arbitrajcılara güvenebiliriz.
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.
