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

### allocate\(\) 
<a id="allocate"></a>

**`function allocate()`**‌

Moves the assets under management into their prescribed [Stategies](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) to maximize yield and diversify risk.‌

### totalValue\(\) <a id="totalvalue"></a>

**`function totalValue()`**‌

Returns total value of underlying assets and strategies.

| `return` name | Type    | Description                                      |
|:------------- |:------- |:------------------------------------------------ |
| value         | uint256 | total value of underlying assets and strategies. |

### checkBalance\(\) <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Returns the balance of an asset specified by the`_asset` parameter held in Vault and all strategies represented by `uint256` type.

| Parameter Name | Type    | Description                                                                                                                                        |
|:-------------- |:------- |:-------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset      | address | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |

### calculateRedeemOutputs\(\) <a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount` parameter. Returns an array of stablecoin values.

To attribute the stablecoin values to the correct stablecoin currency this call should be used in conjunction with `getAllAssets` function that returns an array of stablecoin addresses.

The index of an array that is returned by the `calculateRedeemOutputs` corresponds to the stablecoin address with the same index in an array returned by the `getAllAssets` function.

| Parameter Name | Type    | Description                               |
|:-------------- |:------- |:----------------------------------------- |
| \_amount     | uint256 | amount of OUSD expressed in decimal units |

| `return` name | Type          | Description                                                                 |
|:------------- |:------------- |:--------------------------------------------------------------------------- |
| outputs       | uint256\[\] | array of the amount of the stablecoin assets `redeem` function would return |

### getAssetCount\(\) <a id="getassetcount"></a>

**`function getAssetCount()`**‌

Return the number of supported stablecoin assets represented by `uint256` type.‌

### getAllAssets\(\) <a id="getallassets"></a>

**`function getAllAssets()`**‌

Return all assets addresses of supported stablecoin assets in order represented by `uint256` type.‌

### getStrategyCount\(\)‌ <a id="getstrategycount"></a>

**`function getStrategyCount()`**‌

Return the number of strategies active on the Vault represented by `uint256` type.‌

### getAPR\(\) <a id="getapr"></a>

**`function getAPR()`**‌

Return the total annual percentage yield \(APR\) of the Vault and all Strategies represented by `uint256` type. Resulting number has 18 decimal spaces.‌

### isSupportedAsset\(\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Return the boolean that is true if the asset specified by the `_asset` parameter is supported by the Vault.

| Parameter Name | Type    | Description               |
|:-------------- |:------- |:------------------------- |
| \_asset      | address | Address of the stablecoin |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type   | Description              |
|:-------------- |:------ |:------------------------ |
| symbol         | string | Symbol of the stablecoin |

### priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type   | Description              |
|:-------------- |:------ |:------------------------ |
| symbol         | string | Symbol of the stablecoin |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type    | Description                |
|:-------------- |:------- |:-------------------------- |
| \_asset      | address | Address of the stablecoin‌ |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type    | Description               |
|:-------------- |:------- |:------------------------- |
| \_asset      | address | Address of the stablecoin |

