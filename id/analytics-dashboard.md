# Dasbor Analisis

{% hint style="info" %}
Kunjungi [analytics.ousd.com](https://analytics.ousd.com) untuk melihat bagaimana dana dialokasikan, melihat data kinerja historis, dan melacak keuntungan pribadi Anda.
{% endhint %}

Dasbor [](https://analytics.ousd.com/apy) terutama ditujukan untuk konsumsi oleh tim teknik kami, tetapi kami melanjutkan dan menerapkannya karena etos kami adalah "publik secara default" dan semua yang kami lakukan adalah [sumber terbuka](http://github.com/OriginProtocol). Sayangnya, hal itu sering kali berarti melakukan kesalahan di sisi transparansi dan belum tentu di sisi meluangkan waktu untuk menjelaskan hal-hal dengan jelas.

Sebelum masuk ke perhitungan hasil, penting untuk memahami cara kerja OUSD baik dalam hal [generasi hasil](https://docs.ousd.com/core-concepts/yield-generation) dan [rebasing](https://docs.ousd.com/core-concepts/elastic-supply). You can read all about that in these [docs](https://docs.ousd.com), including [the part about smart contracts being excluded from yield](https://docs.ousd.com/core-concepts/elastic-supply/rebasing-and-smart-contracts).

Untuk meringkas bagaimana APY dihitung, ini adalah tingkat tahunan perubahan dalam akuntansi internal OUSD dari saldo pengguna antara dua titik waktu. To understand that, let's break down the columns in the historical APY table (in reverse order).

**Perbandingan**

There are two types of OUSD balances: rebasing (most accounts) and non-rebasing (smart contracts that have not opted in). Kontrak token OUSD mempertahankan akuntansi internal terpisah untuk setiap jenis saldo menggunakan apa yang disebut "kredit". Rasio yang ditunjukkan di sini adalah pasokan rebasing OUSD dibagi dengan kredit rebasing, yang memberi kita nilai tukar di antara keduanya.

**Kredit**

Some smart contracts holding OUSD have unique credit balances because their rebasing status has changed at some point in the past (by opting in or out). Di sini kami menunjukkan jumlah semua kredit rebasing dan kredit non-rebasing. Ketika dikalikan dengan rasio, itu memberikan perbedaan antara pasokan backing dan pasokan non-rebasing.

**Non-rebasing**

Ini adalah bagian dari pasokan yang disimpan dalam kontrak pintar lain yang belum memilih untuk melakukan rebasing. When added to (credits \* ratio), this equals backing supply. Perhatikan juga bahwa kolom **%** menunjukkan persentase OUSD yang non-rebasing.

**Dorongan**

APY secara efektif "didorong" untuk rebasing akun berkat fakta bahwa beberapa OUSD non-rebasing. Pikirkan tentang semua stablecoin yang digunakan sebagai jaminan untuk mencetak OUSD non-rebasing. Stablecoin itu masih menghasilkan melalui strategi pertanian hasil kami, tetapi keuntungan hanya diperoleh ke akun rebasing. Hasilnya adalah APY efektif lebih tinggi daripada tanpa mekanisme ini. Dorongan adalah ukuran dari perbedaan ini. Jika dorongan adalah 100%, maka pemegang OUSD biasa menikmati APY dua kali lipat dari yang seharusnya.

**Perhitungan APR/APY**

Bringing this full circle, we currently measure yield by measuring the change in the [rebasing credits per token](https://github.com/OriginProtocol/origin-dollar/blob/master/contracts/contracts/token/OUSD.sol#L45) between two points in time. Tetapi ada beberapa pertimbangan lain yang perlu diperhatikan. Pertama, kami harus membuat asumsi tentang berapa banyak blok Ethereum yang ditambang pada rata-rata hari. Kami menggunakan [ 6.500 yang sudah tetap](https://github.com/OriginProtocol/ousd-analytics/blob/master/eagleproject/core/views.py#L43), tetapi jumlah sebenarnya blok per hari adalah variabel. Kedua, kami membutuhkan cakrawala waktu yang masuk akal untuk mengukur. We focus on 30 days, which has proven to be a relatively consistent window of time during which a complete sample of yield-generating activities has occurred. Ketiga, kami mengubah APR menjadi APY dengan mengasumsikan [pelipatgandaan harian konstan](https://github.com/OriginProtocol/ousd-analytics/blob/master/eagleproject/core/views.py#L449-L451). Dengan kata lain, hasil terus diinvestasikan kembali ke dalam strategi yang sama. Akhirnya, ada satu kelemahan yang perlu dipertimbangkan untuk menggunakan rasio rebase untuk mengukur hasil. Since rebase events currently occur sporadically (and not very frequently in a world of high gas prices), the APY won't reflect earnings that have not yet been translated to account balances. Misalnya, mungkin ada lonjakan suku bunga di Compound atau lonjakan volume dalam strategi Curve 3pool, yang akan menyebabkan OUSD menghasilkan lebih banyak daripada rata-rata hari. Sampai [metode rebase](https://github.com/OriginProtocol/origin-dollar/blob/master/contracts/contracts/vault/VaultCore.sol#L365-L370) dipanggil, APY akan melaporkan pendapatan ini lebih rendah. In fact, anyone who sells OUSD during that time would be missing out on the "[next rebase](https://analytics.ousd.com)". The good news is that you should be able to observe the change in your balance over one week and it (annualized) should approximately equal our advertised APY.
