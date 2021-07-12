# Genel Bakış

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD, bir dizi akıllı sözleşmeden oluşur. Bu sözleşmelerin her biri, yönetişim protokolleri aracılığıyla yükseltilebilen bir vekil sözleşmesine sarılmıştır.

Dahili olarak, havuzdaki sahiplik, her bir sahip için havuzun sahiplik yüzdesini temsil eden bir kredi sistemi kullanılarak izlenir. ERC-20 sözleşmesi, bir bakiyeyi görüntülerken veya cüzdanlar arasında bir transfer başlatırken USD şartlarına dönüştürmeyi ele alır.

Kasa, OUSD'yi basmaktan ve yakmaktan sorumludur. Ayrıca, desteklenen [ Stratejileri ](../core-concepts/supported-strategies/) 'nin her birine dağıtılan varlıkların yüzdesini de uygular. Depo, gaz maliyetlerini optimize etmek için, çoğu biriktirme ve itfanın varlıkları stratejilerden sarmadan / çözmeden gerçekleşmesine izin veren bir tampon bulundurur.



