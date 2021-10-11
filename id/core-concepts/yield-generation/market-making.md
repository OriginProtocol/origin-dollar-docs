# Pembuatan Pasar

**Miliki Saham Anda di Bursa Terdesentralisasi**

Automated market makers (AMMs) have quickly risen as the preferred form of decentralized exchange on the Ethereum network. Ini sebagian karena kesulitan mendukung buku pesanan DEX di Ethereum 1.0 yang dapat menyaingi pengalaman instan dan selip rendah di bursa terpusat. Lebih lanjut, AMM seperti Uniswap relatif ramah pengguna dan hemat gas untuk digunakan.

AMMs can only enable new markets when liquidity providers supply liquidity (e.g. multiple tokens for given trading pairs or pools). Sebagai imbalan untuk menyediakan likuiditas, penyedia likuiditas diberi imbalan dengan biaya perdagangan ketika pengguna lain menukar token. For example, when traders swap two tokens on Uniswap v3, they are currently charged anywhere between 0.05% and 1% on top of the gas fees. These fees are distributed pro-rata to liquidity providers of the pair based on the percentage of total liquidity that they have provided.

{% hint style="info" %}
[Kerugian tidak permanen](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) merupakan faktor risiko yang penting untuk dipahami, namun kekhawatiran ini sebagian besar dapat diatasi oleh OUSD yang hanya menyediakan likuiditas untuk stablecoin dengan nilai yang kurang lebih sama.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens (e.g. Curve rewards CRV tokens to liquidity providers). Hasil panen kemudian diteruskan ke pemegang OUSD.

Kami saat ini terintegrasi dengan pembuat pasar otomatis berikut:

{% content-ref url="../supported-strategies/curve.md" %}
[curve.md](../supported-strategies/curve.md)
{% endcontent-ref %}



