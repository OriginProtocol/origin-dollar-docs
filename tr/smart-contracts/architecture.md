# Mimari

![](../.gitbook/assets/ousd_docs_graphics\_3.png)

OUSD, bir dizi akıllı sözleşmeden oluşur. Bu sözleşmelerin her biri, yönetişim protokolleri aracılığıyla yükseltilebilen bir vekil sözleşmesine sarılmıştır.

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. ERC-20 sözleşmesi, bir bakiyeyi görüntülerken veya cüzdanlar arasında bir transfer başlatırken USD şartlarına dönüştürmeyi ele alır.

[Vault](api/vault.md) , OUSD'nin basılması ve yakılmasından sorumludur. Ayrıca, desteklenen [ Stratejileri ](../core-concepts/supported-strategies/) 'nin her birine dağıtılan varlıkların yüzdesini de uygular. Depo, gaz maliyetlerini optimize etmek için, çoğu biriktirme ve itfanın varlıkları stratejilerden sarmadan / çözmeden gerçekleşmesine izin veren bir tampon bulundurur.

OUSD Swap, aka "Flipper" is a smart contract that is provided by Origin for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. This contract is used as an alternative way to route user transactions originating from the web app. It's important to note that this contract may become bankrupt on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Origin Swap uses around 45% less gas than Uniswap v3 due to its simplicity.

