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

Hitung campuran stablecoin yang akan dikembalikan oleh fungsi `redeem` saat menebus sejumlah OUSD yang ditentukan oleh parameter `_amount`. Mengembalikan himpunan nilai stablecoin.

Untuk menghubungkan nilai stablecoin ke mata uang stablecoin yang benar, panggilan ini harus digunakan bersama dengan `fungsi getAllAssets` yang mengembalikan himpunan alamat stablecoin.

Indeks array yang dikembalikan oleh `countRedeemOutputs` sesuai dengan alamat stablecoin dengan indeks yang sama dalam array yang dikembalikan oleh fungsi `getAllAssets`.

| Nama Parameter | Tipe    | Deskripsi                                                |
|:-------------- |:------- |:-------------------------------------------------------- |
| \_jumlah     | uint256 | jumlah OUSD yang disimpan, dinyatakan dalam unit desimal |

| `kembali` nama | Tipe            | Deskripsi                                                 |
|:-------------- |:--------------- |:--------------------------------------------------------- |
| keluaran       | uint256 \ [\] | array jumlah fungsi aset stablecoin `redeem` akan kembali |

### getAssetCount \ (\) <a id="getassetcount"></a>

**`fungsi rebase ()`**

Kembalikan jumlah aset stablecoin yang didukung yang diwakili oleh `uint256` jenis.‌

### getAllAssets \ (\) <a id="getallassets"></a>

**`fungsi getAllAssets()`**

Kembalikan jumlah aset stablecoin yang didukung yang diwakili oleh `uint256` tipe.‌

### dapatkanPerhitunganStrategi \ (\) ‌ <a id="getstrategycount"></a>

**`fungsi getStrategyCount()`**

Kembalikan jumlah strategi aktif di Vault yang yang diwakili oleh tipe `uint256`.‌

### dapatkanAPR \ (\) <a id="getapr"></a>

**`fungsi dapatkanAPR ()`**

Kembalikan total hasil persentase tahunan \ (APR \) Vault dan semua Strategi yang diwakili oleh tipe `uint256`. Angka yang dihasilkan memiliki 18 desimal.‌

### adalahAsetyangdidukung \ (\) <a id="issupportedasset"></a>

**`fungsi adalahAsetyangdidukung (address _asset)`**

Kembalikan boolean yang benar jika aset yang ditentukan oleh parameter `_aset` didukung oleh Vault.

| Nama Parameter | Tipe   | Deskripsi         |
|:-------------- |:------ |:----------------- |
| \_aset       | alamat | Alamat stablecoin |

### hargaUSDMint \ (\) <a id="issupportedasset-1"></a>

**`fungsi priceAssetUSDMint (alamat _asset)`**

Mengembalikan harga nilai tukar stablecoin yang ditentukan oleh `simbol` parameter yang digunakan saat mencetak OUSD yang diwakili oleh tipe ` uint256`. Angka yang dihasilkan memiliki 18 desimal.

| Nama Parameter | Tipe | Deskripsi         |
|:-------------- |:---- |:----------------- |
| simbol         | tali | Simbol stablecoin |

### hargatebusUSD \ (\) <a id="issupportedasset-2"></a>

**`fungsi hargaUSDRedeem (alamat _asset)`**

Mengembalikan harga nilai tukar koin stabil yang ditentukan oleh simbol `` parameter yang digunakan saat menukarkan OUSD yang diwakili oleh `tipe uint256`. Angka yang dihasilkan memiliki 18 desimal.

| Nama Parameter | Tipe | Deskripsi         |
|:-------------- |:---- |:----------------- |
| simbol         | tali | Simbol stablecoin |

### hargaAsetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`fungsi hargaAsetUSDMint (alamat _asset)`**

Mengembalikan harga nilai tukar stablecoin yang ditentukan oleh `_asset` parameter yang digunakan saat mencetak OUSD yang diwakili oleh tipe `jenis uint256`. Angka yang dihasilkan memiliki 18 desimal.

| Nama Parameter | Tipe   | Deskripsi          |
|:-------------- |:------ |:------------------ |
| \_aset       | alamat | Alamat stablecoin‌ |

### hargaAsetUSDRedeem \ (\) ‌ <a id="issupportedasset-3-1"></a>

**`fungsi harga AsetUSDRedeem (address _asset)`**

Mengembalikan harga nilai tukar stabelcoin yang ditentukan oleh parameter `_aset` yang digunakan saat menukarkan OUSD yang diwakili oleh tipe ` uint256`. Angka yang dihasilkan memiliki 18 desimal.

| Nama Parameter | Tipe   | Deskripsi         |
|:-------------- |:------ |:----------------- |
| \_aset       | alamat | Alamat stablecoin |

