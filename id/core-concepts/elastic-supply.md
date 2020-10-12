# Pasokan Elastis

**Pasokan Elastis. Harga Stabil.**

OUSD bekerja secara berbeda dari kebanyakan token. Alih-alih kenaikan harga karena nilai aset yang dikelola meningkat \ (seperti pada Compound cTokens atau Yearn yTokens \), nilai satu OUSD tetap konstan sekitar $ 1. Sebaliknya, kontrak secara konstan menyesuaikan pasokan moneter dan secara otomatis memperbarui saldo di dompet setiap pemegang token untuk mencerminkan hasil yang telah diperoleh oleh protokol.

{% hint style="info" %}
Anggap saja sebagai bunga yang bertambah di rekening bank Anda. Unit akun dan nilai dolar AS tidak berubah. Anda hanya mendapatkan lebih banyak dolar AS dari waktu ke waktu saat Anda memperoleh bunga.
{% endhint %}

![](../.gitbook/assets/ousd_docs_graphics_4.png)

Mekanisme ini terinspirasi oleh pendekatan baru yang diambil oleh [Ampleforth](https://www.ampleforth.org/), tetapi ada beberapa perbedaan utama yang perlu diperhatikan:

1. OUSD 100% didukung oleh stablecoin lain dan tidak akan memiliki tantangan yang sama untuk mempertahankan patokan terhadap dolar. Mengingat kemudahan mencetak dan menebus OUSD, kami dapat mengandalkan arbitrase untuk memastikan pasak dipertahankan.
2. OUSD rebasing should only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Any decrease in your balance would be an indication of trouble in the system.
3. Tidak seperti Ampleforth, yang melakukan rebases sekali sehari, pasokan moneter OUSD terus diperbarui secara waktu nyata saat hasil dihasilkan.

