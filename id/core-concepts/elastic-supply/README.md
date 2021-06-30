# Pasokan Elastis

**Pasokan Elastis. Harga Stabil.**

OUSD bekerja secara berbeda dari kebanyakan token. Alih-alih kenaikan harga karena nilai aset yang dikelola meningkat \ (seperti pada Compound cTokens atau Yearn yTokens \), nilai satu OUSD tetap konstan sekitar $ 1. Sebaliknya, kontrak secara konstan menyesuaikan pasokan moneter dan secara otomatis memperbarui saldo di dompet setiap pemegang token untuk mencerminkan hasil yang telah diperoleh oleh protokol.

{% hint style="info" %}
Anggap saja sebagai bunga yang bertambah di rekening bank Anda. Unit akun dan nilai dolar AS tidak berubah. Anda hanya mendapatkan lebih banyak dolar AS dari waktu ke waktu saat Anda memperoleh bunga.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

Mekanisme ini terinspirasi oleh pendekatan baru yang diambil oleh [Ampleforth](https://www.ampleforth.org/), tetapi ada beberapa perbedaan utama yang perlu diperhatikan:

1. OUSD 100% didukung oleh stablecoin lain dan tidak memiliki tantangan yang sama untuk mempertahankan pasak terhadap dolar. Mengingat kemudahan mencetak dan menebus OUSD, kami dapat mengandalkan arbitrase untuk memastikan pasak dipertahankan.
2. Rebasing OUSD hanya akan meningkatkan pasokan karena jumlah OUSD yang dicetak terkait dengan keuntungan yang diperoleh dari strategi yang mendasarinya. Pokok Anda dilindungi selama tidak ada yang salah dengan protokol pinjaman / AMM dan stablecoin yang mendasarinya. Saldo OUSD Anda tidak akan pernah berkurang, tetapi nilainya bisa turun jika ada kegagalan pada sistem yang mendasarinya.
3. Tidak seperti Ampleforth, yang melakukan rebase sekali sehari, pasokan moneter OUSD terus diperbarui secara real-time saat hasil dihasilkan. Rebase dipicu secara teratur saat pengguna berinteraksi dengan kontrak OUSD.

**Memicu rebase secara manual**

Siapa pun dapat memicu rebase kapan saja dengan [memanggil fungsi rebase di vault](https://etherscan.io/address/originvault.eth#writeProxyContract). Anda dapat melakukan ini di Etherscan dengan menghubungkan dompet web3.
