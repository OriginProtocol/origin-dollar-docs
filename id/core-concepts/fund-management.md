# Pengelolaan Dana

Kontrak pintar OUSD menggabungkan semua deposit stablecoin pengguna ke dalam satu kumpulan aset yang dapat digunakan. Funds are then allocated across one or more** **earning strategies at any given moment in time. Vault lebih menyukai strategi hasil tinggi tetapi juga berusaha mempertahankan diversifikasi di berbagai strategi. Diversifikasi menghilangkan satu titik kegagalan dan mengurangi risiko.

Berbeda dengan peluang Yearn Vaults, TokenSets, atau Zapper, pengguna tidak memilih strategi individu. Semua stablecoin yang disimpan dan akibatnya semua token OUSD dapat dipertukarkan. Setelah struktur tata kelola penuh kami diterapkan, keputusan ini akan dibuat dengan masukan dari pemegang token tata kelola OUSD. OGN holders are encouraged to participate in creating and voting on proposals that impact the protocol in the [OGN governance portal](https://vote.originprotocol.com).

**Strategi Penghasilan**

Strategi penghasilan menempatkan modal yang dikerahkan untuk bekerja di berbagai platform DeFi. Vault akan menentukan strategi mana yang aktif dan berapa persentase dari modal yang diterapkan yang akan mereka terima. Strategi ini akan ditingkatkan dan diganti seiring waktu.

**Penyiasat**

Versi awal kontrak pintar OUSD Vault memberikan bobot sederhana antara 0% dan 100% untuk setiap strategi yang valid untuk melakukan alokasi aset sederhana. Bobot ini akan sering diubah melalui pembaruan oleh Origin dalam jangka pendek dan oleh tata kelola yang terdesentralisasi dalam jangka panjang.

**Diversifikasi**

Diversifikasi di beberapa platform DeFi [mendasarinya](supported-strategies/) akan mengurangi kontrak pintar dan risiko sistemik lainnya. Kontrak pintar akan menghitung APY saat ini dan yang diharapkan dalam upaya memberikan pengembalian yang kompetitif kepada pemegang OUSD. Seiring waktu, kontrak Vault akan ditingkatkan untuk secara cerdas dan otonom beralih di antara strategi tanpa intervensi manual apa pun. Misalnya, Vault akan secara otomatis mengalihkan modal di antara berbagai strategi pinjaman untuk mengoptimalkan hasil.

Namun, masih diharapkan bahwa parameter risiko atau keputusan tertentu tentang apakah strategi tertentu akan dimasukkan dalam mesin pengambilan keputusan otomatis akan dibuat melalui suara tata kelola. 
