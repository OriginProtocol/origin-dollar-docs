# Vault

Kasa, protokolün merkezinde yer alır. Kasa, OUSD tokenlarını basmak / kullanmaktan, çeşitli desteklenen stratejiler arasında fonları yeniden dengelemekten ve ödül tokenlarını tasfiye etmekten sorumludur.

Apps Kasası'ndaki herkese açık olarak çağrılabilen en önemli işlevler şunlardır:

* `mint ()`, desteklenen tek bir stabilcoinin OUSD'ye dönüştürülmesine izin verir
* `mintMultiple ()`, desteklenen birden fazla stablecoin'in tek bir çağrıda OUSD'ye dönüştürülmesine izin verir
* `redeem ()`, belirtilen miktarda OUSD'nin desteklenen diğer sabit paralar için kullanılmasına izin verir.
* `redeemAll ()`, bir kullanıcının diğer desteklenen stabilcoinler için OUSD bakiyesinin tamamını kullanmasına izin verir. Verim biriktikçe kullanıcı bakiyeleri sürekli arttığı için bu özellikle yararlıdır.
* `rebase ()`, havuzda o anda depolanan varlıkların değerine göre tüm kullanıcılar için bakiyeleri günceller.
* `tahsis ()`, verimi en üst düzeye çıkarmak ve riski çeşitlendirmek için yönetim altındaki varlıkları öngörülen [Stratejilere](strategies.md) taşır.

Geri alımlarda, kullanıcıya hangi stabilcoin \ (ler) i iade edeceğine karar veren kullanıcı değil protokoldür. Hangi madeni paranın iade edileceğine dair bu karar, havuzda tutulan varlıkların iç oranlarına dayanmaktadır.



