# Ikhtisar

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD terdiri dari serangkaian kontrak pintar. Masing-masing kontrak ini dibungkus dalam kontrak proxy yang dapat ditingkatkan melalui protokol tata kelola.

Secara internal, kepemilikan dalam kumpulan dilacak menggunakan sistem kredit yang mewakili persentase kepemilikan kumpulan untuk setiap pemegang. Kontrak ERC-20 menangani konversi ke persyaratan USD saat melihat saldo atau memulai transfer antar dompet.

The Vault is responsible for minting and burning OUSD. It also enforces the percentage of assets that are deployed to each of the supported [Strategies](../core-concepts/supported-strategies/). To optimize gas costs, the vault maintains a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.



