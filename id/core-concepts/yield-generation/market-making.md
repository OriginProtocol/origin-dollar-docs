# Pembuatan Pasar

**Miliki Saham Anda di Bursa Terdesentralisasi**

Automated market maker \ (AMMs \) dengan cepat meningkat sebagai bentuk pertukaran desentralisasi yang disukai di jaringan Ethereum. Ini sebagian karena kesulitan mendukung buku pesanan DEX di Ethereum 1.0 yang dapat menyaingi pengalaman instan dan selip rendah di bursa terpusat. Lebih lanjut, AMM seperti Uniswap relatif ramah pengguna dan hemat gas untuk digunakan.

AMM hanya dapat mengaktifkan pasar baru ketika penyedia likuiditas menyediakan likuiditas \ (misalnya beberapa token untuk pasangan atau kumpulan perdagangan tertentu \). Sebagai imbalan untuk menyediakan likuiditas, penyedia likuiditas diberi imbalan dengan biaya perdagangan ketika pengguna lain menukar token. Misalnya, ketika pedagang menukar USDT dengan USDC di Uniswap, mereka saat ini dikenai biaya 0,3% di atas biaya gas. Biaya ini didistribusikan secara pro-rata kepada penyedia likuiditas pada pasangan USDT-USDC berdasarkan persentase total likuiditas yang mereka sediakan.

{% hint style="info" %}
[Kerugian tidak permanen](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) merupakan faktor risiko yang penting untuk dipahami, namun kekhawatiran ini sebagian besar dapat diatasi oleh OUSD yang hanya menyediakan likuiditas untuk stablecoin dengan nilai yang kurang lebih sama.
{% endhint %}

Protokol OUSD mengarahkan USDT, USDC, dan DAI ke pool likuiditas yang berkinerja tinggi sebagaimana ditentukan oleh volume perdagangan dan hadiah token \ (misalnya, Balancer memberi hadiah token BAL ke penyedia likuiditas \). Hasil panen kemudian diteruskan ke pemegang OUSD.

We are currently integrated with the following automated market maker:

{% page-ref page="../supported-strategies/curve.md" %}

We are intending to integrate with the following automated market makers:

{% page-ref page="../supported-strategies/uniswap.md" %}

{% page-ref page="../supported-strategies/balancer.md" %}





