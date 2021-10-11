---
description: >-
  Vault adalah inti dari protokol. Vault bertanggung jawab untuk mencetak / menebus token OUSD, menyeimbangkan kembali dana antara berbagai strategi yang didukung, dan melikuidasi token hadiah.
---

# Vault

## Unit

Semua jumlah OUSD yang diteruskan atau dikembalikan oleh metode Vault menggunakan 18 tempat desimal. Misalnya, 1 OUSD dinyatakan sebagai 1000000000000000000.

Untuk koin stabil lainnya, jumlah tempat desimal bervariasi. DAI menggunakan 18 tempat desimal sedangkan USDC dan USDT hanya menggunakan 6.

Efforts are [currently underway](https://github.com/OriginProtocol/origin-dollar/issues/590) to increase the resolution of rebasing calculations from 18 decimals to 27 decimals. The OUSD token itself will still retain 18 decimals of precision and user balances should not change.

## Metode‌

### mint() <a href="mint" id="mint"></a>

**`function mint(address _asset, uint256 _amount, uint256 _minimumOusdAmount)`**‌

Mints OUSD in exchange for a deposit of a certain `_amount` of stablecoin specified by the `_asset` parameter. The caller receives a certain amount of OUSD depending on the **exchange rate**.

| Nama Parameter        | Tipe    | Deskripsi                                                                                                                                            |
| --------------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_aset              | alamat  | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |
| \_jumlah            | uint256 | Jumlah yang disimpan, dinyatakan dalam unit desimal                                                                                                  |
| \_minimumOusdAmount | uint256 | Jumlah minimum OUSD yang bersedia diterima oleh penelepon. The call to mint() reverts if the minimum is not met.                                     |

### mintMultiple() <a href="mintmultiple" id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts, uint256 _minimumOusdAmount)`**‌

Mints OUSD in exchange for a deposit of multiple stablecoins in a single call. Stablecoins are specified by the `_assets` array parameter and the amounts by the `_amounts` array parameter. The caller receives a certain amount of OUSD depending on the **exchange rate**.

| Nama Parameter        | Tipe        | Deskripsi                                                                                                                                               |
| --------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_aktiva            | address\[] | Addresses of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoins |
| \_jumlah            | uint256\[] | Jumlah yang disimpan, dinyatakan dalam unit desimal                                                                                                     |
| \_minimumOusdAmount | uint256     | Jumlah minimum OUSD yang bersedia diterima oleh pemanggil. The call to mint() reverts if the minimum is not met.                                        |

{% hint style="warning" %}
On redemptions, it is the protocol and not the user that decides which stablecoin(s) are returned to the user. This decision of which coin(s) to return is based on the internal ratios of the assets that are being held in the vault.‌
{% endhint %}

### redeem() <a href="redeem" id="redeem"></a>

**`function redeem(uint256 _amount)`**‌

OUSD specified by the `_amount` parameter is redeemed in exchange for one or multiple supported stablecoins. Amount of stablecoins received depends on the **exchange rate**.

| Nama Parameter | Tipe    | Deskripsi                                                |
| -------------- | ------- | -------------------------------------------------------- |
| \_jumlah     | uint256 | jumlah OUSD yang disimpan, dinyatakan dalam unit desimal |

### redeemAll()‌ <a href="redeemall" id="redeemall"></a>

**`function redeemAll()`**‌

All OUSD in user's possession is redeemed in exchange for one or multiple supported stablecoins. Amount of stablecoins received depends on the **exchange rate**.

### rebase() <a href="rebase" id="rebase"></a>

**`function rebase()`**‌

Updates the balances for all users based on the value of the assets currently stored in the vault. Returns total value of the underlying assets and strategies represented by `uint256` type.‌

### allocate() <a href="allocate" id="allocate"></a>

**`function allocate()`**‌

Moves the assets under management into their prescribed [Stategies](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) to maximize yield and diversify risk.‌

### totalValue() <a href="totalvalue" id="totalvalue"></a>

**`function totalValue()`**‌

Returns total value of underlying assets and strategies.

| `kembali` nama | Tipe    | Deskripsi                                        |
| -------------- | ------- | ------------------------------------------------ |
| nilai          | uint256 | nilai total aset dan strategi yang mendasarinya. |

### checkBalance() <a href="checkbalance" id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Returns the balance of an asset specified by the`_asset` parameter held in Vault and all strategies represented by `uint256` type.

| Nama Parameter | Tipe   | Deskripsi                                                                                                                                            |
| -------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_aset       | alamat | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |

### calculateRedeemOutputs() <a href="calculateredeemoutputs" id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount` parameter. Returns an array of stablecoin values.

To attribute the stablecoin values to the correct stablecoin currency this call should be used in conjunction with `getAllAssets` function that returns an array of stablecoin addresses.

The index of an array that is returned by the `calculateRedeemOutputs` corresponds to the stablecoin address with the same index in an array returned by the `getAllAssets` function.

| Nama Parameter | Tipe    | Deskripsi                                                |
| -------------- | ------- | -------------------------------------------------------- |
| \_jumlah     | uint256 | jumlah OUSD yang disimpan, dinyatakan dalam unit desimal |

| `kembali` nama | Tipe        | Deskripsi                                                 |
| -------------- | ----------- | --------------------------------------------------------- |
| keluaran       | uint256\[] | array jumlah fungsi aset stablecoin `redeem` akan kembali |

### getAssetCount() <a href="getassetcount" id="getassetcount"></a>

**`function getAssetCount()`**‌

Return the number of supported stablecoin assets represented by `uint256` type.‌

### getAllAssets() <a href="getallassets" id="getallassets"></a>

**`function getAllAssets()`**‌

Return all assets addresses of supported stablecoin assets in order represented by `uint256` type.‌

### getStrategyCount()‌ <a href="getstrategycount" id="getstrategycount"></a>

**`function getStrategyCount()`**‌

Return the number of strategies active on the Vault represented by `uint256` type.‌

### getAPR() <a href="getapr" id="getapr"></a>

**`function getAPR()`**‌

Return the total annual percentage yield (APR) of the Vault and all Strategies represented by `uint256` type. Resulting number has 18 decimal places.‌

### isSupportedAsset() <a href="issupportedasset" id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Return the boolean that is true if the asset specified by the `_asset` parameter is supported by the Vault.

| Nama Parameter | Tipe   | Deskripsi         |
| -------------- | ------ | ----------------- |
| \_aset       | alamat | Alamat stablecoin |

### priceUSDMint() <a href="issupportedasset-1" id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nama Parameter | Tipe | Deskripsi         |
| -------------- | ---- | ----------------- |
| simbol         | tali | Simbol stablecoin |

### priceUSDRedeem() <a href="issupportedasset-2" id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nama Parameter | Tipe | Deskripsi         |
| -------------- | ---- | ----------------- |
| simbol         | tali | Simbol stablecoin |

### priceAssetUSDMint()‌ <a href="issupportedasset-3" id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nama Parameter | Tipe   | Deskripsi          |
| -------------- | ------ | ------------------ |
| \_aset       | alamat | Alamat stablecoin‌ |

### priceAssetUSDRedeem()‌ <a href="issupportedasset-3-1" id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nama Parameter | Tipe   | Deskripsi         |
| -------------- | ------ | ----------------- |
| \_aset       | alamat | Alamat stablecoin |
