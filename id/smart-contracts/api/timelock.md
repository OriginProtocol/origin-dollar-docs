# Timelock

{% hint style="danger" %}
The timelock has been added but is currently set to 1 minute. This allows for a faster response if any critical issues are discovered. The timelock is governed by Origin's 5 of 8 multi-sig.
{% endhint %}

Kontrak timelock memberlakukan masa tunggu 48 jam sebelum perubahan apa pun pada kontrak OUSD dapat dilaksanakan. Kunci waktu dapat dipanggil oleh multi-sig kami dan merupakan pemilik kontrak [ERC-20](../architecture.md), [Vault](vault.md) dan [Strategies](strategies.md). Tindakan admin yang menunda waktu memberi pengguna kesempatan untuk keluar dari OUSD jika adminnya menjadi jahat, disusupi, atau membuat perubahan yang tidak disukai pengguna.

{% hint style="info" %}
Timelock adalah ukuran keamanan yang memberi pemegang OUSD 48 jam untuk menarik dana mereka apabila mereka keberatan dengan usulan peningkatan protokol.
{% endhint %}

OUSD menggunakan versi [Compound Timelock](https://compound.finance/docs/governance) yang sedikit dimodifikasi yang telah [diaudit oleh OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). The two notable differences are:

1. OUSD awalnya akan menggunakan periode tunggu yang lebih pendek \ (48 jam \) daripada Compound \ (72 jam \) untuk memungkinkan respons yang lebih cepat jika ditemukan masalah.
2. Some actions, such a reallocating funds between existing strategies and freezing deposits can be called immediately without requiring the 48 waiting period. This is in case a major vulnerability is discovered.





