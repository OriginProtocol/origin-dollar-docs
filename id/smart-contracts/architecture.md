# Arsitektur

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD terdiri dari serangkaian kontrak pintar. Setiap kontrak ini dibungkus dalam kontrak proxy yang dapat ditingkatkan melalui protokol tata kelola.

Secara internal, kepemilikan dalam kumpulan dilacak menggunakan sistem kredit yang mewakili persentase kepemilikan kumpulan untuk setiap pemegang. The [ERC-20](api/erc-20-1.md) contract handles the conversion to USD terms when viewing a balance or initiating a transfer between wallets.

[Vault](api/vault.md) bertanggung jawab untuk mencetak dan membakar OUSD. Ini juga memberlakukan persentase aset yang disebarkan ke masing-masing [Strategi](../core-concepts/supported-strategies/) yang didukung. To optimize gas costs, the vault maintains a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.



