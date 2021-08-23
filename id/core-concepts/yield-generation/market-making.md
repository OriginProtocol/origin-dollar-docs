# Pembuatan Pasar

**Miliki Saham Anda di Bursa Terdesentralisasi**

Automated market maker \ (AMMs \) dengan cepat meningkat sebagai bentuk pertukaran desentralisasi yang disukai di jaringan Ethereum. Ini sebagian karena kesulitan mendukung buku pesanan DEX di Ethereum 1.0 yang dapat menyaingi pengalaman instan dan selip rendah di bursa terpusat. Lebih lanjut, AMM seperti Uniswap relatif ramah pengguna dan hemat gas untuk digunakan.

AMM hanya dapat mengaktifkan pasar baru ketika penyedia likuiditas menyediakan likuiditas \ (misalnya beberapa token untuk pasangan atau kumpulan perdagangan tertentu \). Sebagai imbalan untuk menyediakan likuiditas, penyedia likuiditas diberi imbalan dengan biaya perdagangan ketika pengguna lain menukar token. For example, when traders swap two tokens on Uniswap v3, they are currently charged anywhere between 0.05% and 1% on top of the gas fees. These fees are distributed pro-rata to liquidity providers of the pair based on the percentage of total liquidity that they have provided.

{% hint style="info" %}
[Kerugian tidak permanen](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) merupakan faktor risiko yang penting untuk dipahami, namun kekhawatiran ini sebagian besar dapat diatasi oleh OUSD yang hanya menyediakan likuiditas untuk stablecoin dengan nilai yang kurang lebih sama.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens \(e.g. Curve rewards CRV tokens to liquidity providers\). Hasil panen kemudian diteruskan ke pemegang OUSD.

Kami saat ini terintegrasi dengan pembuat pasar otomatis berikut:

{% page-ref page = "../ didukung-strategi / curve.md"%}





