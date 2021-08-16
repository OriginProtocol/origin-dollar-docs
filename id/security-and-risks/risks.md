# Resiko

{% hint style="danger" %}
Gunakan dengan resiko Anda sendiri. Jangan menggunakan modal lebih dari yang Anda rela kehilangan.
{% endhint %}

Seperti halnya produk DeFi yang menghasilkan hasil, ada risiko terkait dengan memegang OUSD yang penting untuk dipahami. Risiko-risiko ini secara luas dapat diklasifikasikan menjadi 3 kategori:

* Risiko kontrak pintar OUSD
* Risiko platform pihak ketiga yang mendasari
* Risiko stablecoin yang mendasari

**Risiko kontrak pintar OUSD**

Kontrak cerdas kami telah [diaudit](audits.md) oleh beberapa perusahaan keamanan yang dihormati. Kontrak pintar kami belum diaudit, dan bahkan dengan audit formal, masih mungkin terjadi kesalahan logika yang akan menyebabkan hilangnya dana bagi para pemegang OUSD. Kontrak melibatkan matematika dan logika yang kompleks. Meskipun kami telah mengambil setiap tindakan pencegahan untuk memastikan keselamatan dan keamanan kontrak pintar kami, pengguna diingatkan untuk menggunakan dengan risiko mereka sendiri. Origin Protocol tidak akan bertanggung jawab atas hilangnya dana, terlepas dari siapa yang bersalah.

**Risiko platform pihak ketiga**

OUSD dibangun di atas platform DeFi lainnya seperti Aave, Compound, dan Curve yang menambahkan risiko kontrak pintar tambahan. Kami memilih untuk bekerja dengan platform yang memiliki aset ratusan juta dolar di bawah manajemen dan telah melakukan upaya yang wajar untuk memastikan kebenaran protokol mereka. Namun, tidak ada jaminan bahwa platform yang mendasarinya akan terus berfungsi sebagaimana mestinya, dan kegagalan dalam strategi yang mendasarinya kemungkinan besar akan menyebabkan hilangnya dana bagi para pemegang OUSD.

**Risiko Stablecoin**

Penting untuk dipahami bahwa OUSD hanya sekuat stablecoin yang mendukungnya. Setiap kehilangan nilai pada aset stablecoin yang mendasarinya akan menyebabkan kerugian yang serupa dengan nilai OUSD. Meskipun OUSD dirancang untuk mempertahankan hubungan satu lawan satu antara pasokan dan jumlah stablecoin pendukung, OUSD tidak menjamin stablecoin mana yang akan membentuk dukungan itu atau nilai koin tersebut.

Penting untuk dicatat bahwa setiap stablecoin yang didukung ini menimbulkan risiko pihak lawan yang tidak sepele. Tether, khususnya, memiliki masalah perbankan yang terdokumentasi dengan baik dan tantangan regulasi. Selain itu, baik USDT dan USDC memiliki pintu belakang yang memberikan kuasa kepada penerbitnya untuk membekukan uang di dompet pemegangnya. Meskipun DAI tidak memiliki pintu belakang langsung, asetnya juga dapat terkena dampak negatif karena USDC diterima sebagai jaminan untuk pembuatan DAI.

_**Singkatnya, OUSD adalah perangkat lunak beta. Gunakan dengan resiko Anda sendiri. Jangan menggunakan modal lebih dari yang Anda rela kehilangan.**_

**Mitigasi risiko**

Kami secara aktif bekerja dengan beberapa penyedia asuransi DeFi dan akan segera mengumumkan rencana pertanggungan awal kami untuk lebih mengamankan protokol. Selain rencana kami untuk menawarkan pertanggungan asuransi dan [audit](audits.md)kami baru-baru ini, kami telah mengambil langkah-langkah ekstensif untuk meningkatkan proses internal kami sehingga kami melakukan segala kemungkinan untuk menghindari eksploitasi.

Kami telah mempertahankan [Certora](https://www.certora.com/) untuk mulai memverifikasi secara formal berbagai properti keamanan kontrak kami. Mereka akan membantu kami membuat verifikasi otomatis yang akan berjalan setiap kali kami memperbarui kode kontrak kami. Kami sekarang juga memiliki pemeriksaan otomatis untuk kesalahan umum dengan tes [Slither](https://github.com/crytic/slither) dan [Echidna](https://github.com/crytic/echidna). Bersama-sama, ini mengingatkan tim kami tentang masalah keamanan umum selain rangkaian pengujian kami sendiri.

Peninjauan kode yang melibatkan kontrak pintar kami sekarang lebih ketat dari sebelumnya. Kami membutuhkan dua insinyur untuk meninjau setiap perubahan dengan daftar periksa terperinci dan kami memprioritaskan ini daripada pengembangan fitur baru.

Terakhir, kami telah meresmikan rotasi [](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) untuk meninjau [serangan pada proyek lain](https://github.com/OriginProtocol/security/tree/master/incidents) serta memastikan kami menyelami lebih dalam ke masing-masing tinjauan ini, termasuk meninjau kode sumber kontrak yang terpengaruh sendiri.







