# Berkontribusi

**100% Sumber terbuka**

OUSD sepenuhnya merupakan proyek sumber terbuka dan kami menerima segala macam kontribusi. Ada banyak cara untuk membantu, dari melaporkan masalah, menyumbangkan kode, dan membantu kami meningkatkan komunitas kami.

Kami bekerja di depan umum dan perusahaan kami Discord terbuka untuk semua. Jika Anda memiliki pertanyaan atau butuh bantuan untuk memulai, [Discord OUSD](https://discord.gg/jyxpUSe) adalah tempat terbaik untuk mendapatkan bantuan dari tim dan komunitas kami.

**Analisis Pengembang**

Dasbor pengembang internal kami tersedia di [analytics.ousd.com](https://analytics.ousd.com). Dasbor menunjukkan pasokan yang beredar saat ini, aset yang dikelola di brankas, dan alokasi saat ini antara masing-masing stablecoin dan strategi.

#### Proses pengembangan

Strategi percabangan kami mirip dengan [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), tetapi kami melakukan semua pengembangan kami di cabang ` master` dan memiliki cabang ` stabil` untuk kode yang telah dirilis.

Alur pengembangan Anda akan terlihat seperti:

1. Temukan masalah yang menarik dan komunikasikan! Harap beri tahu saluran `#engineering` [Discord](https://discord.gg/jyxpUSe) apa yang ingin Anda kerjakan.
2. Ping [anggota tim inti](https://github.com/orgs/OriginProtocol/teams/core/members) anggota di Discord dan minta untuk ditambahkan ke [tim kontributor](https://github.com/orgs/OriginProtocol/teams/contributors). Jika tidak, Anda harus membagi repositori yang relevan dan mendorong cabang fitur ke garpu Anda sendiri.
3. Tambahkan komentar ke masalah atau tetapkan sendiri sehingga kami tidak memiliki beberapa kontributor yang secara tidak sengaja mengerjakan tugas yang sama.
4. Mulailah dengan cabang `master` dan periksa cabang fitur baru kecuali Anda berkontribusi ke fitur yang ada.
5. Tulis beberapa kode yang luar biasa.
6. Tarik komit terbaru dari `master` dan konfirmasikan bahwa kode Anda berfungsi dengan pekerjaan lain yang telah digabungkan sejak Anda mulai.
7. Dorong cabang Anda ke repositori hulu \ (yaitu https: //github.com/OriginProtocol/ \ [repo \] \) sehingga kontributor lain dapat dengan mudah mengerjakannya jika perlu.
8. Silakan meminta peninjauan di PR dengan mengklik ikon roda gigi di sebelah "Pengulas" di kolom kanan.

Agar kode kontrak pintar kritis dapat digabungkan, kode tersebut harus melewati daftar periksa berikut:

*  Kode ditinjau oleh 2 pengulas
*  Tes unit lulus
*  Tes meluncur lulus tanpa peringatan
*  Tes Echidna lulus

Cabang `master` dikunci sehingga hanya anggota dari [tim inti](https://github.com/orgs/OriginProtocol/teams/core) yang dapat menggabungkan permintaan tarik Anda. Permintaan penarikan yang ditinjau oleh kontributor tepercaya lainnya akan dilacak dengan cepat dan digabungkan lebih cepat! Periksa di saluran `#engineering` Discord untuk pengulas yang sesuai.

#### Gaya Pengkodean

Kami menggunakan berbagai bahasa pemrograman di repositori kami. Saat berkontribusi, harap ikuti konvensi pengkodean yang ada dan lihat file CONTRIBUTING.md di repositori, jika ada.

Untuk JavaScript, kami menggunakan [NPM gaya](https://docs.npmjs.com/misc/coding-style), yang secara otomatis diberlakukan melalui [lebih cantik](https://prettier.io/).

Untuk Soliditas, kami menggunakan indentasi dua spasi.

#### Desain Protokol

Saat mempertimbangkan protokol atau proposal desain implementasi, kami mencari:

* Deskripsi masalah yang diselesaikan oleh proposal desain ini
* Diskusi tentang trade-off yang terlibat
* Review solusi lain yang ada
* Tautan ke literatur yang relevan \ (RFC, makalah, dll \)
* Diskusi tentang solusi yang diusulkan

Harap dicatat bahwa desain protokol adalah pekerjaan yang sulit dan membutuhkan ketelitian. Anda mungkin perlu meninjau literatur yang ada dan memikirkan kasus penggunaan umum.

#### Pedoman Komunitas

Kami ingin membuat komunitas Origin tetap mengagumkan, berkembang, dan kolaboratif. Kami membutuhkan bantuan Anda untuk tetap seperti itu. Untuk membantu hal ini, kami telah membuat beberapa pedoman umum untuk komunitas secara keseluruhan:

* Bersikap baik: Bersikaplah sopan, hormat, dan sopan kepada sesama anggota komunitas: tidak ada pelecehan regional, ras, jenis kelamin, atau lainnya yang akan ditoleransi. Kami menyukai orang baik jauh lebih baik daripada orang jahat!
* Dorong keberagaman dan partisipasi: Buat semua orang di komunitas kami merasa diterima, terlepas dari latar belakang dan tingkat kontribusi mereka, dan lakukan segala kemungkinan untuk mendorong partisipasi dalam komunitas kami.
* Tetap legal: Pada dasarnya, jangan membuat siapa pun mendapat masalah. Bagikan hanya konten yang Anda miliki, jangan bagikan informasi pribadi atau sensitif, dan jangan melanggar hukum.
* Tetap sesuai topik: Pastikan Anda memposting ke saluran yang benar dan hindari diskusi di luar topik. Ingatlah saat Anda memperbarui masalah atau membalas email yang berpotensi Anda kirim ke banyak orang. Harap pertimbangkan ini sebelum Anda memperbarui. Ingat juga bahwa tidak ada yang suka spam.

#### Melaporkan Masalah

Jika Anda menemukan bug, kesalahan, atau ketidakkonsistenan dalam kode atau dokumen Origin, beri tahu kami dengan mengajukan masalah GitHub. Tidak ada masalah yang terlalu kecil. Bantu kami memperbaiki typos kami!

#### Masalah Keamanan

OUSD masih dalam pengembangan awal, yang berarti mungkin ada masalah dengan protokol atau dalam implementasi kami. Kami menangani kerentanan keamanan dengan sangat serius. Jika Anda menemukan masalah keamanan, harap segera hubungi kami!

Jika Anda menemukan kerentanan keamanan, silakan kirim laporan Anda secara pribadi ke [security@originprotocol.com](mailto:security@originprotocol.com) atau kirim pesan terenkripsi ke [@joshfraser di Keybase](https://keybase.io/joshfraser). Harap JANGAN mengajukan masalah publik. Pastikan untuk meninjau pedoman kami untuk pengungkapan yang bertanggung jawab dan kelayakan untuk bug bounties.

{% page-ref page="../security-and-risks/bug-bounties.md" %}

#### **Peningkatan Komunitas**

Origin adalah tentang komunitas seperti tentang teknologi kita.

Kami membutuhkan bantuan terus-menerus dalam meningkatkan dokumentasi kami, membuat alat baru untuk berinteraksi dengan platform kami, menyebarkan berita ke pengguna baru, membantu pengguna baru mendapatkan penyiapan, dan banyak lagi.

Silakan hubungi jika Anda ingin membantu. Saluran `umum` kami di [Discord](https://www.originprotocol.com/discord) adalah tempat yang tepat untuk berbagi ide dan menjadi sukarelawan untuk membantu.

#### Posisi Penuh Waktu

Origin terkadang mempekerjakan pengembang untuk posisi paruh waktu atau penuh waktu.

Kami memiliki preferensi kuat untuk mempekerjakan orang yang sudah mulai berkontribusi pada proyek. Jika Anda menginginkan posisi penuh waktu di tim kami, kesempatan terbaik Anda adalah terlibat dengan tim kami dan mulai kode berkontribusi. Sangat kecil kemungkinannya kami akan menawarkan Anda posisi penuh waktu di tim teknik kami kecuali Anda memiliki setidaknya beberapa permintaan tarik yang digabungkan.

Jika Anda tertarik, lihat [daftar pekerjaan Protokol Origin](https://angel.co/originprotocol/jobs). Jika Anda ingin membantu dengan cara lain, ajukan ide Anda di [saluran Discord kami](https://www.originprotocol.com/discord).



