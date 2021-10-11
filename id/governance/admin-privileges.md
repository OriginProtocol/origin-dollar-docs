# Hak Istimewa Admin

Kontrak pintar OUSD dirancang agar dapat diupgrade oleh pemilik. Tim Origin menggunakan dua kontrak dompet multisig Gnosis yang berbeda untuk membuat perubahan pada protokol. Dompet multisig ini telah [diaudit oleh OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), tim Origin, dan lainnya.

{% hint style="info" %}
Tindakan admin yang menunda waktu memberi pengguna kesempatan untuk keluar dari OUSD jika adminnya menjadi jahat, disusupi, atau membuat perubahan yang tidak disukai pengguna.
{% endhint %}

Admin utama adalah kontrak multisig 5 dari 8 yang diperlukan untuk membuat perubahan kode apa pun pada protokol. OUSD hanya dapat ditingkatkan dari dompet multi-sig 5 dari 8 ini. Kunci multi-sig ini dipegang oleh individu yang memiliki hubungan dekat dengan perusahaan, dan bahkan pendiri Origin yang bertindak bersama tidak memiliki kontrol yang cukup untuk menjalankan fungsi pemilik sendiri. Selain itu, kontrak OUSD dimiliki oleh [timelock](../smart-contracts/api/timelock.md) yang memungkinkan tim Asal untuk terus membuat perubahan pada protokol, tetapi hanya setelah penundaan waktu.

Beberapa fungsi, seperti menyeimbangkan dana di antara strategi atau menjeda setoran, dapat dipicu tanpa timelock dan dengan penanda tangan yang jauh lebih sedikit. Hal ini memungkinkan tim Origin untuk bereaksi lebih cepat terhadap kondisi pasar atau ancaman keamanan. These signers, known as Strategists,  have the ability to execute a limited number of functions_ _with only 2 of 9 signers.

Memiliki hak istimewa admin diperlukan di hari-hari awal untuk memastikan bahwa protokol aman dan dioptimalkan untuk mendapatkan hasil sekaligus meminimalkan risiko. Kami berharap untuk merilis beberapa iterasi kontrak pintar kami dalam beberapa bulan pertama keberadaan protokol.

Setelah beberapa siklus peningkatan selesai, kami bermaksud untuk mengalihkan kepemilikan dari kendali perusahaan kami ke kontrak tata kelola terdesentralisasi, sehingga memungkinkan komunitas untuk memilih dan berpartisipasi dalam pembaruan protokol di masa mendatang.
