# Timelock

{% hint style="danger" %}
Timelock telah ditambahkan tetapi saat ini disetel ke 1 menit. Hal ini memungkinkan respons yang lebih cepat jika ada masalah kritis yang ditemukan. Timelock diatur oleh 5 dari 8 multi-sig Origin.
{% endhint %}

Kontrak timelock memberlakukan masa tunggu 48 jam sebelum perubahan apa pun pada kontrak OUSD dapat dilaksanakan. Kunci waktu dapat dipanggil oleh multi-sig kami dan merupakan pemilik kontrak [ERC-20](../architecture.md), [Vault](vault.md) dan [Strategies](strategies.md). Tindakan admin yang menunda waktu memberi pengguna kesempatan untuk keluar dari OUSD jika adminnya menjadi jahat, disusupi, atau membuat perubahan yang tidak disukai pengguna.

{% hint style="info" %}
Timelock adalah ukuran keamanan yang memberi pemegang OUSD 48 jam untuk menarik dana mereka apabila mereka keberatan dengan usulan peningkatan protokol.
{% endhint %}

OUSD menggunakan versi [Compound Timelock](https://compound.finance/docs/governance) yang sedikit dimodifikasi yang telah [diaudit oleh OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). Dua perbedaan yang mencolok adalah:

1. OUSD will initially use a shorter wait period (48 hours) than Compound (72 hours) to allow for a faster response if any issues are discovered.
2. Beberapa tindakan, seperti realokasi dana antara strategi yang ada dan pembekuan deposito dapat segera dilakukan tanpa memerlukan 48 masa tunggu. Ini apabila sebuah kerentanan besar ditemukan.



