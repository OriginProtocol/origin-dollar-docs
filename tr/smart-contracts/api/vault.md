---
description: >-
  Kasa, protokolün merkezinde yer alır. Kasa, OUSD tokenlarını basmak / kullanmaktan, çeşitli desteklenen stratejiler arasında fonları yeniden dengelemekten ve ödül tokenlarını tasfiye etmekten sorumludur.
---

# Kasa

## Yöntemler‌

### mint\(\)<a id="mint"></a>

**`function mint(address _asset, uint256 _amount)`**

`_asset` parametresi ile belirtilen `_tutar` stablecoin depozitosu karşılığında OUSD'yi daraltır. Arayan, **döviz kuru**bağlı olarak belirli miktarda OUSD alır.

| Parametre adı | Tür     | Açıklama                                                                                                                                       |
|:------------- |:------- |:---------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset     | address | [desteklenen](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stabilcoinin adresi |
| \_Miktar    | uint256 | ondalık birimlerle ifade edilen yatırılan miktar                                                                                               |

### mintMultiple\(\)<a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts)`**

Tek bir aramada birden fazla stabilcoin depozitosu karşılığında Mints OUSD. Sabit paralar `_assets` dizi parametresi ve miktarlar `_amounts` dizi parametresi ile belirtilir. Arayan, **döviz kuru**bağlı olarak belirli miktarda OUSD alır.

| Parametre adı      | Tür                   | Açıklama                                                                                                                                       |
|:------------------ |:--------------------- |:---------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets CONTEXT | address\[\] CONTEXT | [desteklenen](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stabilcoinin adresi |
| \_Miktar         | uint256\[\]         | ondalık birimlerle ifade edilen yatırılan miktar                                                                                               |

{% hint style="uyarı" %}
Geri alımlarda, kullanıcıya hangi stabilcoin \ (ler) i iade edeceğine karar veren kullanıcı değil protokoldür. Hangi coin\(ler)in iade edileceğine dair bu karar, havuzda tutulan varlıkların iç oranlarına dayanmaktadır.‌
{% endhint %}

### tazmin etmek\(\) <a id="redeem"></a>

**`function mint(address _asset, uint256 _amount)`**

`_amount` parametresiyle belirtilen OUSD, desteklenen bir veya daha fazla stablecoin karşılığında kullanılır. Alınan stablecoin miktarı **döviz kuru**bağlıdır.

| Parametre adı      | Tür     | Açıklama                                         |
|:------------------ |:------- |:------------------------------------------------ |
| \_amount CONTEXT | uint256 | ondalık birimlerle ifade edilen yatırılan miktar |

### redeemAll \ (\) ‌ <a id="redeemall"></a>

**`function mint(address _asset, uint256 _amount)`**

Kullanıcının sahip olduğu tüm OUSD, desteklenen bir veya daha fazla sabit coin karşılığında kullanılır. Alınan stablecoin miktarı **döviz kuru**bağlıdır.

### rebase\(\) 
<a id="rebase"></a>

**`function rebase()`**‌

rebase (), havuzda o anda depolanan varlıkların değerine göre tüm kullanıcılar için bakiyeleri günceller. `uint256` türüyle temsil edilen dayanak varlıkların ve stratejilerin toplam değerini verir.

### ayırmak \ (\) <a id="allocate"></a>

**`function rebase()`**‌

Verimi en üst düzeye çıkarmak ve riski çeşitlendirmek için yönetim altındaki varlıkları öngörülen [Stratejilere](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) taşır.

### toplam değer\(\) <a id="totalvalue"></a>

**`function rebase()`**‌

Temel varlıkların ve stratejilerin toplam değerini verir.

| `dönüş` isim | Tür     | Açıklama                                                  |
|:------------ |:------- |:--------------------------------------------------------- |
| değer        | uint256 | Temel varlıkların ve stratejilerin toplam değerini verir. |

### checkBalance\(\) 
<a id="checkbalance"></a>

**`function rebase()`**‌

Apps Kasası'nda tutulan`_asset` parametresi ve `uint256` türüyle temsil edilen tüm stratejiler tarafından belirtilen bir öğenin bakiyesini döndürür.

| Parametre adı | Tür   | Açıklama                                                                                                                                       |
|:------------- |:----- |:---------------------------------------------------------------------------------------------------------------------------------------------- |
| \_varlık    | adres | [desteklenen](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stabilcoinin adresi |

### calculateRedeemOutputs \ (\) <a id="calculateredeemoutputs"></a>

**`function mint(address _asset, uint256 _amount)`**

`redeem` işlevinin `_amount` parametresi tarafından belirtilen belirli miktarda OUSD paraya çevrildiğinde döndüreceği stabilcoin karışımını hesaplayın. Bir dizi stablecoin değeri döndürür.

Stabilcoin değerlerini doğru stabilcoin para birimine atfetmek için bu çağrı, bir stabilcoin adresi dizisi döndüren `getAllAssets` fonksiyonu ile birlikte kullanılmalıdır.

`calculateRedeemOutputs` tarafından döndürülen bir dizinin dizini, `getAllAssets` işlevi tarafından döndürülen bir dizideki aynı dizine sahip stabilcoin adresine karşılık gelir.

| Parametre adı | Tür     | Açıklama                                         |
|:------------- |:------- |:------------------------------------------------ |
| \_Miktar    | uint256 | ondalık birimlerle ifade edilen yatırılan miktar |

| `dönüş` isim | Tür           | Açıklama                                                                 |
|:------------ |:------------- |:------------------------------------------------------------------------ |
| çıktılar     | uint256\[\] | stabilcoin varlıklarının miktarı dizisi `paraya çevirme` işlevi döndürür |

### getAssetCount \ (\) <a id="getassetcount"></a>

**`function rebase()`**‌

`uint256` türü ile temsil edilen desteklenen stablecoin varlıklarının sayısını döndürün.

### getAllAssets \ (\) <a id="getallassets"></a>

**`function rebase()`**‌

`uint256` türü ile temsil edilen desteklenen stablecoin varlıklarının sayısını döndürün.

### getStrategyCount \ (\) ‌ <a id="getstrategycount"></a>

**`function rebase()`**‌

`uint256` türü ile temsil edilen desteklenen stablecoin varlıklarının sayısını döndürün.

### getAPR \ (\) <a id="getapr"></a>

**`function rebase()`**‌

Apps Kasası ve `uint256` türüyle temsil edilen tüm Stratejilerin toplam yıllık yüzde getirisini \ (APR \) getirin. Ortaya çıkan numarada 18 ondalık boşluk vardır.

### isSupportedAsset \ (\) <a id="issupportedasset"></a>

**`isSupportedAsset (adres _asset)`**

`_asset` parametresiyle belirtilen öğe Apps Kasası tarafından destekleniyorsa doğru olan boole değerini döndürür.

| Parametre adı | Tür   | Açıklama             |
|:------------- |:----- |:-------------------- |
| \_varlık    | adres | Stabilcoin'in adresi |

### fiyatUSDMint \ (\) <a id="issupportedasset-1"></a>

**`function mint(address _asset, uint256 _amount)`**

`uint256` türüyle temsil edilen OUSD basarken kullanılan `sembolü` parametreleri tarafından belirtilen sabit bir madeni paranın döviz kuru fiyatını döndürür. Ortaya çıkan numarada 18 ondalık boşluk vardır.

| Parametre adı | Tür  | Açıklama              |
|:------------- |:---- |:--------------------- |
| sembol        | dizi | Stabilcoin'in sembolü |

### fiyatUSDRedeem \ (\) <a id="issupportedasset-2"></a>

**`function mint(address _asset, uint256 _amount)`**

`uint256` türüyle temsil edilen OUSD basarken kullanılan `sembolü` parametreleri tarafından belirtilen sabit bir madeni paranın döviz kuru fiyatını döndürür. Ortaya çıkan numarada 18 ondalık boşluk vardır.

| Parametre adı | Tür  | Açıklama              |
|:------------- |:---- |:--------------------- |
| sembol        | dizi | Stabilcoin'in sembolü |

### priceAssetUSDMint \ (\) ‌ <a id="issupportedasset-3"></a>

**`function mint(address _asset, uint256 _amount)`**

`uint256` türüyle temsil edilen OUSD basarken kullanılan `sembolü` parametreleri tarafından belirtilen sabit bir madeni paranın döviz kuru fiyatını döndürür. Ortaya çıkan numarada 18 ondalık boşluk vardır.

| Parametre adı | Tür     | Açıklama              |
|:------------- |:------- |:--------------------- |
| \_varlık    | address | Stabilcoin'in adresi‌ |

### priceAssetUSDRedeem \ (\) ‌ <a id="issupportedasset-3-1"></a>

**`function mint(address _asset, uint256 _amount)`**

`uint256` türüyle temsil edilen OUSD basarken kullanılan `sembolü` parametreleri tarafından belirtilen stabil coinin döviz kuru fiyatını döndürür. Ortaya çıkan numarada 18 ondalık boşluk vardır.

| Parametre adı | Tür   | Açıklama             |
|:------------- |:----- |:-------------------- |
| \_varlık    | adres | Stabilcoin'in adresi |

