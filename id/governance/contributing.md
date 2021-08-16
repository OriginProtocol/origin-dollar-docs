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

Kami menggunakan berbagai bahasa pemrograman di repositori kami. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io/).

For Solidity, we use two-space indents.

#### Desain Protokol

When considering protocol or implementation design proposals, we are looking for:

* A description of the problem this design proposal solves
* Discussion of the trade-offs involved
* Review of other existing solutions
* Links to relevant literature \(RFCs, papers, etc\)
* Discussion of the proposed solution

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### Pedoman Komunitas

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* Be nice: Be courteous, respectful and polite to fellow community members: no regional, racial, gender, or other abuse will be tolerated. We like nice people way better than mean ones!
* Encourage diversity and participation: Make everyone in our community feel welcome, regardless of their background and the extent of their contributions, and do everything possible to encourage participation in our community.
* Keep it legal: Basically, don’t get anybody in trouble. Share only content that you own, do not share private or sensitive information, and don’t break laws.
* Stay on topic: Make sure that you are posting to the correct channel and avoid off-topic discussions. Remember when you update an issue or respond to an email you are potentially sending to a large number of people. Please consider this before you update. Also remember that nobody likes spam.

#### Melaporkan Masalah

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### Masalah Keamanan

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% page-ref page="../security-and-risks/bug-bounties.md" %}

#### **Peningkatan Komunitas**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `general` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Posisi Penuh Waktu

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).



