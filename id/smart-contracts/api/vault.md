---
description: >-
  Vault adalah inti dari protokol. Vault bertanggung jawab untuk mencetak / menebus token OUSD, menyeimbangkan kembali dana antara berbagai strategi yang didukung, dan melikuidasi token hadiah.
---

# Vault

## Unit

Semua jumlah OUSD yang diteruskan atau dikembalikan oleh metode Vault menggunakan 18 tempat desimal. Misalnya, 1 OUSD dinyatakan sebagai 1000000000000000000.

Untuk koin stabil lainnya, jumlah tempat desimal bervariasi. DAI menggunakan 18 tempat desimal sedangkan USDC dan USDT hanya menggunakan 6.

## Metode‌

### cetak\(\) <a id="mint"></a>

**`fungsi cetak(address _asset, uint256 _amount, uint256 _minimumOusdAmount)`**

Cetak OUSD dengan imbalan setoran sejumlah `_ jumlah` stablecoin yang ditentukan oleh parameter `_asset`. Penelepon menerima sejumlah OUSD tergantung pada **nilai tukar**.

| Nama Parameter        | Tipe    | Deskripsi                                                                                                                                       |
|:--------------------- |:------- |:----------------------------------------------------------------------------------------------------------------------------------------------- |
| \_aset              | alamat  | Alamat dari [didukung](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoins |
| \_jumlah            | uint256 | Jumlah yang disimpan, dinyatakan dalam unit desimal                                                                                             |
| \_minimumOusdAmount | uint256 | Jumlah minimum OUSD yang bersedia diterima oleh penelepon. Panggilan ke cetak\(\) kembali jika minimum tidak terpenuhi.                       |

### mintMultiple \ (\) <a id="mintmultiple"></a>

**`fungsi cetak(address _asset, uint256 _amount, uint256 _minimumOusdAmount)`**

Cetak OUSD dengan imbalan setoran beberapa stablecoin dalam satu panggilan. Stablecoin ditentukan oleh parameter array `_aset` dan jumlahnya oleh parameter array `_jumlah`. Pemanggil menerima sejumlah OUSD tergantung pada **nilai tukar**.

| Nama Parameter        | Tipe            | Deskripsi                                                                                                                                       |
|:--------------------- |:--------------- |:----------------------------------------------------------------------------------------------------------------------------------------------- |
| \_aktiva            | alamat\[\]    | Alamat dari [didukung](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoins |
| \_jumlah            | uint256 \ [\] | Jumlah yang disimpan, dinyatakan dalam unit desimal                                                                                             |
| \_minimumOusdAmount | uint256         | Jumlah minimum OUSD yang bersedia diterima oleh pemanggil. Panggilan ke cetak\(\) kembali jika minimum tidak terpenuhi.                       |

{% hint style="warning" %}
Saat penebusan, adalah protokol dan bukan pengguna yang memutuskan stablecoin \ (s \) mana yang akan dikembalikan ke pengguna. Keputusan tentang coin mana \(s\) yang akan dikembalikan didasarkan pada rasio internal dari aset yang disimpan di vault.‌
{% endhint %}

### menebus\(\) <a id="redeem"></a>

**`fungsi tebus (uint256 _jumlah)`**

OUSD yang ditentukan oleh parameter `_amount` ditukarkan dengan satu atau beberapa stablecoin yang didukung. Jumlah stablecoin yang diterima bergantung pada **nilai tukar**.

| Nama Parameter | Tipe    | Deskripsi                                                |
|:-------------- |:------- |:-------------------------------------------------------- |
| \_jumlah     | uint256 | jumlah OUSD yang disimpan, dinyatakan dalam unit desimal |

### tebusSemua \ (\) ‌ <a id="redeemall"></a>

**`fungsi redeemAll ()`**

Semua OUSD yang dimiliki pengguna ditebus dengan satu atau beberapa stablecoin yang didukung. Jumlah stablecoin yang diterima bergantung pada **nilai tukar**.

### rebase \ (\) <a id="rebase"></a>

**`fungsi rebase ()`**

Memperbarui saldo untuk semua pengguna berdasarkan nilai aset yang saat ini disimpan di vault. Mengembalikan nilai total aset dan strategi pokok yang diwakili oleh `uint256` jenis.‌

### alokasikan \ (\) <a id="allocate"></a>

**`fungsi mengalokasikan ()`**

Pindahkan aset di bawah manajemen ke dalam preskripsi mereka [ Strategi](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) untuk memaksimalkan hasil dan diversifikasi resiko

### nilai total\(\) <a id="totalvalue"></a>

**`fungsi totalValue ()`**

Mengembalikan nilai total aset dan strategi yang mendasarinya.

| `kembali` nama | Tipe    | Deskripsi                                        |
|:-------------- |:------- |:------------------------------------------------ |
| nilai          | uint256 | nilai total aset dan strategi yang mendasarinya. |

### checkBalance \ (\) <a id="checkbalance"></a>

**`fungsi checkBalance (address _asset)`**

Mengembalikan saldo aset yang ditentukan oleh`_asset` parameter yang disimpan di Vault dan semua strategi yang diwakili oleh `uint256` tipe.

| Nama Parameter | Tipe   | Deskripsi                                                                                                                                       |
|:-------------- |:------ |:----------------------------------------------------------------------------------------------------------------------------------------------- |
| \_aset       | alamat | Alamat dari [didukung](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoins |

### hitungjumlahpenebusan \ (\) <a id="calculateredeemoutputs"></a>

**`fungsi countRedeemOutputs(uint256 _amount)`**

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount` parameter. Returns an array of stablecoin values.

To attribute the stablecoin values to the correct stablecoin currency this call should be used in conjunction with `getAllAssets` function that returns an array of stablecoin addresses.

The index of an array that is returned by the `calculateRedeemOutputs` corresponds to the stablecoin address with the same index in an array returned by the `getAllAssets` function.

| Nama Parameter | Tipe    | Deskripsi                                                |
|:-------------- |:------- |:-------------------------------------------------------- |
| \_jumlah     | uint256 | jumlah OUSD yang disimpan, dinyatakan dalam unit desimal |

| `kembali` nama | Tipe            | Deskripsi                                                 |
|:-------------- |:--------------- |:--------------------------------------------------------- |
| keluaran       | uint256 \ [\] | array jumlah fungsi aset stablecoin `redeem` akan kembali |

### getAssetCount \ (\) <a id="getassetcount"></a>

**`function getAssetCount()`**‌

Return the number of supported stablecoin assets represented by `uint256` type.‌

### getAllAssets \ (\) <a id="getallassets"></a>

**`function getAllAssets()`**‌

Return all assets addresses of supported stablecoin assets in order represented by `uint256` type.‌

### dapatkanPerhitunganStrategi \ (\) ‌ <a id="getstrategycount"></a>

**`function getStrategyCount()`**‌

Return the number of strategies active on the Vault represented by `uint256` type.‌

### dapatkanAPR \ (\) <a id="getapr"></a>

**`function getAPR()`**‌

Return the total annual percentage yield \(APR\) of the Vault and all Strategies represented by `uint256` type. Resulting number has 18 decimal places.‌

### adalahAsetyangdidukung \ (\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Return the boolean that is true if the asset specified by the `_asset` parameter is supported by the Vault.

| Nama Parameter | Tipe   | Deskripsi         |
|:-------------- |:------ |:----------------- |
| \_aset       | alamat | Alamat stablecoin |

### hargaUSDMint \ (\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nama Parameter | Tipe | Deskripsi         |
|:-------------- |:---- |:----------------- |
| simbol         | tali | Simbol stablecoin |

### hargatebusUSD \ (\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nama Parameter | Tipe | Deskripsi         |
|:-------------- |:---- |:----------------- |
| simbol         | tali | Simbol stablecoin |

### priceAssetUSDMint \ (\) ‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nama Parameter | Tipe   | Deskripsi          |
|:-------------- |:------ |:------------------ |
| \_aset       | alamat | Alamat stablecoin‌ |

### priceAssetUSDRedeem \ (\) ‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nama Parameter | Tipe   | Deskripsi         |
|:-------------- |:------ |:----------------- |
| \_aset       | alamat | Alamat stablecoin |

