# Timelock

{% hint style="danger" %}
Timelock akan ditambahkan segera setelah semuanya diverifikasi sebagai berfungsi. Sampai saat itu, kontrak akan diatur oleh 5 dari 8 multi-sig Origin. Hal ini memungkinkan respons yang lebih cepat jika ada masalah kritis yang ditemukan.
{% endhint %}

Kontrak timelock memberlakukan masa tunggu 48 jam sebelum perubahan apa pun pada kontrak OUSD dapat dilaksanakan. Kunci waktu dapat dipanggil oleh multi-sig kami dan merupakan pemilik kontrak [ERC-20](erc-20.md), [Vault](vault.md) dan [Strategies](strategies.md). Tindakan admin yang menunda waktu memberi pengguna kesempatan untuk keluar dari OUSD jika adminnya menjadi jahat, disusupi, atau membuat perubahan yang tidak disukai pengguna.

{% hint style="info" %}
Timelock adalah ukuran keamanan yang memberi pemegang OUSD 48 jam untuk menarik dana mereka apabila mereka keberatan dengan usulan peningkatan protokol.
{% endhint %}

OUSD menggunakan versi [Compound Timelock](https://compound.finance/docs/governance) yang sedikit dimodifikasi yang telah [diaudit oleh OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). 3 perbedaan penting adalah:

1. OUSD awalnya akan menggunakan periode tunggu yang lebih pendek \ (48 jam \) daripada Compound \ (72 jam \) untuk memungkinkan respons yang lebih cepat jika ditemukan masalah.
2. Setelah 48 jam berlalu, siapa pun bebas untuk melakukan panggilan, tidak hanya pemilik kontrak.
3. Deposit \ (tapi bukan penarikan atau transfer \) dapat langsung dibekukan tanpa memerlukan 48 waktu tunggu. Ini apabila sebuah kerentanan besar ditemukan.





