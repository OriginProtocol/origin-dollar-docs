# FAQ

**Dimana saya bisa membeli OUSD?**

Lihat [Memulai](https://docs.ousd.com/getting-started) untuk melihat berbagai opsi.

**Berapa biaya untuk mencetak dan menebus OUSD?**

Seperti halnya transaksi Ethereum, Anda akan memerlukan Eter untuk berinteraksi dengan kontrak pintar OUSD. Kami telah mengambil langkah-langkah untuk mengurangi penggunaan gas jika memungkinkan, tetapi biaya ini dapat bervariasi.

Setiap kali Anda mencetak atau menukarkan OUSD, akan ada nilai tukar yang diterapkan ke stablecoin Anda yang disetor atau ditarik. Anda dapat membaca lebih lanjut tentang ini di [Harga Oracles](https://docs.ousd.com/core-concepts/price-oracles).

Untuk mendorong kepemilikan jangka panjang OUSD dan untuk melindungi protokol dari penyerang, biaya keluar sebesar 0,5% dibebankan pada semua penukaran. Anda dapat membaca lebih lanjut tentang ini di [Harga Oracles](https://docs.ousd.com/how-it-works).

**Seberapa cepat saldo saya akan bertambah setelah saya memiliki OUSD?**

Jumlah OUSD di dompet Anda akan bertambah setiap kali ada acara rebase positif. Anda dapat membaca lebih lanjut tentang ini di [ Pasokan Elastis](https://docs.ousd.com/core-concepts/elastic-supply). Pasokan saat ini didasarkan ulang beberapa kali per hari dan biasanya berkorelasi dengan berapa banyak orang yang mencetak dan menukarkan OUSD.

**Mengapa OUSD tidak tumbuh saat diadakan di Uniswap, SushiSwap, dll?**

Secara default, peristiwa rebase tidak memengaruhi pasokan OUSD yang ada dalam kontrak pintar. Kontrak ini dapat memilih untuk menerima OUSD tambahan jika mereka mampu menangani token pasokan elastis. Anda dapat membaca lebih lanjut tentang ini di [Rebasing & Kontrak Pintar](https://docs.ousd.com/core-concepts/elastic-supply/rebasing-and-smart-contracts).

**Bagaimana mungkin APY bisa begitu tinggi?**

Anda dapat membaca tentang berbagai strategi kami di [Yield Generation](https://docs.ousd.com/core-concepts/yield-generation). Saat ini kami mendapatkan sebagian besar hasil dari memanen token hadiah \(yaitu COMP dan CRV\). Selain itu, imbal hasil meningkat karena lebih banyak OUSD ditahan dalam kontrak pintar yang tidak memilih untuk melakukan rebasing karena jaminan yang mendasarinya terus menghasilkan untuk pemegang OUSD rata-rata.

**Mengapa saldo saya meningkat lebih lambat dari APY yang diiklankan?**

OUSD balances increase when the supply is rebased. But the size of each rebase varies wildly depending on how much the vault has earned since the last rebase. And while most rebases collect a small amount earnings from lending strategies, other rebases involve liquidating rewards tokens or collecting fees. As a result, the yield will vary significantly during short time periods.

**What about the hack? Is OUSD safe?**

On November 7th 2020, OUSD was exploited for 7M USD due to a previously undetected reentrancy bug. You can read more [details about the hack](https://medium.com/originprotocol/urgent-ousd-has-hacked-and-there-has-been-a-loss-of-funds-7b8c4a7d534c) on our blog as well as the [detailed compensation plan](https://medium.com/originprotocol/origin-dollar-ousd-detailed-compensation-plan-faa73f87442e) for taking care of the affected users. Origin Dollar was relaunched in December after completing multiple audits and security upgrades. You can learn more about the steps taken to secure the protocol in our [relaunch announcement](https://medium.com/originprotocol/origin-dollar-ousd-is-back-b8ee0c601dad).

