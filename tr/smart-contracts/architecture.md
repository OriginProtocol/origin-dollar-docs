# Mimari

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD, bir dizi akıllı sözleşmeden oluşur. Bu sözleşmelerin her biri, yönetişim protokolleri aracılığıyla yükseltilebilen bir vekil sözleşmesine sarılmıştır.

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. ERC-20 sözleşmesi, bir bakiyeyi görüntülerken veya cüzdanlar arasında bir transfer başlatırken USD şartlarına dönüştürmeyi ele alır.

[Vault](api/vault.md) , OUSD'nin basılması ve yakılmasından sorumludur. Ayrıca, desteklenen [ Stratejileri ](../core-concepts/supported-strategies/) 'nin her birine dağıtılan varlıkların yüzdesini de uygular. Depo, gaz maliyetlerini optimize etmek için, çoğu biriktirme ve itfanın varlıkları stratejilerden sarmadan / çözmeden gerçekleşmesine izin veren bir tampon bulundurur.



