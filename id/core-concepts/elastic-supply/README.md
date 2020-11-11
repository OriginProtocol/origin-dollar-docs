# Pasokan Elastis

**Pasokan Elastis. Harga Stabil.**

OUSD bekerja secara berbeda dari kebanyakan token. Alih-alih kenaikan harga karena nilai aset yang dikelola meningkat \ (seperti pada Compound cTokens atau Yearn yTokens \), nilai satu OUSD tetap konstan sekitar $ 1. Sebaliknya, kontrak secara konstan menyesuaikan pasokan moneter dan secara otomatis memperbarui saldo di dompet setiap pemegang token untuk mencerminkan hasil yang telah diperoleh oleh protokol.

{% hint style="info" %}
Anggap saja sebagai bunga yang bertambah di rekening bank Anda. Unit akun dan nilai dolar AS tidak berubah. Anda hanya mendapatkan lebih banyak dolar AS dari waktu ke waktu saat Anda memperoleh bunga.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

Mekanisme ini terinspirasi oleh pendekatan baru yang diambil oleh [Ampleforth](https://www.ampleforth.org/), tetapi ada beberapa perbedaan utama yang perlu diperhatikan:

1. OUSD is 100% backed by other stablecoins and does not have the same challenge maintaining the peg to the dollar. Mengingat kemudahan mencetak dan menebus OUSD, kami dapat mengandalkan arbitrase untuk memastikan pasak dipertahankan.
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Pokok Anda dilindungi selama tidak ada yang salah dengan protokol pinjaman / AMM dan stablecoin yang mendasarinya. Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.

