# FAQ

**Dimana saya bisa membeli OUSD?**

Lihat [Memulai](https://docs.ousd.com/getting-started) untuk melihat berbagai opsi.

**Berapa biaya untuk mencetak dan menebus OUSD?**

Seperti halnya transaksi Ethereum, Anda akan memerlukan Eter untuk berinteraksi dengan kontrak pintar OUSD. Kami telah mengambil langkah-langkah untuk mengurangi penggunaan gas jika memungkinkan, tetapi biaya ini dapat bervariasi.

Setiap kali Anda mencetak atau menukarkan OUSD, akan ada nilai tukar yang diterapkan ke stablecoin Anda yang disetor atau ditarik. Anda dapat membaca lebih lanjut tentang ini di [Harga Oracles](https://docs.ousd.com/core-concepts/price-oracles).

To encourage long-term holding of OUSD and to protect the protocol from attackers, an exit fee of 0.25% is charged on all redeems. You can read more about this in [How It Works](https://docs.ousd.com/how-it-works).

**Seberapa cepat saldo saya akan bertambah setelah saya memiliki OUSD?**

Jumlah OUSD di dompet Anda akan bertambah setiap kali ada acara rebase positif. Anda dapat membaca lebih lanjut tentang ini di [ Pasokan Elastis](https://docs.ousd.com/core-concepts/elastic-supply). Pasokan saat ini didasarkan ulang beberapa kali per hari dan biasanya berkorelasi dengan berapa banyak orang yang mencetak dan menukarkan OUSD.

**Mengapa OUSD tidak tumbuh saat diadakan di Uniswap, SushiSwap, dll?**

Secara default, peristiwa rebase tidak memengaruhi pasokan OUSD yang ada dalam kontrak pintar. Kontrak ini dapat memilih untuk menerima OUSD tambahan jika mereka mampu menangani token pasokan elastis. Anda dapat membaca lebih lanjut tentang ini di [Rebasing & Kontrak Pintar](https://docs.ousd.com/core-concepts/elastic-supply/rebasing-and-smart-contracts).

**Bagaimana mungkin APY bisa begitu tinggi?**

Anda dapat membaca tentang berbagai strategi kami di [Yield Generation](https://docs.ousd.com/core-concepts/yield-generation). We currently get most of the yield from harvesting rewards tokens (namely COMP and CRV). Selain itu, imbal hasil meningkat karena lebih banyak OUSD ditahan dalam kontrak pintar yang tidak memilih untuk melakukan rebasing karena jaminan yang mendasarinya terus menghasilkan untuk pemegang OUSD rata-rata.

**Mengapa saldo saya meningkat lebih lambat dari APY yang diiklankan?**

Saldo OUSD meningkat saat pasokan mengalami rebase. Tetapi ukuran setiap rebase sangat bervariasi tergantung pada berapa banyak yang diperoleh vault sejak rebase terakhir. Dan sementara sebagian besar rebase mengumpulkan sedikit pendapatan dari strategi pinjaman, rebase lainnya melibatkan likuidasi token hadiah atau mengumpulkan biaya. Akibatnya, hasil akan bervariasi secara signifikan selama periode waktu yang singkat.

**Bagaimana dengan peretasan? Apakah OUSD aman?**

Pada 7 November 2020, OUSD dieksploitasi sebanyak 7 juta USD karena bug reentrancy yang sebelumnya tidak terdeteksi. Anda dapat membaca lebih lanjut [detail tentang peretasan](https://medium.com/originprotocol/urgent-ousd-has-hacked-and-there-has-been-a-loss-of-funds-7b8c4a7d534c) di blog kami serta [detail rencana kompensasi](https://medium.com/originprotocol/origin-dollar-ousd-detailed-compensation-plan-faa73f87442e) untuk mengganti rugi pengguna yang terkena dampak. Origin Dollar diluncurkan kembali pada bulan Desember setelah menyelesaikan beberapa audit dan peningkatan keamanan. Anda dapat mempelajari lebih lanjut tentang langkah-langkah yang diambil untuk mengamankan protokol di [pengumuman peluncuran kembali](https://medium.com/originprotocol/origin-dollar-ousd-is-back-b8ee0c601dad).
